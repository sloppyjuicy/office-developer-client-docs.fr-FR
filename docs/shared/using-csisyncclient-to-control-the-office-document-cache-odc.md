---
title: Utilisation de CSISyncClient pour contrôler le Cache de documents Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Découvrez comment utiliser CSISyncClient pour contrôler le Cache de documents Office (ODC).
ms.openlocfilehash: 908442bdc4e02f8268b9af877921da45a64ab197
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565283"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Utilisation de CSISyncClient pour contrôler le Cache de documents Office (ODC)

Découvrez comment utiliser CSISyncClient pour contrôler le Cache de documents Office (ODC).
  
CSISyncClient est un serveur COM out-of-process (CsiSyncClient.exe) qui permet à Microsoft OneDrive contrôler le comportement de la Cache de documents Office (ODC). Par exemple, OneDrive peut-être faire appel à la ODC via CSISyncClient pour télécharger des fichiers vers et depuis les systèmes d’extrémité MS-FSSHTTP est activé. Cela permet de garantie service fonctionnalités avancées dans Office, telles que les transitions de co-création et transparentes d’en mode hors connexion à en ligne.
  
CsiSyncClient est disponible dans Office Desktop (x86 et x64). Remarque : Alors que les nouvelles versions d’Office peuvent livrées avec CsiSyncClient, le processus sera utilisé pour la compatibilité descendante uniquement. L’interface CsiSyncClient et la méthodologie de contrôler le ODC seront modifié dans les futures versions de Microsoft Office.
  
L’identificateur de classe est actuellement définie pour répondre uniquement à OneDrive.
  
L’objet COM est utilisable comme serveur COM out-of-proc et s’exécute dans CsiSyncClient.exe. En raison de limitations avec Access (qui le ODC utilise), il est fourni avec le type de bit Office est fourni dans ce x64 Office signifie un x64 objet COM ou x86 Office signifie un x86 objet COM. Pour contourner cette limitation, spécification CLSCTX_LOCAL_SERVER comme partie de l’interface CoCreateInstance aura l’objet COM être hébergé en tant qu’un serveur COM out-of-process, autoriser la compatibilité cross-nombre de bits.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient utilise les interfaces suivantes.
  
### <a name="interface-ilsclocalsyncclient"></a>Interface ILSCLocalSyncClient

Il s’agit de l’interface principale utilisée pour synchroniser des fichiers dans Office.
  
