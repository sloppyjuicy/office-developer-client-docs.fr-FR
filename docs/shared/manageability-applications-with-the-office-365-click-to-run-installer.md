---
title: Intégration d’applications de gestion avec Office 365 click-to-run installer
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d’installation Office 365 Click-to-Run avec une solution de gestion de logiciels.
ms.openlocfilehash: abe941e3e3818eed1f18108f1678e46e8156b08c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787943"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a>Intégration d’applications de gestion avec Office 365 click-to-run installer

Découvrez comment intégrer le programme d’installation Office 365 Click-to-Run avec une solution de gestion de logiciels.
  
Le programme d’installation Office 365 Click-to-Run fournit une interface COM qui permet de contrôler par programme de gestion de la mise à jour professionnels de l’informatique et les solutions de gestion de logiciels. Cette interface fournit des fonctions de gestion supplémentaires au-delà de celles fournies par l’outil de déploiement d’Office.
  
> [!NOTE]
> Cet article s’applique à Office 2016 et versions ultérieures, Office 365. 
  
## <a name="integrating-with-the-click-to-run"></a>Intégration avec Click-to-Run

Pour utiliser cette interface, une application de gestion appelle l’interface COM et appelle exposé API qui communiquent directement avec le service d’installation Click-to-Run. 
  
> [!NOTE]
> Le programme d’installation Office Click-to-Run peut être exécutée à partir de la ligne de commande avec les paramètres qui peuvent contrôler le comportement, comme indiqué dans [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117). 
  
**Voici un diagramme conceptuel de l’interface COM**

![Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run")
  
L’interface implémente com. installer Office 365 Click-to-Run, **IUpdateNotify** inscrit à CLSID **CLSID_UpdateNotifyObject**.
  
Cette interface peut être appelée comme suit :
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

L’appel réussit uniquement si l’appelant s’exécute avec des privilèges élevés, comme le programme d’installation Click-to-Run doit être exécuté avec des privilèges élevés.
  
L’interface **IUpdateNotify** COM expose trois fonctions asynchrones responsables de la validation les commandes et paramètres et planification de l’exécution avec le service d’installation Click-to-Run. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Une autre méthode, **état**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou l’état de la commande en cours d’exécution (succès, échec, les codes d’erreur détaillé).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Il existe quatre états que le service d’installation Click-to-Run peut prendre au cours de son cycle de vie, pendant laquelle les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactif, le téléchargement et l’application. 
  
**Voici le diagramme de la Machine à états Interface COM**

![Un diagramme d’état de l’interface COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Un diagramme d’état de l’interface COM")
  
> [!NOTE]
> **Redémarrage**: démarrage de l’ordinateur est un certain temps lorsque le service du programme d’installation Click-to-Run n’est pas disponible. Un appel réussi à la méthode état après un redémarrage renverra eUPDATE_UNKNOWN. 
  
**Inactif :** Lorsque le programme d’installation Click-to-Run se trouve dans l’état d’inactivité, vous pouvez appeler : 
  
- **Appliquer**: Install déjà téléchargé du contenu.
    
- **Annuler**: renvoie `0x800000e`, « une méthode a été appelée à un moment inattendu ».
    
- **Télécharger**: télécharge le nouveau contenu pour l’installation du client pour une version ultérieure.
    
- **État**: renvoie le résultat de la dernière action terminée, ou un message d’erreur si l’action s’est terminée en échec. S’il n’existe aucune action précédente, **état** renvoie `eUPDATE_UNKNOWN`.
    
**Téléchargement :** Lorsque le programme d’installation Click-to-Run se trouve dans l’état de téléchargement, vous pouvez appeler : 
  
- **Appliquer**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ».
    
- **Annuler**: arrête le téléchargement et supprime le contenu téléchargé partiellement.
    
- **Télécharger**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ». 
    
- **État**: renvoie **DOWNLOAD_WIP** pour indiquer que le travail de téléchargement est en cours. 
    
**Application :** Lorsque le programme d’installation Click-to-Run est en cours d’installation précédemment télécharger du contenu : 
  
- **Appliquer**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ».
    
- **Annuler**: renvoie `0x800000e`, l’action Appliquer ne peut pas être annulée.
    
- **Télécharger**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ». 
    
- **État**: renvoie **APPLY_WIP** pour indiquer qui applique le travail est en cours. 
    
> [!NOTE]
> Étant donné que OfficeC2RCOM est un service COM + et est chargé de manière dynamique, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode de cette classe pour vous assurer que vous obtenez le résultat attendu. Service COM + gère la création d’une nouvelle instance si nécessaire. Lorsqu’une des méthodes est appelée pour la première fois, COM + charge l’objet **IUpdateNotify** et exécutez-le dans une des instances de dllhost.exe. Le nouvel objet restera actif pendant environ 3 minutes dans inactif. Si un appel suivant est effectué dans les trois minutes du dernier appel, l’objet **IUpdateNotify** restera chargé et une nouvelle instance n’est pas créée. Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify doit être déchargé et un nouvel objet **IUpdateNotify** sera créé lors de l’appel suivant. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guide de référence des API COM Click-to-Run installer

Dans la documentation de référence API suivante :
  
- Les paramètres sont dans un format de paire clé/valeur séparée par un espace.
    
- Les paramètres ne respectent pas la casse.
    
- Il existe une [liste de paramètres](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) avec la documentation disponible. 
    
- Résumé de l’interface IUpdateNotify2 est désormais inclus.
    
### <a name="apply"></a>Appliquer

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Paramètres

-  _DisplayLevel_: **true** pour afficher l’état d’installation, y compris les erreurs, au cours du processus de mise à jour ; **false** pour masquer l’état d’installation, y compris les erreurs, au cours du processus de mise à jour. La valeur par défaut est **false**.
    
-  _forceappshutdown_: **la valeur true** pour forcer l’archivage des applications Office à arrêter immédiatement l’action **Appliquer** déclenchement ; **false** échoue si toutes les applications Office sont en cours d’exécution. La valeur par défaut est **false**. Pour plus d’informations, consultez la [section Notes](#bk_ApplyRemark) . 
    
  Si n’importe quelle application Office est en cours d’exécution lors de l’action **Appliquer** est déclenchée, l’action **Appliquer** généralement échoue. Transmission `forceappshutdown=true` pour **Appliquer** la méthode provoque le service **OfficeClickToRun** arrêter les applications et appliquer la mise à jour immédiatement. L’utilisateur peut rencontrer une perte de données dans ce cas. 
    
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |Action a bien été envoyée au service Click-To-Run pour l’exécution.  <br/> |
|**E_ACCESSDENIED** <br/> |L’appelant n’est pas en cours d’exécution avec des privilèges élevés.  <br/> |
|**E_INVALIDARG** <br/> |Paramètres non valides ont été transmis.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Action n’est pas autorisée à ce stade. Pour plus d’informations, consultez la [section Notes](#bk_ApplyRemark) .  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Remarques

- Si n’importe quelle application Office est en cours d’exécution lors de l’action **Appliquer** est déclenchée, l’action **Appliquer** échouera. Transmission `forceappshutdown=true` pour **Appliquer** la méthode provoque le service **OfficeClickToRun** arrêter immédiatement toutes les applications Office qui sont en cours d’exécution et appliquent la mise à jour. L’utilisateur peut rencontrer données comme ils ne sont pas invités à enregistrer les modifications pour ouvrir des documents... 
    
- Cette action ne peut être déclenchée lorsque le statut COM est une des options suivantes : 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si vous appelez la méthode **Apply** sans télécharger le contenu précédemment, la méthode **Apply** signalera **réussi** détecté rien à appliquer et réussi le processus à **Appliquer** . 
    
### <a name="cancel"></a>Cancel

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|S_OK  <br/> |Action a bien été envoyée au service Click-to-Run pour l’exécution.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Action n’est pas autorisée à ce stade. Consultez la section [Notes](#bk_CancelRemarks) pour plus d’informations  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Remarques

- Cette méthode peut uniquement être déclenché lorsque l' id du statut COM **eDOWNLOAD_WIP**. Il essaie d’annuler l’opération de téléchargement en cours. L’état COM sera Remplacez **eDOWNLOAD_CANCELLING** et finalement à **eDOWNLOAD_CANCELED**. L’état COM renverra **E_ILLEGAL_METHOD_CALL** si déclenché à tout moment. 
    
### <a name="download"></a>Téléchargement

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Paramètres

-  _DisplayLevel_: **true** pour afficher l’état d’installation, y compris les erreurs, au cours du processus de mise à jour ; **false** pour masquer l’état d’installation, y compris les erreurs, au cours du processus de mise à jour. La valeur par défaut est **false**.
    
-  _updatebaseurl_: URL de la source de téléchargement de substitution.
    
-  _updatetoversion_: la version mise à jour Office. Définissez ce paramètre si vous souhaitez mettre à jour vers une version antérieure à la version actuellement installée.
    
-  _downloadsource_: le CLSID de l’implémentation de **IBackgroundCopyManager** personnalisé (Gestionnaire de BITS). 
    
-  _contentid_: identifie le contenu à télécharger à partir du serveur de contenu via le Gestionnaire de BITS personnalisé. Cette valeur est transmise par le biais de l’interface de BITS pour interprétation.
    
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |Action a bien été envoyée au service Click-To-Run pour l’exécution.  <br/> |
|**E_ACCESSDENIED** <br/> |L’appelant n’est pas en cours d’exécution avec des privilèges élevés.  <br/> |
|**E_INVALIDARG** <br/> |Paramètres non valides ont été transmis.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Action n’est pas autorisée à ce stade. Pour plus d’informations, consultez la [section Notes](#bk_DownloadRemark) .  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Remarques

- Vous devez spécifier _downloadsource_ et _contentid_ comme une paire. Si ce n’est pas le cas, la méthode **Télécharger** renverra une erreur **E_INVALIDARG** . 
    
- Si _downloadsource_, _contentid_et _updatebaseurl_ sont fournis, _updatebaseurl_ sera ignorée. 
    
- Cette action ne peut être déclenchée lorsque le statut COM est une des options suivantes : 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si vous appelez la méthode **Apply** sans contenu téléchargé précédemment, la méthode **Apply** signalera **réussi** détecté rien à appliquer et réussi le processus à **Appliquer** . 
    
#### <a name="examples"></a>Exemples

- Pour télécharger le contenu à partir du Gestionnaire de BITS personnalisé : appelez la fonction **download()** en passant les paramètres suivants : 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Pour télécharger le contenu à partir du CDN Microsoft : appelez la fonction **download()** sans spécifier les paramètres _downloadsource_, _contentid_ou _updatebaseurl_ . 
    
- Pour télécharger le contenu à partir d’un emplacement personnalisé : appelez la fonction **download()** en passant le paramètre suivant : 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>État

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a>Paramètres

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Pointeur vers une structure UPDATE_STATUS_REPORT.  <br/> |
   
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |La méthode **Status** renvoie toujours ce résultat. Inspecter les `UPDATE_STATUS_RESULT` structure de l’état de l’action en cours.  <br/> |
   
#### <a name="remarks"></a>Remarques

- Le champ État de la `UPDATE_STATUS_REPORT` contient l’état de l’action en cours. Une des valeurs d’état suivant est retournée : 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- Si la dernière commande a provoqué une erreur, le champ d’erreur de le `UPDATE_STATUS_REPORT` contient des informations détaillées sur l’erreur. Deux types de codes d’erreur sont renvoyés à partir de la méthode **d’état** . 
    
- Si l’erreur inférieure à `UDPATE_ERROR_CODE::eUNKNOWN`, l’erreur est un des codes d’erreur prédéfinis suivants :
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  Si le code d’erreur retourné est supérieur à `UDPATE_ERROR_CODE::eUNKNOWN` il s’agit d’un appel de fonction qui a échoué **HRESULT** . Pour extraire le HRESULT soustraire `UDPATE_ERROR_CODE::eUNKNOWN` à partir de la valeur renvoyée dans le champ d’erreur de le `UPDATE_STATUS_REPORT`.
    
  La liste complète des valeurs d’erreur et d’état sont consultables en examinant la bibliothèque de type **IUpdateNotify** incorporée dans OfficeC2RCom.dll. 
    
- Le champ contentid est utilisé pour les appels à **l’état** après **téléchargé** a lancé et renvoie le contentid qui a été passé à l’appel à **Télécharger** . Il est recommandé d’initialiser ce champ **null** avant d’appeler la méthode **Status** et puis vérifiez la valeur une fois que **l’état** a été renvoyé. Si la valeur est toujours **null**, qui signifie qu’il n’existe aucune contentid à renvoyer. Si la valeur n’est pas **null**, vous devez le libérer avec un appel à **SysFreeString()**. Voici un extrait de code d’appel **d’état** après le **téléchargement**.
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a>Résumé de l’interface IUpdateNotify2

> [!NOTE]
> Ce résumé est fourni en tant que les informations de complément pour [intégrer la gestion des applications avec le programme d’installation Office 365-un clic](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx). Une fois que le document public est mis à jour, ce document peut être considéré comme obsolète. 
  
À partir de C2RTenant [16.0.8208.6352](http://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (première version accessible au public doit être build de diriger juin--8326.*), nous avons ajouté une nouvelle interface **IUpdateNotify2** . Voici certaines informations de base sur cette interface : 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Cette interface hébergée également l’interface IUpdateNotify d’origine pour des raisons de compatibilité descendante. Ce qui signifie que si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject** . 
    
- Nouvelles méthodes ajoutées à IUpdateNotify2 :
    
  - **HRESULT** GetBlockingApps ([out] BSTR \* AppsList). Obtenir des mises à jour de la liste des applications de blocage. Cet appel renverra les applications Office en cours d’exécution qui bloquent le processus de mise à jour de continuer. 
    
  - **HRESULT** GetOfficeDeploymentData ([in] type de données int, [in] pcwszName **LPCWSTR** , [out] BSTR * OfficeData). Obtenir les données de déploiement d’Office. 
    
- Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer :
    
  - Votre version C2R est plus récente que la version ci-dessus (\>= juin diriger version).
    
  - Utilisez UpdateNotifyObject2, au lieu **UpdateNotifyObject** pour appeler **CoCreateInstance**.
    
Si vous n’utilisez pas les nouvelles méthodes, vous n’avez pas besoin pour les modifier. Toutes les méthodes existants fonctionnera exactement la même manière qu’avant.
  
## <a name="implementing-the-bits-interface"></a>Implémentation de l’interface de BITS

Le [Service Background Intelligent Transfer Service](https://msdn.microsoft.com/en-us/library/bb968799(v=vs.85).aspx) (BITS) est un service fourni par Microsoft pour transférer des fichiers entre un client et le serveur. BITS est un des canaux de programme d’installation Office Click-To-Run permettre utiliser pour télécharger le contenu. Par défaut, le Office Click-To-Run programme d’installation utilise Windows créées dans l’implémentation de BITS pour télécharger le contenu à partir du CDN. 
  
En fournissant une implémentation personnalisée de BITS à la méthode **download()** de l’interface **IUpdateNotify** , votre logiciel de gestion peut contrôler où et comment le client télécharge le contenu. Une interface de BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisés autres que les canaux intégrés Click-to-Run, tel que du CDN Office, serveurs IIS, ou les partages de fichiers. 
  
La configuration minimale requise pour une interface personnalisée de BITS fonctionner avec Office C2R service est :
  
- Pour **IBackgroundCopyManager**:
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- Pour **IBackgroundCopyJob**:
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- Pour **IBackgroundCopyJob3**:
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- Pour le `Addfile` et `AddFileWithRanges` fonctions, l’URL à distance est au format suivant : 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits est codé en dur et signifie BITS personnalisées.
    
  -  _ \<contentid\> _ est le paramètre _contentid_ pour la méthode **Download()** . 
    
  -  _ \<chemin d’accès relatif au fichier cible\> _ fournit le nom de fichier et emplacement du fichier à télécharger. 
    
    Par exemple, si vous avez fourni une _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` à la **Download()** méthode et C2R Office souhaite télécharger le fichier cab de version, tel que `v32.cab` fichier, il appelle **AddFile()** par ce qui suit `RemoteUrl`:
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Pour **IBackgroundCopyError**:
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Pour **IBackgroundCopyFile**:
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://support.office.com/en-us/article/Overview-of-update-channels-for-Office-365-ProPlus-9ccf0f13-28ff-4975-9bd2-7e4ea2fefef4?ui=en-US&rs=en-US&ad=US) using the [Office 2016 Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or [System Center Configuration Manager](https://support.office.com/en-us/article/Manage-updates-to-Office-365-ProPlus-with-System-Center-Configuration-Manager-b4a17328-fcfe-40bf-9202-58d7cbf1cede).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="http://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
http://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a>Automatisation de test de contenu

Les administrateurs informatiques peuvent choisir pour que les clients de bureau configurés pour recevoir des mises à jour automatiquement lorsqu’elles sont disponibles directement à partir de la Microsoft réseau CDN (Content Delivery), ou ils peuvent choisir de contrôler le déploiement des mises à jour disponibles à partir de la mise à jour canaux à l’aide de l’outil de déploiement Office ou System Center Configuration Manager.
  
Le service prend en charge la possibilité pour les outils de gestion pour qu’il reconnaisse et automatiser le téléchargement du contenu lors de mises à jour sont disponibles.
  
**L’image suivante est une vue d’ensemble de télécharger une image personnalisée**

![Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run")
  
### <a name="overview-of-downloading-a-custom-image"></a>Vue d’ensemble de télécharger une image personnalisée
  
Dans le diagramme précédent, vous voyez qu’une nouvelle image d’Office 365 ProPlus est disponible sur le réseau de Distribution contenu (CDN) Office. Avec l’image d’Office 365 ProPlus, une liste de fichiers au format XML est également disponible qui contient les informations nécessaires pour activer le logiciel de gestion créer directement des images personnalisées en remplaçant la nécessité d’utiliser l’outil de déploiement d’Office.
  
Une entreprise configure leurs WSUS pour synchroniser les mises à jour de Client Office 365. Ces mises à jour ne contiennent pas de la charge utile réelle de l’image, mais n’autorise pas le logiciel de gestion reconnaître lorsque le nouveau contenu est disponible. Le logiciel de gestion peut ensuite lire les métadonnées de mise à jour du Client pour comprendre de quelle version d’Office que la mise à jour s’applique à.
  
Si la mise à jour est applicable, le logiciel de gestion permettre utiliser le contenu CDN et la liste des fichiers pour créer l’image personnalisée et le stocker sur l’emplacement de partage de fichiers est configuré pour utiliser.
  
### <a name="format-of-the-xml-file-list"></a>Format de la liste des fichiers XML

Il existe deux listes de fichiers dans un fichier cab sur le CDN. 1 répertorie les fichiers pour la version 32 bits d’Office et l’autre pour la version 64 bits d’Office. L’URL de l’emplacement de la liste des fichiers Office (OFL. Fichier CAB) est [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). Les listes de deux fichiers sont appelées :
  
- O365Client_32bit.Xml
    
- O365Client_64bit.Xml
    
Dans le code XML pour chaque fichier listes est un <UpdateFiles> nœud qui contient un attribut de version.  `<UpdateFiles version="1.4">`. Cette version est incrémentée si des modifications sont apportées aux listes de fichiers.
  
Il existe deux paramètres qui doivent être combinés avec le code XML pour créer une image personnalisée : 
  
- Remplacez la *version %* par le numéro de version d’Office. Il peut être dérivé les métadonnées de mise à jour du Client (expliquée dans la section suivante). 
    
- Définir *baseURL* à l’aide de la valeur de l’URL associée à la branche qu'est créée pour l’image. Il est dérivé les métadonnées de la mise à jour du Client, expliquée dans la section suivante. 
    
Les étapes de création d’une image sont les suivants :
  
1. Ouvrez la liste des fichiers XML.
    
2. Remplacez les occurrences de *version %* avec la version Office applicable. Le numéro de version peut être acquis à partir de releasehistory.xml comme décrit plus loin dans cet article. 
    
3. Lire l’attribut URL de la branche cible.
    
4. Supprimer des nœuds de langue pour les langues non requis dans l’image personnalisée.
    
   > [!NOTE]
   > Les nœuds de langage = « 0 » sont linguistiquement neutre et doit être inclus dans l’image. 
  
5. Construire une image locale du CDN par itération dans la liste des fichiers XML et la copie des fichiers CDN, lors de la création de la structure de dossiers selon vos besoins. 
    
   - Si l’attribut *rename* est fourni, puis se *Renommer* le fichier copié à la valeur fournie dans l’attribut renommer. Cela permet de créer des fichiers v64.cab et v32.cab la valeur par défaut de niveau supérieur. Ces sont les versions du fichier cab plus haut niveau de build renommées et sont utilisés en tant que la version d’installation par défaut si la version n’est pas spécifiée. 
    
   - Utiliser des URL relativePath + nom de fichier pour construire l’emplacement CDN.
    
Voici des exemples qui utilisent le canal mensuel (tel que défini par le `<baseURL>` nœud) et créer la version 16.0.4229.1004 à partir de releasehistory.xml. 
  
```xml
<baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- Voici un fichier neutre linguistiques nécessaire pour toutes les langues. Le nom du fichier est v64_16.0.4229.1004.cab et il doit être copié à partir de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` et renommé en `…/office/data/v64.cab`. 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- Ce qui suit est un fichier à inclure dans l’image en-US comme indiqué par le langage LCID = 1033. Le nom du fichier est s641033.cab et il doit être copié à partir de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` et pas renommé.
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a>Vérification du hachage des fichiers .dat

Outils de création d’image peuvent vérifier l’intégrité des fichiers téléchargés .dat en comparant une valeur de hachage calculée avec la valeur de hachage fournie associée à chacun des fichiers .dat. Voici un exemple d’un fichier .dat du canal avec 16.0.4229.1004 de version et langue à bulgare mensuel :
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- L’attribut **hashLocation** Spécifie l’emplacement de chemin d’accès relatif de le stream.x64.bg-bg.hash pour le fichier stream.x64.bg-bg.dat. Construire l’emplacement du fichier hachage en concaténant URL relativePath + hashLocation. Dans l’exemple suivant, l’emplacement de stream.x64.bg-bg.hash serait : 
    
  ```http
  http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- L’attribut **hashAlgo** indique quel algorithme de hachage utilisé. Dans ce cas Sha256 a été utilisé. 
    
  Pour valider l’intégrité du fichier stream.x64.bg-bg.dat, ouvrez le stream.x64.bg-bg.hash et lisez la valeur de hachage qui est la première ligne de texte dans le fichier de hachage. Comparez cela à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier téléchargé .dat.
    
  L’exemple suivant montre le code c# pour lire la valeur de hachage.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a>Mises à jour du Client Office 365

Toutes les mises à jour Office 365 Client sont publiés dans le [Catalogue Microsoft Update](http://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Mises à jour du Client Office 365 activer le logiciel de gestion traiter les mises à jour Office 365 Client d’une manière très similaire à n’importe quel autre WU mise à jour avec une exception ; les mises à jour client ne contiennent pas une charge réelle. Les mises à jour de Client Office 365 ne doivent pas être installé sur les clients mais plutôt utilisées pour déclencher le flux de travail avec le logiciel de gestion en remplaçant la commande d’installation avec COM en fonction de mécanisme d’installation ci-dessus. 
  
**La figure suivante illustre un diagramme du flux de travail de mise à jour du Client Office 365.**

![Diagramme de flux de travail pour les mises à jour du client O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")
  
Chaque Office 365 mise à jour cliente qui est publiée inclut les métadonnées relatives à la mise à jour. Ces métadonnées incluent un paramètre appelé *MoreInfoUrl* qui peut être utilisé pour obtenir les informations suivantes : 
  
-  *Ver*: identifie la version d’Office associée à cette mise à jour. 
    
-  *Branche*: identifie le canal de mise à jour pour cette mise à jour. Les valeurs sont InsiderFast, initiés, tous les mois, cibles, requête large. Valeurs supplémentaires peuvent être ajoutées à l’avenir. 
    
-  *Forme d’arc courbé*: identifie l’architecture de processeur associé à cette mise à jour. 
    
-  *xmlVer*: la version des listes de fichiers XML qui doit être utilisé pour construire l’image de base pour cette mise à jour. 
    
-  *xmlPath*: chemin d’accès à la OFL. Répertorie les fichiers CAB qui contient le fichier XML. 
    
-  *mlFile*: le nom de la liste des fichiers qui doit être utilisée pour cette mise à jour. La valeur sera O365Client_32bit ou O365Client_64bit et correspond à la forme d’arc courbé. 
    
L’URL suivante est un exemple du paramètre *MoreInfoURL* qui fait référence pour les versions de mise à jour du client Office 365 pour la version 32 bits d’Office avec le numéro de version de 16.0.2342.2343 sur le canal en cours. 
  
http://officecdn.microsoft.com/pr/wsus/ofl.cabest l’emplacement des listes de fichiers XML pour cette mise à jour, spécifiquement le O365Client_32bit.xml à partir de la OFL. CAB.
  
[Versions de canal de mise à jour de client Office 365](http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a>Métadonnées supplémentaires pour l’automatisation de test de contenu

Outre les métadonnées qui sont publiée qui définit il sont également des fichiers XML publiés du CDN qui peuvent aider à fournir des informations supplémentaires sur les clients Office 365 qui sont disponibles à partir du CDN Office.
  
**SKU. XML**
  
Ce fichier XML est contenu dans un fichier CAB signé et publié du CDN Office à l’adresse suivante : [http://officecdn.microsoft.com/pr/wsus/skus.cab](http://officecdn.microsoft.com/pr/wsus/skus.cab).
  
Les métadonnées publiées dans ce fichier XML sont utile pour déterminer les produits qui sont disponibles pour le déploiement et de maintenance à partir du CDN Office ainsi que les différentes options pour chacun. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

** \<ReleaseInfo\> ** nœud racine contient l’attribut PublishedDate qui identifie la date à laquelle ce fichier a été publié. 
  
** \<SKU\> ** nœud identifie un référence SKU individuelle. 
  
- L’attribut *ProductID* identifie l’ID qui est passé en tant que l’attribut ID de la configuration.xml si vous utilisez l’outil de détection Office. Par exemple, `<Product ID="O365ProPlusRetail">`. 
    
- La *valeur par défaut* d’attributs, si la valeur True, identifie la référence SKU recommandé. 
    
** \<Application\> ** nœuds sont utilisés pour définir les applications Office individuelles qui prend en charge par chaque version cliente. 
  
- L’attribut *Name* est le nom d’application affiché. 
    
- L’attribut *AppID* est l’attribut ID passé le configuration.xml pour le ** \<ExcludeApp\> ** nœud si vous utilisez l’outil de détection Office. Par exemple, `<ExcludeApp ID="Publisher" />`. 
    
**RELEASEHISTORY. XML**
  
Ce fichier XML est contenu dans un fichier CAB signé et publié du CDN Office à l’emplacement suivant : [http://officecdn.microsoft.com/pr/wsus/releasehistory.cab](http://officecdn.microsoft.com/pr/wsus/releasehistory.cab). 
  
Les métadonnées publiées dans ce fichier XML sont utile pour déterminer quels sont les canaux sont prises en charge pour la maintenance des mises à jour à partir du CDN Office ainsi que des informations sur l’historique de génération pour chacun des canaux pris en charge.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

Le ** \<ReleaseHistory\> ** nœud racine contient l’attribut PublishedDate qui identifie la date à laquelle ce fichier a été publié. 
  
Le ** \<UpdateChannel\> ** nœud définit un canal pris en charge. 
  
- L’attribut *Name* définit l’ID du canal qui est utilisé pour passer à l’outil de détection Office dans le configuration.xml en tant que l’attribut de canal. 
    
  Exemple : `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">` 
    
  > [!NOTE] 
  > Cet attribut est déconseillé et est utilisé pour la compatibilité descendante uniquement. Utilisez l’attribut ID à la place de l’attribut Name. 
    
- L’attribut *ID* définit l’ID du canal qui est utilisé pour passer à l’outil de détection Office dans le configuration.xml en tant que l’attribut de canal. 
    
  Exemple : `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">` 
    
- L’attribut **DisplayName** est utilisé comme nom d’affichage. 
    
Le ** \<mettre à jour\> ** nœud permet de définir chaque mise à jour qui a été publié pour ce canal donné. 
  
- Attribut la **plus récente** , si la valeur True, définit la mise à jour est la version la plus récente pour ce canal. 
    
- L’attribut **Version** définit le numéro de version de cette mise à jour particulière. 
    
- L’attribut **LegacyVersion** définit le numéro de version complète de cette mise à jour particulière. 
    
- L’attribut **Build** définit le numéro de version de cette mise à jour particulière. 
    
- L’attribut **PubTime** définit la date et l’heure à laquelle cette mise à jour a été publié sur le CDN Office. 
    

