---
title: Intégration d’applications de gestion Microsoft 365 Apps programme d’installation « Exécuter en un clic
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d Microsoft 365 Apps d’installation « En un clic » à une solution de gestion des logiciels.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297313"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Intégration d’applications de gestion Microsoft 365 Apps programme d’installation « Exécuter en un clic

Découvrez comment intégrer le programme d Microsoft 365 Apps d’installation « En un clic » à une solution de gestion des logiciels.
  
Le Microsoft 365 Apps installer « En un clic » fournit une interface COM qui permet aux professionnels de l’informatique et aux solutions de gestion de logiciels de contrôler par programme la gestion des mises à jour. Cette interface offre des fonctionnalités de gestion supplémentaires au-delà de ce qui est fourni par l’outil Office Deployment.
  
> [!NOTE]
> Cet article s’applique Office applications qui utilisent le programme d’installation « En un clic ». 
  
## <a name="integrating-with-the-click-to-run"></a>Intégration à l’outil « Click-to-Run

Pour utiliser cette interface, une application de gestion appelle l’interface COM et appelle les API exposées qui communiquent directement avec le service d’installation « En un clic ». 
  
> [!NOTE]
> Le programme d’installation Office « En un clic » peut être exécuté à partir de la ligne de commande avec des paramètres qui peuvent contrôler le comportement, comme documenté dans [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool). 
  
**Voici un diagramme conceptuel de l’interface COM**

