---
title: Intégration des applications de gestion avec les applications Microsoft 365 installer le programme d’installation « démarrer en un clic »
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 avec une solution de gestion de logiciels.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297313"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Intégration des applications de gestion avec les applications Microsoft 365 installer le programme d’installation « démarrer en un clic »

Découvrez comment intégrer le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 avec une solution de gestion de logiciels.
  
Le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 fournit une interface COM qui permet aux professionnels de l’informatique et au contrôle par programme des solutions de gestion des logiciels de gérer les mises à jour. Cette interface fournit des fonctionnalités de gestion supplémentaires au-delà de ce qui est fourni par l’outil déploiement d’Office.
  
> [!NOTE]
> Cet article s’applique aux applications Office qui utilisent le programme d’installation « démarrer en un clic ». 
  
## <a name="integrating-with-the-click-to-run"></a>Intégration à « démarrer en un clic »

Pour utiliser cette interface, une application de gérabilité appelle l’interface COM et appelle des API exposées qui communiquent directement avec le service d’installation « démarrer en un clic ». 
  
> [!NOTE]
> Le programme d’installation Office « démarrer en un clic » peut être exécuté à partir de la ligne de commande avec des paramètres qui peuvent contrôler le comportement, comme indiqué dans l' [outil déploiement d’Office pour démarrer en un clic](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool). 
  
**Voici un diagramme conceptuel de l’interface COM**