- ProgID : Office.LocalSyncClient
- CLSID : {14286318-B6CF-49a1-81FC-D74AD94902F9}
- Bibliothèque de types : {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
L’objet COM qui est exposé est utilisé comme un serveur out-of-Process. Spécification CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet de compatibilité entre les processus 32 bits et 64 bits.
  
Une fois que vous avez créé conjointement l’objet COM, vous devez d’abord appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . Une fois que [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) est terminée, vous pouvez appeler n’importe quelle API aussi souvent que vous le souhaitez et dans n’importe quel ordre. Vous pouvez également appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela n’a aucun effet. 
  
Les exceptions pour le paragraphe précédent sont [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Une fois que vous appelez [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l’objet COM, vous devez détruire cet objet et créer un nouveau. [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprimer votre subcache, supprimez toutes les informations de fichier associé dans le cache, mais laissez les documents sur le disque. Il également conserve l’état pour communiquer avec le cache. Cela vous permet d’appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) à nouveau pour créer un nouveau cache sans devoir supprimer et recréer l’objet COM. 
  
**Fonctions membres publics**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::DeleteFile

DeleteFile est utilisée pour supprimer les informations du fichier à partir du cache. Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
Chaîne qui identifie le ResourceID du fichier. Cette valeur doit être vide avec un maximum de 128 caractères. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Le ResourceID donné n’est pas dans le cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize n’a pas été correctement appelé dans le passé.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier est en cours de synchronisation ou ouvrir et ne peut pas être supprimée.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges retourne un énumérateur des objets ILSCEvent et retourne également un jeton qui est donné à l’appel suivant à GetChanges, en supposant que le consommateur a traité l’ensemble d’événements précédent. Événements avant le _nPreviousChangesToken_ spécifié seront supprimés et non disponible. S’il n’y a aucun événement à traiter, _pnCurrentChangesToken_ doit être la même valeur que _nPreviousChangesToken_, mais _ppiEvents_ sera toujours définie. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Paramètres

 _nPreviousChangesToken_
  
Identifie l’événement qui a été traitée en dernier par le consommateur. 
  
 _pnCurrentChangesToken_
  
Identifie l’événement le plus récent est transmise au consommateur. Ne doit pas être null.
  
 _ppiEvents_
  
Énumérateur pour les événements remis au consommateur. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission est utilisée pour interroger si heuristique synchronisation du bureau pour réseau coût et consommation d’énergie sont remplacées. Sur un 3G ou un autre réseau coûteuses, ou lors de l’exécution sur la batterie et branché, Office peut choisir de bloquer le trafic réseau jusqu'à un moment plus opportun.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Paramètres

 _nspType_
  
Indicateur qui définit le heuristique de coût de requête. Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Spécifie si l’heuristique coût demandé est actuellement remplacé ou non. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique : si elle existe dans le cache, si elle est en attente de la communication avec la copie sur le serveur, et si Office 2013 possède le plus jusqu'à les données de date de la copie locale. Il nécessite un indicateur de bits des valeurs [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations de l’objet COM CsiSyncClient consiste à interroger. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
Chaîne qui identifie le fichier sur le client. Cette valeur doit être vide, avec un maximum de 128 caractères. 
  
 _sfRequestedStatus_
  
Indicateur qui définit les informations à retourner. Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
Chaîne qui identifie l’emplacement du fichier identifié par _bstrResourceID_ sur le client. Ne doit pas être null. 
  
 _pbstrETag_
  
Chaîne qui contient l’eTag pour le fichier identifié par _bstrResourceID_. Ne doit pas être null. 
  
 _psfFileStatus_
  
Indicateur qui contiendra le statut demandé par le biais de _sfRequestedStatus_ pour le fichier identifié par _bstrResourceID_. Ne doit pas être null. Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Les informations du fichier spécifiées par _bstrResourceID_ n’existent pas dans le cache.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged a été demandé, ou le fichier spécifié par _bstrResourceID_ est verrouillé ou manquant.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions renvoie une liste délimitée par des canaux des extensions de fichiers qui sont actuellement pris en charge par l’objet COM CsiSyncClient. Notez que cette liste peut modifier et le consommateur serez ainsi averti d’une modification par le biais de l’objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured). 
  
Un exemple de la chaîne renvoyée se présente comme suit : « | docx | docm | pptx | »
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Paramètres

 _pbstrSupportedFileExtensions_
  
Chaîne à définir avec un ensemble d’extensions de fichiers pris en charge par l’objet COM CsiSyncClient délimité par canal. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize doit être la première méthode appelée. Dans le cas contraire, toutes les autres API renverra E_LSC_NOTINITIALIZED. L’appel de Initialize sur un objet déjà initialisé renvoie S_OK et n’a aucun effet. Si E_LSC_CACHEMISMATCH est renvoyée, l’appelant peut appeler [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé à le SuppliedID donné. Toutefois, dans ce cas autres API retournera encore E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Paramètres

 _bstrSuppliedID_
  
Identifie le consommateur et qui mettent en cache à utiliser. Doit être vide avec un maximum de 32 caractères. 
  
 _bstrProgID_
  
Identifie un objet COM de la consommation de communication bidirectionnelle. Doit être vide avec un maximum de 39 caractères. Voir [ \<ProgID\> clé](https://docs.microsoft.com/en-us/windows/desktop/com/-progid--key) pour plus d’informations sur le ProgID. 
  
 _bstrFileSystemDirectoryHint_
  
Identifie la racine du répertoire dans lequel seront stockés les fichiers locaux. Doit être vide avec un maximum de 256 caractères. Le répertoire doit déjà exister. 
  
 _pEventCallback_
  
L’interface de rappel qui avertit CsiSyncClient sur les modifications. Voir IPartnerActivityCallback::EventOccurred. Cette valeur ne doit pas être nulle. 
  
 _pfCreatedNewCache_
  
Renvoie si un nouveau cache a été créé. Si le cache n’est associé à la SuppliedID, un sera créé. Cette valeur ne doit pas être nulle.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Un SuppliedID déjà possède un cache qui lui est associé, mais dispose d’un ProgId ou FileSystemDirectoryHint différentes de celles qui sont fournies.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |Le FileSystemDirectoryHint (ou un sous-dossier) existe déjà sur un cache différent.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |Le ProgID existe déjà sur un cache différent.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange est utilisée pour indiquer à l’objet COM CsiSyncClient pour essayer de télécharger le fichier spécifié. La méthode prépare le fichier à télécharger, y compris le contenu du fichier en cours de lecture. Si un téléchargement est déjà en attente, téléchargement précédent sera ignoré et le nouveau contenu préparé pour télécharger. Si le fichier est ouvert pour modification dans une application, cette méthode renvoie S_OK sans préparer le fichier de téléchargement (l’application doit déjà effectuer cette étape si des modifications sont apportées).
  
Cette méthode permet volumineux s’il a été marqué comme télécharge bloqués précédemment (voir [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _bstrFileSystemPath_
  
Une chaîne qui identifie le fichier sur le client. Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères. Ce chemin d’accès doit être dans l’arborescence du répertoire spécifié par le FileSystemDirectoryHint lors de l’appel à [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué. 
  
 _bstrResourceID_
  
Une chaîne qui identifie le ResourceID du fichier. Cette valeur doit être vide avec un maximum de 128 caractères. 
  
 _bstrWebPath_
  
Une chaîne qui identifie le fichier sur le serveur. Cette valeur doit être URL non vide et valide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ a un autre ResourceID celui spécifié. Un événement de type LSCEventType_OnFilePathConflict est envoyée lorsque cette erreur est renvoyée. Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Le fichier a été supprimée opération intermédiaire.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |L’extension de fichier donné n’est pas pris en charge par l’objet COM CsiSyncClient. Voir [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |L’objet COM n’avez pas prévu un téléchargement parce que le fichier dans le cache a des modifications les plus récentes à partir du disque.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ est manquant ou verrouillé.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié déjà en attente de modification dans un cache différent et ne peut pas encore être associé au cache du consommateur.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Le WebPath fourni se situe sous un cache différent.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile associe une nouvelle URL et le chemin d’accès local pour un ResourceID donné. Si le fichier spécifié par le ResourceID n’existe pas déjà dans le cache, une tentative seront créer et marquer pour téléchargement.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
Une chaîne qui identifie le ResourceID du fichier. Cette valeur doit être vide avec un maximum de 128 caractères. 
  
 _bstrNewFileSystemPath_
  
Chaîne qui spécifie le nouveau chemin d’accès local pour le fichier. Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères. Ce chemin d’accès doit être dans l’arborescence spécifiée par le FileSystemDirectoryHint lors de l’appel à initialiser. 
  
 _bstrNewWebPath_
  
Chaîne qui spécifie la nouvelle URL pour le fichier. Cette valeur doit être non vides URL valide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427. 
  
 _fBlockUploads_
  
Spécifie si les téléchargements vers le nouvel emplacement sont actuellement autorisées. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Le _bstrNewFileSystemPath_ ou _bstrNewWebPath_ existent déjà sur un autre fichier dans n’importe quel cache. Un événement de type LSCEventType_OnFilePathConflict est envoyée lorsque cette erreur est renvoyée. Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Les informations du fichier a été supprimées du cache pendant l’exécution de cette méthode.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié est en cours de synchronisation dans une application Office.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache supprime le cache associé à le SuppliedID qui a été fournie dans Initialize. Cela inclut toutes les informations sur les fichier, mais laisse les fichiers sur le client et le serveur. Cette méthode rend également l’objet dans un état partiellement non initialisé. Les appels valides uniquement après ce sont [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Cette méthode peut être appelée si Initialize échoue et renvoie E_LSC_CACHEMISMATCH et supprime le cache associé à le SuppliedID qui a été fournie avec l’appel défectueux.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Paramètres

Aucune
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange indique à l’objet COM CsiSyncClient pour marquer le fichier spécifié pour le téléchargement. Si le fichier est ouvert dans une application Office pour modifier, cette méthode renvoie S_OK sans marquage du fichier de téléchargement (l’application doit déjà effectuer cette étape si des modifications sont apportées).
  
Cette méthode permet téléchargements si elle a été marquée comme téléchargements bloqués précédemment (voir RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Une chaîne qui identifie le fichier sur le client. Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères. Ce chemin d’accès doit être dans l’arborescence spécifiée par le FileSystemDirectoryHint lors de l’appel à initialiser.  <br/> |
|bstrResourceID  <br/> |Une chaîne qui identifie le ResourceID du fichier. Cette valeur doit être vide avec un maximum de 128 caractères.  <br/> |
|bstrWebPath  <br/> |Une chaîne qui identifie le fichier sur le serveur. Cette valeur doit être une URL valide non vide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec pour définir l’état de la connectivité du cache.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ a un autre ResourceID celui spécifié.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |L’extension de fichier donné n’est pas pris en charge par l’objet COM CsiSyncClient. Voir GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Le fichier a été supprimé dans une opération intermédiaire.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié a des modifications en attente dans un cache différent déjà et ne peut pas encore être associé au cache du consommateur.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Le WebPath fourni se situe sous un cache différent.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Définit le cache dans un état en ligne ou hors connexion. Si elle est en mode hors connexion, Office tentera pas à communiquer avec le serveur pour tous les fichiers dans ce cache, quel que soit le paramètre de _fBlockUploads_ de chaque fichier. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Paramètres

 _fIsOnline_
  
Valeur de type boolean détermination de l’état de la connectivité du cache. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec pour définir l’état de la connectivité du cache.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission est utilisé pour substituer ou heuristique de synchronisation de restoreOffice pour réseau d’utilisation de coûts et d’alimentation. Sur un 3G ou un autre réseau coûteuses, ou lors de l’exécution sur la batterie et branché, Office peut choisir de bloquer le trafic réseau jusqu'à un moment plus opportun. Le consommateur de cette API pouvez l’utiliser pour remplacer heuristique d’Office et de forcer la synchronisation ait lieu.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Paramètres

 _nspType_
  
Indicateur qui définit le heuristique coût à remplacer. Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Spécifie s’il faut forcer la synchronisation, remplaçant ainsi que heuristique coût, ou remplacer n’est plus. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de la synchronisation heuristique de remplacer.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Décharge le cache de l’objet COM et effectuer des opérations de fermeture. [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelée avant la destruction de l’objet COM. Une fois appelée, aucune autre API ne peut être appelé, l’objet COM doit être détruit et créer une nouvelle si vous souhaitez continuer d’opérations. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Paramètres

Aucun.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec d’annuler l’initialisation.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interface IEnumLSCEvent

Cette interface représente une liste d’événements ILSCEvent.
  
**Fonctions membres publics**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Récupère l’événement suivant à partir de la liste des événements.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Paramètres

 _ppiLSCEvent_
  
Pointeur vers une interface ILSCEvent.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Il existe plus d’événements.  <br/> |
|S_OK  <br/> |L’appel a réussi.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Réinitialise l’énumérateur au premier événement.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Paramètres

Aucun.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
### <a name="interface-ilscevent"></a>Interface ILSCEvent

Cette interface représente un événement de synchronisation. Toutes les informations relatives à l’événement peuvent être récupérées à partir de l’interface.
  
**Fonctions membres publics**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Notez que cette valeur est renseignée lorsque [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, pas lorsque l’événement a été créé, vous devrez uniquement l’état actuel du fichier, pas l’état du fichier lors de la modification de l’état de conflit. 
  
Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Paramètres

 _pfIsInConflict_
  
L’état actuel de conflit du fichier associé à l’événement.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Paramètres

 _pnError_
  
L’erreur associée à cet événement.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Paramètres

 _pbstrETag_
  
L’ETag associé à cet événement
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Obtient le type de cet événement.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Paramètres

 _pnEventType_
  
Le type d’événement de cet événement. Voir [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs valides. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|S_OK  <br/> |L’appel a réussi.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Obtient le chemin d’accès local de travail de cet événement.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Paramètres

 _pbstrLocalWorkingPath_
  
Le chemin d’accès local du fichier à laquelle cet événement se rapporte. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Obtient l’ID de ressource pour l’événement.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _pbstrResourceID_
  
ResourceID du fichier associé à cet événement.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict. Lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque un conflit de chemin d’accès Web ou le chemin d’accès Local avec un autre fichier dans le cache des fichiers Office, cela événement est généré. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Paramètres

 _pbstrResourceIDAttempted_
  
ResourceID qui a provoqué cet événement sont générés. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Paramètres

 _pnSyncErrorType_
  
Le type d’erreur associé à cet événement. Voir [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs possibles. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|S_OK  <br/> |L’appel a réussi.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Paramètres

 _pbstrWebPath_
  
Spécifie le chemin d’accès Web associé à cet événement. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
### <a name="interface-ilscevent2"></a>Interface ILSCEvent2

Cette interface conserve des informations supplémentaires sur un événement de synchronisation.
  
**Fonctions membres publics**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Obtient les informations de la chaîne d’erreur sur un événement de synchronisation.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Paramètres

 _pbstrErrorChain_
  
Une chaîne contenant les informations de la chaîne d’erreur. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_NOTIMPL  <br/> |La version d’Office installée ne prend pas en charge cette interface  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs des valeurs de paramètre ne sont pas valides.  <br/> |
|E_FAIL  <br/> |Les informations de la chaîne d’erreur ne sont pas disponibles.  <br/> |
|S_OK  <br/> |L’appel a réussi.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interface IPartnerActivityCallback

Cette interface fournit une fonction de rappel à l’objet COM CSISyncClient.
  
**Fonctions membres publics**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Il s’agit d’une fonction de rappel sur l’objet donné à l’objet COM CsiSyncClient. Il est prévu que lorsqu’un événement se produit (voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour des types d’événement valide), l’objet COM CsiSyncClient appeler cette méthode, le consommateur de signalisation. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Paramètres

 _eEventTypeOccurred_
  
Le type d’événement de cet événement. Voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les valeurs valides. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK.
  
## <a name="enumerations"></a>Énumérations

CSISyncClient utilise les énumérations suivantes.
  
### <a name="enum-lsceventsyncerrortype"></a>Énumération LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Cette énumération spécifie les catégories d’erreurs qui peuvent se produire lors de la synchronisation d’un fichier.
  
|Énumérateur|Description|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |L’erreur de synchronisation de cet événement était inattendu et peut nécessiter une attention particulière. Par défaut, l’utilisateur peut avoir à intervenir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |L’erreur de synchronisation de cet événement ne doit pas une attention particulière. Office il gère automatiquement.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |L’erreur de synchronisation de cet événement requiert un utilisateur pour le résoudre. Par exemple, erreur de conflit de fusion requiert un utilisateur ouvrir le document et les fusionner.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |L’erreur de synchronisation de cet événement requiert le consommateur intervenir, mais ne nécessitent ne pas une attention particulière par l’utilisateur.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |L’erreur de synchronisation de cet événement requiert le consommateur intervenir comme un cas spécial.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Énumération LSCEventType
<a name="Enum_LSCEventType"> </a>

Cette énumération spécifie le type d’événements qui peut se produire pour un fichier particulier.
  
|Énumérateur|Description|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Modifications apportées à un fichier local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Un utilisateur ouvre un fichier.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Terminé le téléchargement des modifications de fichiers à partir du serveur.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Terminé le téléchargement des modifications de fichier sur le serveur.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |L’état de conflit de fusion d’un fichier a changé.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Un fichier a été ajouté.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Un fichier a été supprimé.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Synchronisation a été activée pour les fichiers d’un utilisateur.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Démarrer le téléchargement des modifications de fichiers à partir du serveur.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Démarrer le téléchargement des modifications de fichier sur le serveur.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Cet événement est généré lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque un conflit de chemin d’accès Web ou le chemin d’accès Local avec un autre fichier dans le Cache de fichiers Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Énumération LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Cette énumération spécifie le type des événements qui peuvent se produire. Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d’événement.
  
|Énumérateur|Description|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Un ILSCEvent s’est produite. Le consommateur doit appeler [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour extraire les données.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Les extensions de fichier prises en charge ont été modifiées. Le consommateur doit appeler [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions prises en charge.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Énumération LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Cette énumération spécifie les indicateurs utilisés pour une heuristique de coût du réseau. 

|Énumérateur|Description|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True si l’heuristique coût pour les réseaux coûteux (par exemple, 3 G) est remplacé.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True si l’heuristique coût consommation d’énergie (par exemple, une batterie) est remplacé.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Énumération LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Cette énumération est utilisée pour représenter l’état de synchronisation d’un fichier. 
  
|Énumérateur|Description|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True si les données à envoyer au fichier du serveur en attente.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True si les données à télécharger à partir du fichier de serveur en attente.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True si les données Office sur le fichier dans son cache est la plus récente copie des données sur le disque.  <br/> |
   