![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM Office programme d’installation « Exécuter en un clic")
  
Le Microsoft 365 Apps installer « En un clic » implémente une interface COM, **IUpdateNotify** inscrite dans CLSID **CLSID_UpdateNotifyObject**.
  
Cette interface peut être invoquée comme suit :
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

L’appel réussit uniquement si l’appelant s’exécute avec des privilèges élevés, car le programme d’installation « En un clic » doit être exécuté avec des privilèges élevés.
  
L’interface COM **IUpdateNotify** expose trois fonctions asynchrones responsables de la validation des commandes et des paramètres et de la planification de l’exécution avec le service d’installation « En un clic ». 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Une autre méthode, **Status**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou sur l’état de la commande en cours d’exécution (réussite, échec, codes d’erreur détaillés).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Il existe quatre états dans lesquels le service d’installation « En un clic » peut se trouver pendant son cycle de vie, au cours duquel les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactivité, téléchargement et application. 
  
**Voici le diagramme de la machine à états de l’interface COM**

![Diagramme d’état pour l’interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Diagramme d’état pour l’interface COM")
  
> [!NOTE]
> **Redémarrage**: lorsque l’ordinateur démarre, le service d’installation Démarrer en un clic n’est pas disponible pendant un certain temps. Un appel réussi à la méthode Status après un redémarrage eUPDATE_UNKNOWN. 
  
**Inactif :** Lorsque le programme d’installation En un clic est inactif, vous pouvez appeler : 
  
- **Appliquer**: installer le contenu précédemment téléchargé.
    
- **Cancel**: renvoie  `0x800000e` « Une méthode a été appelée à un moment inattendu ».
    
- **Téléchargement**: télécharge le nouveau contenu sur le client pour une installation ultérieure.
    
- **État**: renvoie le résultat de la dernière action terminée ou un message d’erreur si l’action s’est terminée en échec. S’il n’existe aucune action précédente, **l’état** renvoie  `eUPDATE_UNKNOWN` .
    
**Téléchargement :** Lorsque le programme d’installation En un clic est à l’état de téléchargement, vous pouvez appeler : 
  
- **Appliquer**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ».
    
- **Cancel**: arrête le téléchargement et supprime le contenu partiellement téléchargé.
    
- **Téléchargement**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ». 
    
- **Status**: renvoie **DOWNLOAD_WIP** pour indiquer que le travail de téléchargement est en cours. 
    
**Application :** Lorsque le programme d’installation En un clic est en cours d’installation, téléchargez préalablement le contenu : 
  
- **Appliquer**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ».
    
- **Cancel**: renvoie  `0x800000e` , l’action Appliquer ne peut pas être annulée.
    
- **Téléchargement**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ». 
    
- **État**: renvoie **APPLY_WIP** pour indiquer que le travail en cours d’application est en cours. 
    
> [!NOTE]
> Étant donné qu’OfficeC2RCOM est un service COM+ et est chargé dynamiquement, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode sur cette classe pour vous assurer que vous obtenez le résultat attendu. Le service COM+ gère la création d’une instance si nécessaire. Lorsqu’une des méthodes est appelée pour la première fois, COM+ charge l’objet **IUpdateNotify** et l’exécute dans l’une dllhost.exe instances. Le nouvel objet reste actif pendant environ 3 minutes en cas d’inactivité. Si un appel ultérieur est effectué dans les trois minutes suivant le dernier appel, l’objet **IUpdateNotify** reste chargé et une nouvelle instance n’est pas créée. Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify est déchargé et un nouvel objet **IUpdateNotify** est créé lors de l’appel suivant. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guide de référence de l’API COM du programme d’installation « Exécuter en un clic »

Dans la documentation de référence de l’API suivante :
  
- Les paramètres sont au format paire clé/valeur séparés par un espace.
    
- Les paramètres ne sont pas sensibles à la cas.
    
- Il existe une [liste de paramètres avec](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) la documentation disponible. 
    
- Le résumé de l’interface IUpdateNotify2 est désormais inclus.
    
### <a name="apply"></a>Appliquer

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameters

-  _displaylevel_: **true pour** afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false pour** masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour. La valeur par défaut est **False**.
    
-  _forceappshutdown_: **true** pour forcer Office applications à s’arrêter immédiatement lorsque l’action  Appliquer est déclenchée ; **false** pour échouer si des applications Office sont en cours d’exécution. La valeur par défaut est **False**. Pour [plus d’informations,](#bk_ApplyRemark) voir la remarque. 
    
  Si une Office’application est en  cours d’exécution lorsque l’action Appliquer est déclenchée, l’action  Appliquer échoue généralement. Le passage à la méthode Apply entraîne l’arrêt immédiat des applications par le `forceappshutdown=true` service  **OfficeClickToRun** et l’application de la mise à jour. L’utilisateur peut être en perte de données dans ce cas. 
    
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |L’action a été envoyée au service « Click-To-Run » pour exécution.  <br/> |
|**E_ACCESSDENIED** <br/> |L’appelant n’est pas en cours d’exécution avec des privilèges élevés.  <br/> |
|**E_INVALIDARG** <br/> |Des paramètres non valides ont été passés.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |L’action n’est pas autorisée pour le moment. Pour [plus d’informations,](#bk_ApplyRemark) voir la remarque.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Remarques

- Si une Office’application est  en cours d’exécution lorsque l’action Appliquer est déclenchée, **l’action** Appliquer échoue. La transmission à la méthode Apply entraîne l’arrêt immédiat par le `forceappshutdown=true` service  **OfficeClickToRun** de toutes les applications Office en cours d’exécution et applique la mise à jour. L’utilisateur peut faire l’expérience des données car il n’est pas invité à enregistrer les modifications apportées aux documents ouverts. 
    
- Cette action ne peut être déclenchée que lorsque l’état COM est l’un des suivants : 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si vous appelez la méthode **Apply** sans télécharger  préalablement le contenu, la méthode **Apply** indique Réussite car elle n’a détecté aucun résultat à appliquer et a terminé le **processus Appliquer** avec succès. 
    
### <a name="cancel"></a>Annuler

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|S_OK  <br/> |L’action a été envoyée au service « Click-to-Run » pour exécution.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |L’action n’est pas autorisée pour le moment. Pour plus [d’informations,](#bk_CancelRemarks) voir la section Remarques  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Remarques

- Cette méthode ne peut être déclenchée que lorsque l’ID d’état COM **eDOWNLOAD_WIP**. Il tentera d’annuler l’action de téléchargement actuelle. L’état COM change en **eDOWNLOAD_CANCELLING** et finit par **eDOWNLOAD_CANCELED**. L’état COM retourne **E_ILLEGAL_METHOD_CALL** si déclenché à tout autre moment. 
    
### <a name="download"></a>Télécharger

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameters

-  _displaylevel_: **true pour** afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false pour** masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour. La valeur par défaut est **False**.
    
-  _updatebaseurl_: URL de l’autre source de téléchargement.
    
-  _updatetoversion_: version vers Office mise à jour. Définissez ce paramètre si vous souhaitez mettre à jour une version antérieure à la version actuellement installée.
    
-  _downloadsource_: CLSID de l’implémentation **IBackgroundCopyManager** personnalisée (gestionnaire BITS). 
    
-  _contentid_: identifie le contenu à télécharger à partir du serveur de contenu via le gestionnaire BITS personnalisé. Cette valeur est transmise par le biais de l’interface BITS pour interprétation.
    
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |L’action a été envoyée au service « Click-To-Run » pour exécution.  <br/> |
|**E_ACCESSDENIED** <br/> |L’appelant n’est pas en cours d’exécution avec des privilèges élevés.  <br/> |
|**E_INVALIDARG** <br/> |Des paramètres non valides ont été passés.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |L’action n’est pas autorisée pour le moment. Pour [plus d’informations,](#bk_DownloadRemark) voir la remarque.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Remarques

- Vous devez spécifier  _downloadsource_ et  _contentid_ en tant que paire. Si ce n’est **pas le cas, la** méthode Download E_INVALIDARG erreur.  
    
- Si  _downloadsource,_  _contentid_ et  _updatebaseurl_ sont fournis,  _updatebaseurl_ sera ignoré. 
    
- Cette action ne peut être déclenchée que lorsque l’état COM est l’un des suivants : 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si vous appelez la méthode **Apply** sans contenu  téléchargé précédemment, la méthode **Apply** indique Réussite car elle n’a détecté aucun résultat à appliquer et a terminé le processus **Appliquer** avec succès. 
    
#### <a name="examples"></a>Exemples

- Pour télécharger le contenu à partir du gestionnaire BITS personnalisé : appelez la fonction **download()** en passant les paramètres suivants : 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Pour télécharger le contenu à partir de la Office réseau de distribution de contenu (CDN) : appelez la fonction **download()** sans spécifier les paramètres _downloadsource,_ _contentid_ ou _updatebaseurl._ 
    
- Pour télécharger le contenu à partir d’un emplacement personnalisé : appelez la fonction **download()** en passant le paramètre suivant : 
    
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

#### <a name="parameters"></a>Parameters

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Pointeur vers une UPDATE_STATUS_REPORT structure.  <br/> |
   
#### <a name="return-results"></a>Renvoyer des résultats

|||
|:-----|:-----|
|**S_OK** <br/> |La **méthode Status** renvoie toujours ce résultat. Examinez  `UPDATE_STATUS_RESULT` la structure pour l’état de l’action en cours.  <br/> |
   
#### <a name="remarks"></a>Remarques

- Le champ d’état du  `UPDATE_STATUS_REPORT` champ contient l’état de l’action en cours. L’une des valeurs d’état suivantes est renvoyée : 
    
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

- Si la dernière commande a entraîné une erreur, le champ d’erreur contient des informations détaillées  `UPDATE_STATUS_REPORT` sur l’erreur. Deux types de codes d’erreur sont renvoyés à partir de la **méthode Status.** 
    
- Si l’erreur est inférieure à , l’erreur est l’un des  `UPDATE_ERROR_CODE::eUNKNOWN` codes d’erreur prédéfin définis suivants :
    
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

  Si le code d’erreur de retour est supérieur au  `UPDATE_ERROR_CODE::eUNKNOWN` **HRESULT** d’un appel de fonction qui a échoué. Pour extraire la soustraction HRESULT  `UPDATE_ERROR_CODE::eUNKNOWN` de la valeur renvoyée dans le champ d’erreur du  `UPDATE_STATUS_REPORT` .
    
  La liste complète des valeurs d’état et d’erreur peut être vue en inspectant la bibliothèque de types **IUpdateNotify** incorporée dans OfficeC2RCom.dll. 
    
- Le champ contentid est utilisé  pour les appels à **l’état** une fois le téléchargement lancé et renvoie le contentid qui a été transmis à l’appel **de** téléchargement. Il est préférable d’initialiser ce champ sur **null** avant d’appeler  la méthode **Status,** puis de vérifier la valeur une fois l’état renvoyé. Si la valeur est toujours **null,** cela signifie qu’il n’y a aucun contentid à renvoyer. Si la valeur n’est pas **null,** vous devez la libérer avec un appel à **SysFreeString()**. Voici un extrait de code de la façon d’appeler **l’état** après le **téléchargement.**
    
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

À partir de la version [16.0.8208.6352], nous avons ajouté une nouvelle interface **IUpdateNotify2.** 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Cette interface a également hébergé l’interface IUpdateNotify d’origine pour assurer la compatibilité ascendante. Par conséquent, si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject.** 
    
- Nouvelles méthodes ajoutées à IUpdateNotify2 :
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList). Obtenir la liste des applications de blocage des mises à jour. Cet appel retourne l’exécution Office applications qui bloquent le processus de mise à jour de poursuivre. 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Obtenir Office de déploiement. 
    
- Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer que :
    
  - Votre version C2R est plus récente que la build ci-dessus ( \> = build de bifurcation de juin).
    
  - Utilisez UpdateNotifyObject2, au lieu de **UpdateNotifyObject** pour appeler **CoCreateInstance**.
    
Si vous n’utilisez aucune des nouvelles méthodes, vous n’avez rien à modifier. Toutes les méthodes existantes fonctionneront de la même manière qu’auparavant.
  
## <a name="implementing-the-bits-interface"></a>Mise en œuvre de l’interface BITS

Le [service BITS (Background Intelligent Transfer Service)](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) est un service fourni par Microsoft pour transférer des fichiers entre un client et un serveur. BITS est l’un des canaux Office le programme d’installation « Exécuter en un clic » peut utiliser pour télécharger du contenu. Par défaut, le programme d Microsoft 365 Apps d’installation « En un clic » utilise l’implémentation intégrée de BITS du Windows pour télécharger le contenu à partir du CDN. 
  
En fournissant une implémentation BITS personnalisée à la méthode **download()** de l’interface **IUpdateNotify,** votre logiciel de gestion peut contrôler où et comment le client télécharge le contenu. Une interface BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisé autre que les canaux intégrés « Click-to-Run » tels que les CDN, les serveurs IIS ou les partages de fichiers. 
  
La condition minimale requise pour qu’une interface BITS personnalisée fonctionne avec Office service C2R est :
  
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

- Pour les  `Addfile`  `AddFileWithRanges` fonctions, l’URL distante est au format suivant : 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits est codé en dur et signifie BITS personnalisé.
    
  -  _\<contentid\>_ est le _paramètre contentid_ de la **méthode Download().** 
    
  -  _\<relative path to target file\>_ fournit l’emplacement et le nom du fichier à télécharger. 
    
    Par exemple, si vous avez fourni un _contentid_ de la méthode Download() et que Office C2R souhaite télécharger le fichier cab version, tel que le fichier, il appelle `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **AddFile()** avec les informations suivantes `RemoteUrl` :
    
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
## <a name="automating-content-staging"></a>Automatisation de la zone de transit de contenu

Les administrateurs informatiques peuvent choisir que les clients de bureau soient activés pour recevoir automatiquement les mises à jour lorsqu’ils sont disponibles directement à partir du CDN ou ils peuvent choisir de contrôler le déploiement des mises à jour disponibles à partir des canaux de mise à jour à l’aide de l’outil déploiement Office ou de Microsoft Endpoint Configuration Manager.
  
Le service prend en charge la possibilité pour les outils de gestion de reconnaître et d’automatiser le téléchargement du contenu lorsque des mises à jour sont disponibles.
  
**L’image suivante est une vue d’ensemble du téléchargement d’une image personnalisée**

![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM Office programme d’installation « Exécuter en un clic")
  
### <a name="overview-of-downloading-a-custom-image"></a>Vue d’ensemble du téléchargement d’une image personnalisée
  
Dans le diagramme précédent, vous voyez qu’une nouvelle image Microsoft 365 Apps est disponible sur le CDN. Parallèlement à l’image Microsoft 365 Apps, une API est disponible et dispose des informations nécessaires pour permettre aux logiciels de gestion de créer directement des images personnalisées en remplaçant la nécessité d’utiliser l’outil déploiement Office.

Une entreprise configure son service WSUS pour synchroniser les mises Microsoft 365 Apps jour. Ces mises à jour ne contiennent pas la charge utile réelle de l’image, mais permettent au logiciel de gestion de reconnaître quand du nouveau contenu est disponible. Le logiciel de gestion peut ensuite lire les Microsoft 365 Apps de mise à jour pour comprendre à quelle version Office la mise à jour s’applique.

Si la mise à jour est applicable, le logiciel de gestion peut utiliser le contenu CDN et la liste de fichiers pour créer l’image personnalisée et la stocker sur l’emplacement de partage de fichiers qu’il est configuré pour utiliser.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Utilisation de l’API Microsoft 365 Apps liste de fichiers

L Microsoft 365 Apps API de liste de fichiers est utilisée pour récupérer les noms des fichiers nécessaires à une mise à jour Microsoft 365 Apps spécifique.

Requête HTTP

GET https://config.office.com/api/filelist

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Paramètres facultatifs de la requête

|**Name**|**Description**|
|:-----|:-----|
| canal <br/>| Spécifie le nom du canal  <br/> Facultatif : valeur par défaut « SemiAnnual » <br/> Valeurs pris en charge https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| version <br/>| Spécifie la version de mise à jour <br/> Facultatif : valeur par défaut de la dernière version disponible pour le canal spécifié |
| arch <br/>| Spécifie l’architecture du client <br/> Facultatif : valeur par défaut de ' x64' <br/> Valeurs prise en charge : x64, x86 |
| lid <br/>| Spécifie les fichiers de langue à inclure <br/> Facultatif : aucune valeur par défaut <br/> Pour spécifier plusieurs langues, incluez un paramètre de requête de capot pour chaque langue <br/> Utilisez le format d’identificateur de langue, par exemple. 'en-us', 'fr-fr' |
| alllanguages <br/>| Spécifie d’inclure tous les fichiers de langue <br/> Facultatif : valeurs par défaut sur false |

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.

Pour créer une image, suivez les étapes suivantes :
1.  Appelez l’API, en fournissant les paramètres de requête appropriés pour le canal, la version et l’architecture de la mise à jour qui vous intéresse.
Remarque : les objets de fichier avec l’attribut « lcid » : « 0 » sont des fichiers linguistiquement neutres et doivent être inclus dans l’image.
2.  Créez une image locale du CDN en itérant les objets de fichier et en copiant les fichiers CDN, tout en créant la structure de dossiers spécifiée par l’attribut « relativePath » défini pour chacun des objets de fichier.

L’exemple suivant récupère la liste des fichiers pour le canal actuel et la version 16.0.4229.1004 pour 64 bits et inclut les fichiers en français et en anglais :

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Vérification de hachage des fichiers .dat

Les outils de création d’images peuvent vérifier l’intégrité des fichiers .dat téléchargés en comparant une valeur de hachage calculée à la valeur de hachage fournie associée à chacun des fichiers .dat. Voici un exemple d’objet fichier qui spécifie les valeurs hashLocation et hashAlgorithm :
  
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

- **L’attribut hashLocation** spécifie l’emplacement du chemin d’accès relatif .cab fichier contenant la valeur de hachage. Construisez l’emplacement du fichier de hachage en concatenant l’URL + relativePath + hashLocation. Dans l’exemple suivant, l stream.x64.bg-bg.hash serait : 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- **L’attribut hashAlgorithm** spécifie l’algorithme de hachage utilisé. 
    
  Pour valider l’intégrité du fichier stream.x64.bg-bg.dat, ouvrez le fichier stream.x64.bg-bg.hash et lisez la valeur HASH qui est la première ligne de texte du fichier de hachage. Comparez cette valeur à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier .dat téléchargé.
    
  L’exemple suivant montre comment C# code pour lire le hachage.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Microsoft 365 Apps Mises à jour

Toutes Microsoft 365 Apps mises à jour sont publiées dans le [catalogue Microsoft Update.](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)
  
Microsoft 365 Apps Les mises à jour permettent aux logiciels de gestion de traiter Microsoft 365 Apps mises à jour d’une manière très similaire à toute autre mise à jour WU, à une exception près . les mises à jour du client ne contiennent pas de charge utile réelle. Les mises à jour Microsoft 365 Apps ne doivent pas être installées sur les clients, mais plutôt utilisées pour déclencher les flux de travail avec le logiciel de gestion remplaçant la commande d’installation par le mécanisme d’installation COM indiqué ci-dessus.

**La figure suivante montre un diagramme du flux de travail Office 365 de mise à jour du client.**

![Diagramme de flux de travail pour les mises à jour du client O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")
  
Chaque Microsoft 365 Apps mise à jour publiée inclut des métadonnées sur la mise à jour. Ces métadonnées incluent un paramètre appelé MoreInfoUrl qui peut être utilisé pour dériver l’appel d’API à l’API de liste de fichiers pour cette mise à jour spécifique.

Dans l’exemple suivant, l’API de liste de fichiers est incorporée dans moreInfoURL et commence par « ServicePath= »

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Métadonnées supplémentaires pour l’automatisation de la zone de transit de contenu

**API d’historique des sorties**
  
L Microsoft 365 Apps’API d’historique des mises à jour est utilisée pour récupérer les détails de chacune des mises à jour publiées sur le CDN avec les noms de canaux et d’autres attributs de canal.

Requête HTTP

```http
GET https://config.office.com/api/filelist/channels 
```

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.

**SKUs API**
  
L’API SSK retourne des informations utiles pour déterminer les produits disponibles pour le déploiement et la maintenance à partir du Office CDN avec différentes options pour chacun d’eux.

Requête HTTP

```http
GET https://config.office.com/api/filelist/skus 
```

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.