![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM sur le programme d’installation Office « démarrer en un clic »")
  
Le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 implémente une interface COM, **IUpdateNotify** inscrite au CLSID **CLSID_UpdateNotifyObject**.
  
Cette interface peut être appelée comme suit :
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

L’appel ne réussira que si l’appelant s’exécute sous des privilèges élevés, car le programme d’installation démarrer en un clic doit être exécuté avec des privilèges élevés.
  
L’interface com **IUpdateNotify** expose trois fonctions asynchrones chargées de la validation des commandes et des paramètres et de l’exécution de la planification avec le service d’installation « démarrer en un clic ». 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Une méthode, **Status**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou l’état de la commande en cours d’exécution (c.-à-d. réussite, échec, codes d’erreur détaillés).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Il existe quatre États selon lesquels le service d’installation « démarrer en un clic » peut se trouver pendant son cycle de vie, pendant laquelle les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactivité, téléchargement et application. 
  
**Le schéma de machine à États de l’interface COM est le suivant :**

![Diagramme d’état pour l’interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Diagramme d’État pour l’interface COM")
  
> [!NOTE]
> **Redémarrage**: lors du démarrage de l’ordinateur, le service d’installation « démarrer en un clic » n’est pas disponible. Un appel réussi à la méthode Status après un redémarrage renverra eUPDATE_UNKNOWN. 
  
**Inactif :** Lorsque le programme d’installation « démarrer en un clic » est à l’état inactif, vous pouvez appeler les éléments suivants : 
  
- **Appliquer**: installer le contenu précédemment téléchargé.
    
- **Cancel**: renvoie  `0x800000e` , « une méthode a été appelée à un moment inattendu ».
    
- **Téléchargement**: télécharge le nouveau contenu sur le client pour une installation ultérieure.
    
- **État**: renvoie le résultat de la dernière action terminée ou un message d’erreur si l’action s’est terminée en raison d’un échec. S’il n’existe aucune action précédente, **Status** renvoie  `eUPDATE_UNKNOWN` .
    
**Téléchargement :** Lorsque le programme d’installation démarrer en un clic est à l’état de téléchargement, vous pouvez appeler les éléments suivants : 
  
- **Apply**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ».
    
- **Cancel**: arrête le téléchargement et supprime le contenu partiellement téléchargé.
    
- **Téléchargement**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ». 
    
- **Status**: renvoie **DOWNLOAD_WIP** pour indiquer que le téléchargement est en cours. 
    
**Application :** Lorsque le programme d’installation « démarrer en un clic » se trouve dans le processus d’installation du contenu précédemment téléchargé : 
  
- **Apply**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ».
    
- **Cancel**: renvoie  `0x800000e` , l’action Apply ne peut pas être annulée.
    
- **Téléchargement**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ». 
    
- **État**: renvoie **APPLY_WIP** pour indiquer que l’opération d’application est en cours. 
    
> [!NOTE]
> Étant donné que OfficeC2RCOM est un service COM+ et qu’il est chargé dynamiquement, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode sur cette classe afin de vous assurer que vous obtenez le résultat attendu. Le service COM+ gère la création d’une nouvelle instance si nécessaire. Lorsqu’une des méthodes est appelée pour la première fois, COM+ charge l’objet **IUpdateNotify** et l’exécute dans l’une des instances dllhost.exe. Le nouvel objet reste actif pendant environ 3 minutes d’inactivité. Si un appel est effectué dans les trois minutes suivant le dernier appel, l’objet **IUpdateNotify** reste chargé et une nouvelle instance n’est pas créée. Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify est déchargé et un nouvel objet **IUpdateNotify** est créé lors de l’appel suivant. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guide de référence de l’API COM « démarrer en un clic »

Dans la documentation de référence de l’API suivante :
  
- Les paramètres se trouvent dans un format de paire clé/valeur séparé par un espace.
    
- Les paramètres ne respectent pas la casse.
    
- Il existe une [liste de paramètres](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) avec la documentation disponible. 
    
- Le résumé de l’interface IUpdateNotify2 est désormais inclus.
    
### <a name="apply"></a>Appliquer

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Paramètres

-  _DisplayLevel_: **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour. La valeur par défaut est **False**.
    
-  _forceappshutdown_: **true** pour obliger les applications Office à s’arrêter immédiatement lorsque l’action d' **application** est déclenchée ; **false** pour faire échouer si des applications Office sont en cours d’exécution. La valeur par défaut est **False**. Pour plus d’informations, voir [Remarques](#bk_ApplyRemark) . 
    
  Si une application Office est en cours d’exécution lorsque l’action d' **application** est déclenchée **, l’action d’application échoue** généralement. `forceappshutdown=true`En passant à la méthode **apply** , le service **OfficeClickToRun** arrête immédiatement les applications et applique la mise à jour. Dans ce cas, l’utilisateur peut subir une perte de données. 
    
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.  <br/> |
|**E_ACCESSDENIED** <br/> |L’appelant n’est pas en cours d’exécution avec des privilèges élevés.  <br/> |
|**E_INVALIDARG** <br/> |Les paramètres non valides ont été transmis.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |L’action n’est pas autorisée pour le moment. Pour plus d’informations, voir [Remarques](#bk_ApplyRemark) .  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Remarques

- Si une application Office est en cours d’exécution lorsque l’action d' **application** est déclenchée **, l’action d’application échoue** . `forceappshutdown=true`En passant à la méthode **apply** , le service **OfficeClickToRun** arrête immédiatement toutes les applications Office en cours d’exécution et applique la mise à jour. L’utilisateur peut se servir des données, car il n’est pas invité à enregistrer les modifications apportées aux documents ouverts.. 
    
- Cette action ne peut être déclenchée que lorsque le statut COM est l’un des suivants : 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si vous appelez la méthode **apply** sans télécharger le contenu précédemment, la méthode **apply** signalera la **réussite** car elle n’a pas pu s’appliquer et a terminé le processus d' **application** . 
    
### <a name="cancel"></a>Annuler

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|S_OK  <br/> |L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |L’action n’est pas autorisée pour le moment. Pour plus d’informations, consultez la section [Remarques](#bk_CancelRemarks) .  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Remarques

- Cette méthode ne peut être déclenchée que lorsque l’ID d’État COM **eDOWNLOAD_WIP**. Elle tentera d’annuler l’action de téléchargement en cours. L’état de COM passe à **eDOWNLOAD_CANCELLING** et change finalement en **eDOWNLOAD_CANCELED**. L’État COM renvoie **E_ILLEGAL_METHOD_CALL** s’il est déclenché à tout autre moment. 
    
### <a name="download"></a>Télécharger

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Paramètres

-  _DisplayLevel_: **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour. La valeur par défaut est **False**.
    
-  _updatebaseurl_: URL vers l’autre source de téléchargement.
    
-  _updatetoversion_: version à mettre à jour Office vers. Définissez ce paramètre si vous souhaitez effectuer une mise à jour vers une version antérieure à la version actuellement installée.
    
-  _downloadsource_: CLSID de l’implémentation **IBackgroundCopyManager** personnalisée (gestionnaire bits). 
    
-  _contentid_: identifie le contenu à télécharger à partir du serveur de contenu via le gestionnaire des bits personnalisé. Cette valeur est transmise à l’interprétation via l’interface BITS.
    
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.  <br/> |
|**E_ACCESSDENIED** <br/> |L’appelant n’est pas en cours d’exécution avec des privilèges élevés.  <br/> |
|**E_INVALIDARG** <br/> |Les paramètres non valides ont été transmis.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |L’action n’est pas autorisée pour le moment. Pour plus d’informations, voir [Remarques](#bk_DownloadRemark) .  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Remarques

- Vous devez spécifier  _downloadsource_ et  _contentid_ en tant que paire. Si ce n’est pas le cas, la méthode de **Téléchargement** renvoie une erreur **E_INVALIDARG** . 
    
- Si  _downloadsource_,  _contentid_et  _updatebaseurl_ sont fournis,  _updatebaseurl_ sera ignoré. 
    
- Cette action ne peut être déclenchée que lorsque le statut COM est l’un des suivants : 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si vous appelez la méthode **apply** sans le contenu précédemment téléchargé, la méthode **apply** signalera la **réussite** car elle n’a pas pu s’appliquer et a terminé le processus d' **application** . 
    
#### <a name="examples"></a>Exemples

- Pour télécharger le contenu à partir du gestionnaire des fichiers BITS personnalisé : appelez la fonction **Download ()** en transmettant les paramètres suivants : 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Pour télécharger le contenu à partir du réseau de distribution de contenu (CDN) Office : appelez la fonction **Download ()** sans spécifier les paramètres  _downloadsource_,  _contentid_ou  _updatebaseurl_ . 
    
- Pour télécharger le contenu à partir d’un emplacement personnalisé : appelez la fonction **Download ()** en transmettant le paramètre suivant : 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>Statut

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
|**S_OK** <br/> |La méthode **Status** renvoie toujours ce résultat. Inspectez la  `UPDATE_STATUS_RESULT` structure pour connaître l’état de l’action actuelle.  <br/> |
   
#### <a name="remarks"></a>Remarques

- Champ d’état de la  `UPDATE_STATUS_REPORT` contient l’état de l’action en cours. L’une des valeurs d’État suivantes est renvoyée : 
    
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

- Si la dernière commande a généré une erreur, le champ d’erreur de  `UPDATE_STATUS_REPORT` contient des informations détaillées sur l’erreur. Deux types de codes d’erreur sont renvoyés à partir de la méthode **Status** . 
    
- Si l’erreur est inférieure à  `UPDATE_ERROR_CODE::eUNKNOWN` , l’erreur est l’un des codes d’erreur prédéfinis suivants :
    
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

  Si le code d’erreur renvoyé est plus grand que  `UPDATE_ERROR_CODE::eUNKNOWN` le **HRESULT** d’un appel de fonction ayant échoué. Pour extraire la soustraction HRESULT  `UPDATE_ERROR_CODE::eUNKNOWN` de la valeur renvoyée dans le champ Error du  `UPDATE_STATUS_REPORT` .
    
  La liste complète des valeurs d’État et d’erreur peut être affichée en inspectant la bibliothèque de types **IUpdateNotify** incorporée dans OfficeC2RCom.dll. 
    
- Le champ contentid est utilisé pour les appels à l' **État** après le **Téléchargement** et renvoie le contentid qui a été transmis à l’appel de **Téléchargement** . Il est recommandé d’initialiser ce champ sur **null** avant d’appeler la méthode **Status** , puis de vérifier la valeur après que **Status** a été renvoyé. Si la valeur est toujours **null**, cela signifie qu’il n’existe aucun contentid à renvoyer. Si la valeur n’est pas **null**, vous devez la libérer avec un appel à **SysFreeString ()**. Voici un extrait de code expliquant comment appeler l' **État** après le **Téléchargement**.
    
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

À partir de la version [16.0.8208.6352] nous avons ajouté une nouvelle interface **IUpdateNotify2** . 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Cette interface hébergeait également l’interface IUpdateNotify d’origine pour assurer la compatibilité descendante. Cela signifie que si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject** . 
    
- Nouvelles méthodes ajoutées à IUpdateNotify2 :
    
  - **HRESULT** GetBlockingApps ([out] BSTR \* AppsList). Obtenir la liste des applications de blocage des mises à jour. Cet appel renverra les applications Office en cours d’exécution, ce qui bloquera le processus de mise à jour. 
    
  - **HRESULT** GetOfficeDeploymentData ([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Obtenir les données de déploiement d’Office. 
    
- Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer que :
    
  - Votre version d’C2R est plus récente que la build ci-dessus (version de la partie \> juin).
    
  - Utilisez UpdateNotifyObject2 au lieu de **UpdateNotifyObject** pour appeler **CoCreateInstance**.
    
Si vous n’utilisez aucune des nouvelles méthodes, vous n’avez pas besoin de modifier quoi que ce soit. Toutes les méthodes existantes fonctionneront exactement de la même manière qu’avant.
  
## <a name="implementing-the-bits-interface"></a>Implémentation de l’interface BITS

Le [service de transfert intelligent en arrière-plan](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (bits) est un service fourni par Microsoft pour transférer des fichiers entre un client et un serveur. BITS est l’un des canaux que le programme d’installation d’Office « démarrer en un clic » peut utiliser pour télécharger du contenu. Par défaut, le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 utilise l’implémentation intégrée de Windows BITS pour télécharger le contenu à partir du CDN. 
  
En fournissant une implémentation BITS personnalisée à la méthode de **téléchargement ()** de l’interface **IUpdateNotify** , votre logiciel de gestion peut contrôler l’emplacement et la façon dont le client télécharge le contenu. Une interface BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisé autre que les canaux intégrés « démarrer en un clic », tels que le CDN, les serveurs IIS ou les partages de fichiers. 
  
La configuration minimale requise pour une interface BITS personnalisée pour fonctionner avec le service Office C2R est la suivante :
  
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

- Pour les  `Addfile`  `AddFileWithRanges` fonctions et, l’URL distante est au format suivant : 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits est codé en dur et représente des BITS personnalisés.
    
  -  _\<contentid\>_ est le paramètre  _contentid_ de la méthode **Download ()** . 
    
  -  _\<relative path to target file\>_ indique l’emplacement et le nom de fichier du fichier à télécharger. 
    
    Par exemple, si vous avez fourni un  _contentid_ de  `f732af58-5d86-4299-abe9-7595c35136ef` à la méthode **Download ()** et que Office C2R souhaite télécharger le fichier CAB de la version, par exemple  `v32.cab` fichier, il appellera **AddFile ()** avec les éléments suivants  `RemoteUrl` :
    
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
## <a name="automating-content-staging"></a>Automatisation du transfert de contenu

Les administrateurs informatiques peuvent choisir d’activer la réception automatique des mises à jour lorsqu’elles sont disponibles directement à partir du CDN ou de contrôler le déploiement des mises à jour disponibles à partir des canaux de mise à jour à l’aide de l’outil déploiement d’Office ou du gestionnaire de configuration de point de terminaison Microsoft.
  
Le service prend en charge la possibilité pour les outils de gestion de reconnaître et d’automatiser le téléchargement du contenu lorsque des mises à jour sont disponibles.
  
**L’image suivante est une vue d’ensemble du téléchargement d’une image personnalisée**

![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM sur le programme d’installation Office « démarrer en un clic »")
  
### <a name="overview-of-downloading-a-custom-image"></a>Vue d’ensemble du téléchargement d’une image personnalisée
  
Dans le schéma précédent, vous voyez qu’une nouvelle image de Microsoft 365 Apps est disponible sur le CDN. En plus de l’image des applications Microsoft 365, une API est disponible, qui contient les informations nécessaires pour permettre aux logiciels de gestion de créer directement des images personnalisées, qui remplacent la nécessité d’utiliser l’outil déploiement d’Office.

Une entreprise configure ses services WSUS pour synchroniser les mises à jour des applications Microsoft 365. Ces mises à jour ne contiennent pas la charge utile de l’image réelle, mais elles permettent au logiciel de gérabilité de reconnaître quand un nouveau contenu est disponible. Le logiciel de gestion peut ensuite lire les métadonnées de mise à jour des applications Microsoft 365 pour comprendre la version d’Office à laquelle la mise à jour s’applique.

Si la mise à jour est applicable, le logiciel de gestion peut utiliser le contenu CDN et la liste des fichiers pour créer l’image personnalisée et la stocker sur l’emplacement de partage de fichiers qu’elle est configurée à utiliser.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Utilisation de l’API de liste de fichiers Apps 365 Microsoft

L’API de liste de fichiers Apps Microsoft 365 est utilisée pour récupérer les noms des fichiers nécessaires pour une mise à jour d’applications Microsoft 365.

Requête HTTP

GET https://config.office.com/api/filelist

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Paramètres facultatifs de la requête

|**Nom**|**Description**|
|:-----|:-----|
| channel <br/>| Spécifie le nom du canal  <br/> Facultatif-valeur par défaut : « semestriel » <br/> Valeurs prises en charge https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| version <br/>| Spécifie la version de mise à jour <br/> Optional : valeur par défaut de la dernière version disponible pour le canal spécifié |
| arcs <br/>| Spécifie l’architecture client <br/> Optional : par défaut, « x64 » <br/> Valeurs prises en charge : x64, x86 |
| abattant <br/>| Spécifie les fichiers de langue à inclure <br/> Facultatif : aucune valeur par défaut <br/> Pour spécifier plusieurs langues, incluez un paramètre de requête de capot pour chaque langue <br/> Utilisez le format d’identificateur de langue, par exemple. « en-US », « fr-fr » |
| alllanguages <br/>| Spécifie l’inclusion de tous les fichiers de langue <br/> Facultatif-valeur par défaut : false |

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets file dans le corps de la réponse.

Pour créer une image, procédez comme suit :
1.  Appelez l’API, en fournissant les paramètres de requête appropriés pour le canal, la version et l’architecture de la mise à jour qui vous intéressent.
Remarque : les objets file avec l’attribut « LCID » : « 0 » sont des fichiers de langue neutre et doivent être inclus dans l’image.
2.  Construisez une image locale du CDN en effectuant une itération dans les objets fichier et en copiant les fichiers CDN, lors de la création de la structure de dossiers spécifiée par l’attribut « relativePath » défini pour chaque objet fichier.

L’exemple suivant récupère la liste des fichiers du canal actuel et de la version 16.0.4229.1004 pour 64 bits et inclut les fichiers de langue française et anglaise :

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Vérification de hachage des fichiers. dat

Les outils de création d’image peuvent vérifier l’intégrité des fichiers. dat téléchargés en comparant une valeur de hachage calculée avec la valeur de hachage fournie associée à chacun des fichiers. dat. Voici un exemple d’un objet file qui spécifie les valeurs hashLocation et hashAlgorithm :
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- L’attribut **hashLocation** spécifie l’emplacement de chemin d’accès relatif du fichier. cab qui contient la valeur de hachage. Construisez l’emplacement du fichier de hachage en concaténant URL + relativePath + hashLocation. Dans l’exemple suivant, l’emplacement stream.x64.bg-bg. hash doit être : 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- L’attribut **HashAlgorithm** spécifie l’algorithme de hachage qui a été utilisé. 
    
  Pour valider l’intégrité du fichier stream.x64.bg-bg. dat, ouvrez stream.x64.bg-bg. Hash et lisez la valeur de hachage qui est la première ligne de texte dans le fichier de hachage. Comparez ceci à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier. dat téléchargé.
    
  L’exemple suivant montre le code C# permettant de lire le hachage.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Mises à jour des applications Microsoft 365

Toutes les mises à jour des applications Microsoft 365 sont publiées dans le [catalogue Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Les mises à jour des applications Microsoft 365 permettent aux logiciels de gérabilité de traiter les mises à jour des applications Microsoft 365 de la même manière que n’importe quelle autre mise à jour WU, à une exception près : les mises à jour du client ne contiennent pas de charge utile réelle. Les mises à jour des applications Microsoft 365 ne doivent pas être installées sur les clients, mais plutôt utilisées pour déclencher les flux de travail avec le logiciel de gérabilité en remplaçant la commande d’installation par le mécanisme d’installation basé sur COM indiqué ci-dessus.

**La figure suivante illustre un diagramme du flux de travail de mise à jour du client Office 365.**

![Diagramme de flux de travail pour les mises à jour du client O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")
  
Chaque mise à jour des applications Microsoft 365 publiée inclut des métadonnées sur la mise à jour. Ces métadonnées incluent un paramètre nommé MoreInfoUrl qui peut être utilisé pour dériver l’appel de l’API à l’API de liste de fichiers pour cette mise à jour spécifique.

Dans l’exemple suivant, l’API de liste de fichiers est incorporée dans le MoreInfoURL et commence par « ServicePath = »

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Métadonnées supplémentaires pour l’automatisation du transfert de contenu

**API d’historique des versions**
  
L’API d’historique de publication des applications Microsoft 365 est utilisée pour récupérer les détails de chacune des mises à jour publiées sur le CDN, ainsi que les noms de canal et d’autres attributs de canal.

Requête HTTP

```http
GET https://config.office.com/api/filelist/channels 
```

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets file dans le corps de la réponse.

**API UGS**
  
L’API SKU renvoie des informations utiles pour déterminer les produits disponibles pour le déploiement et la maintenance à partir du CDN Office, ainsi que diverses options pour chacun d’eux.

Requête HTTP

```http
GET https://config.office.com/api/filelist/skus 
```

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets file dans le corps de la réponse.
