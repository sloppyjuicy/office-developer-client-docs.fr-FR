---
title: Utilisation de CSISyncClient pour contrôler le cache de documents Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Découvrez comment utiliser CSISyncClient pour contrôler le cache de documents Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346255"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Utilisation de CSISyncClient pour contrôler le cache de documents Office (ODC)

Découvrez comment utiliser CSISyncClient pour contrôler le cache de documents Office (ODC).
  
CSISyncClient est un serveur COM out-of-proc (CsiSyncClient. exe) qui permet à Microsoft OneDrive de contrôler le comportement du cache de documents Office (ODC). Par exemple, OneDrive peut appeler le ODC via CSISyncClient pour télécharger et télécharger des fichiers vers et à partir de points de terminaison compatibles avec MS FSSHTTP. Cela permet d'activer les fonctionnalités avancées de service dans Office, telles que la co-création et les transitions transparentes de Offline vers Online.
  
CsiSyncClient est disponible dans Office Desktop (x86 et x64). Remarque: tandis que les versions plus récentes d'Office peuvent être livrées avec CsiSyncClient, le processus sera utilisé uniquement à des fins de compatibilité descendante. L'interface CsiSyncClient et la méthodologie de contrôle du ODC seront modifiées dans les versions ultérieures d'Office.
  
L'ID de classe est actuellement défini pour répondre uniquement à OneDrive.
  
L'objet COM est utilisable comme un serveur COM out-of-proc et s'exécute dans CsiSyncClient. exe. En raison des limites liées à Access (que le service ODC utilise), il est fourni avec le type de bit qu'il contient, c'est pourquoi x64 Office signifie un objet COM x64, ou x86 Office signifie un objet COM x86. Pour contourner cette limitation, la spécification de CLSCTX_LOCAL_SERVER dans le cadre de la fonction CoCreateInstance aura pour objet COM d'être hébergé en tant que serveur COM out-of-proc, ce qui permet la compatibilité entre les bits par tour.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient utilise les interfaces suivantes.
  
### <a name="interface-ilsclocalsyncclient"></a>Interface ILSCLocalSyncClient

Il s'agit de l'interface principale utilisée pour synchroniser les fichiers dans Office.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49A1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
L'objet COM qui est exposé est utilisé en tant que serveur out-of-proc. La spécification de CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet la compatibilité entre les processus 64 bits et 32 bits.
  
Une fois que vous avez co-créé l'objet COM, vous devez appeler [d'abord ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . Une fois [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) s'est terminé avec succès, vous pouvez appeler n'importe quelle API autant de fois que vous le souhaitez et dans n'importe quel ordre. Vous pouvez également appeler [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela n'a aucun effet. 
  
Les exceptions au paragraphe précédent sont [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Une fois que vous avez appelé [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l'objet com, vous devez détruire cet objet et en créer un nouveau. [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprimera votre sous-cache, supprimez toutes les informations de fichier associées dans le cache, mais laissez les documents sur le disque. Il laisse également l'état intact pour la communication avec le cache. Cela vous permet d'appeler [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) à nouveau pour créer un nouveau cache sans avoir à détruire et recréer l'objet com. 
  
**Fonctions membres publiques**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile est utilisé pour supprimer les informations de fichier du cache. Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
La chaîne qui identifie le ResourceID du fichier. Cette valeur ne doit pas être vide, avec un maximum de 128 caractères. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Le ResourceID donné n'est pas dans le cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize n'a pas été appelé avec succès dans le passé.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier est en cours de synchronisation ou d'ouverture et ne peut pas être supprimé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient:: GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges renvoie un énumérateur d'objets ILSCEvent et renvoie également un jeton qui est attribué à l'appel suivant à GetChanges, en supposant que le consommateur a traité le jeu d'événements précédent. Les événements précédant le _nPreviousChangesToken_ spécifié seront supprimés et indisponibles. S'il n'y a aucun événement à traiter, _pnCurrentChangesToken_ doit avoir la même valeur que _NPreviousChangesToken_, mais _ppiEvents_ continuera à être défini. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Paramètres

 _nPreviousChangesToken_
  
Identifie l'événement qui a été traité en dernier par le consommateur. 
  
 _pnCurrentChangesToken_
  
Identifie l'événement le plus récent transmis au consommateur. Ne doit pas être null.
  
 _ppiEvents_
  
Un énumérateur pour les événements transmis au consommateur. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: GetClientNetworkSyncPermission

GetClientNetworkSyncPermission est utilisé pour demander si les heuristiques de synchronisation d'Office pour le coût réseau et la consommation d'énergie sont remplacées. Lorsqu'il est connecté à un réseau 3G ou à un autre réseau à coût élevé, ou lorsqu'il fonctionne sur batterie ou qu'il est branché, Office peut choisir de bloquer le trafic réseau jusqu'à un temps plus opportun.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Paramètres

 _nspType_
  
Indicateur qui définit le coût heuristique à interroger. Voir [énumérAtion LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Indique si la heuristique de coût demandée est actuellement remplacée ou non. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient:: GetFileStatus

GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique: s'il existe dans le cache, s'il est en attente de communication avec la copie du serveur et si Office 2013 a les données les plus à jour à partir de la copie locale. Elle requiert un indicateur de bits des valeurs d' [énumérAtion LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations pour lesquelles l'objet com CsiSyncClient doit effectuer une requête. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
La chaîne qui identifie le fichier sur le client. Cette valeur ne doit pas être vide, avec un maximum de 128 caractères. 
  
 _sfRequestedStatus_
  
Indicateur qui définit les informations à renvoyer. Voir [énumérAtion LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
La chaîne qui identifie l'emplacement du fichier identifié par _bstrResourceID_ sur le client. Ne doit pas être null. 
  
 _pbstrETag_
  
Chaîne qui contient l'eTag pour le fichier identifié par _bstrResourceID_. Ne doit pas être null. 
  
 _psfFileStatus_
  
Indicateur qui contiendra l'État demandé via _sfRequestedStatus_ pour le fichier identifié par _bstrResourceID_. Ne doit pas être null. Voir [énumérAtion LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Les informations de fichier spécifiées par _bstrResourceID_ n'existent pas dans le cache.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged a été demandé ou le fichier spécifié par _bstrResourceID_ est verrouillé ou manquant.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient:: GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions renvoie une liste d'extensions de fichiers délimitées par des canaux qui sont actuellement prises en charge par l'objet COM CsiSyncClient. Notez que cette liste peut changer et que le consommateur est informé d'une modification via l'objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured). 
  
Un exemple de la chaîne renvoyée est le suivant: "| docx | docm | pptx |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Paramètres

 _pbstrSupportedFileExtensions_
  
Chaîne à définir avec un jeu d'extensions de fichiers délimité par des canaux et pris en charge par l'objet COM CsiSyncClient. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient:: Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize doit être la première méthode appelée. Dans le cas contraire, toutes les autres API retournent E_LSC_NOTINITIALIZED. L'appel de la méthode Initialize sur un objet déjà initialisé renvoie S_OK et ne fait rien. Si E_LSC_CACHEMISMATCH est renvoyé, l'appelant peut appeler [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé au SuppliedID donné. Toutefois, dans ce cas, d'autres API continuent de renvoyer E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Paramètres

 _bstrSuppliedID_
  
Identifie le consommateur et le cache à utiliser. Doit être vide avec un maximum de 32 caractères. 
  
 _bstrProgID_
  
Identifie l'objet COM du consommateur pour la communication bidirectionnelle. Doit être vide avec un maximum de 39 caractères. Pour plus d'informations sur les ProgID, voir [ \<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) . 
  
 _bstrFileSystemDirectoryHint_
  
Identifie la racine du répertoire dans lequel les fichiers locaux seront stockés. Doit être vide avec un maximum de 256 caractères. Le répertoire doit déjà exister. 
  
 _pEventCallback_
  
Interface de rappel que CsiSyncClient enverra sur les modifications. Voir IPartnerActivityCallback:: EventOccurred. Cette valeur ne doit pas être null. 
  
 _pfCreatedNewCache_
  
Indique si un nouveau cache a été créé. Si aucun cache n'est associé au SuppliedID, un cache est créé. Cette valeur ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Un SuppliedID est déjà associé à un cache, mais a un ProgId ou FileSystemDirectoryHint différent de ceux fournis.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |Le FileSystemDirectoryHint (ou un sous-dossier) existe déjà dans un autre cache.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |Le ProgID existe déjà dans un autre cache.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient:: LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange est utilisé pour indiquer à l'objet COM CsiSyncClient de tenter de télécharger le fichier spécifié. La méthode prépare le chargement du fichier, y compris la lecture du contenu actuel du fichier. Si un chargement est déjà en attente, le téléchargement précédent est ignoré et le nouveau contenu préparé pour le chargement. Si le fichier est ouvert pour modification dans une application, cette méthode renvoie S_OK sans préparer le fichier pour le chargement (l'application doit déjà effectuer cette étape s'il y a des modifications).
  
Cette méthode autorisera les téléchargements s'il a été marqué comme étant des téléchargements bloqués précédemment (voir [ILSCLocalSyncClient:: RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _bstrFileSystemPath_
  
Chaîne qui identifie le fichier sur le client. Cette valeur doit être un chemin d'accès local non vide avec un maximum de 256 caractères. Ce chemin d'accès doit se trouver dans l'arborescence de répertoires spécifiée par l'FileSystemDirectoryHint lorsque l'appel à [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué. 
  
 _bstrResourceID_
  
Chaîne qui identifie le ResourceID du fichier. Cette valeur ne doit pas être vide, avec un maximum de 128 caractères. 
  
 _bstrWebPath_
  
Chaîne qui identifie le fichier sur le serveur. Cette valeur doit être une URL non vide, valide, mais ne dépassant pas INTERNET_MAX_URL_LENGTH, comme défini https://support.microsoft.com/kb/208427par. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ a un ResourceId différent de celui spécifié. Un événement de type LSCEventType_OnFilePathConflict est envoyé lorsque cette erreur est renvoyée. Voir [ILSCLocalSyncClient:: GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Le fichier a été supprimé au milieu des opérations.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |L'extension de fichier donnée n'est pas prise en charge par l'objet COM CsiSyncClient. Voir [ILSCLocalSyncClient:: GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |L'objet COM n'a pas planifié de téléchargement, car le fichier dans le cache avait les modifications les plus récentes à partir du disque.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ est manquant ou verrouillé.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Le FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifié par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Le fichier spécifié par _bstrResourceID_ a une FileSystemPath différente de celle spécifiée.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Le chemin d'accès webPath fourni se trouve dans un autre cache.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient:: RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile associe une nouvelle URL et le chemin d'accès local d'un ResourceID donné. Si le fichier spécifié par le ResourceID n'existe pas déjà dans le cache, une tentative est effectuée pour le créer et le marquer pour téléchargement.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
Chaîne qui identifie le ResourceID du fichier. Cette valeur ne doit pas être vide, avec un maximum de 128 caractères. 
  
 _bstrNewFileSystemPath_
  
Valeur de type String qui spécifie le nouveau chemin d'accès local du fichier. Cette valeur doit être un chemin d'accès local non vide avec un maximum de 256 caractères. Ce chemin d'accès doit se trouver dans l'arborescence de répertoires spécifiée par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué. 
  
 _bstrNewWebPath_
  
Valeur de type String qui spécifie la nouvelle URL du fichier. Cette valeur doit être une URL valide non vide, mais pas plus de INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427. 
  
 _fBlockUploads_
  
Indique si les téléchargements vers le nouvel emplacement sont autorisés actuellement. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Le _bstrNewFileSystemPath_ ou _bstrNewWebPath_ existe déjà dans un autre fichier dans n'importe quel cache. Un événement de type LSCEventType_OnFilePathConflict est envoyé lorsque cette erreur est renvoyée. Voir [ILSCLocalSyncClient:: GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Les informations de fichier ont été supprimées du cache pendant l'exécution de cette méthode.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Le FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifié par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié est en cours de synchronisation dans une application Office.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient:: ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache supprime le cache associé au SuppliedID qui a été fourni lors de l'initialisation. Cela inclut toutes les informations du fichier, mais laisse les fichiers sur le client et le serveur. Cette méthode laisse également l'objet dans un état partiellement non initialisé. Les seuls appels valides une fois qu'il s'agit de [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Cette méthode peut être appelée si Initialize échoue et renvoie E_LSC_CACHEMISMATCH, et supprime le cache associé au SuppliedID fourni avec l'appel qui a échoué.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Paramètres

Aucun
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé correctement dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient:: ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange indique à l'objet COM CsiSyncClient de marquer le fichier spécifié pour le téléchargement. Si le fichier est ouvert dans une application Office pour modification, cette méthode renvoie S_OK sans marquer le fichier pour téléchargement (l'application doit déjà effectuer cette étape s'il y a des modifications).
  
Cette méthode autorise les téléchargements si elle a été marquée comme téléchargements bloqués précédemment (voir RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

|Parameter|Description|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Chaîne qui identifie le fichier sur le client. Cette valeur doit être un chemin d'accès local non vide avec un maximum de 256 caractères. Ce chemin d'accès doit se trouver dans l'arborescence de répertoires spécifiée par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.  <br/> |
|bstrResourceID  <br/> |Chaîne qui identifie le ResourceID du fichier. Cette valeur ne doit pas être vide, avec un maximum de 128 caractères.  <br/> |
|bstrWebPath  <br/> |Chaîne qui identifie le fichier sur le serveur. Cette valeur doit être une URL valide non vide, mais pas plus de INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de la définition de l'état de connectivité du cache.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ a un ResourceId différent de celui spécifié.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |L'extension de fichier donnée n'est pas prise en charge par l'objet COM CsiSyncClient. Voir GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Le fichier a été supprimé au milieu de l'opération.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Le FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifié par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Le fichier spécifié par _bstrResourceID_ a une FileSystemPath différente de celle spécifiée.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Le chemin d'accès webPath fourni se trouve dans un autre cache.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient:: SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Définit le cache dans un État en ligne ou hors connexion. Si ce n'est pas le cas, Office ne tentera pas de communiquer avec le serveur pour les fichiers de ce cache, quel que soit le paramètre _fBlockUploads_ de chaque fichier individuel. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Paramètres

 _fIsOnline_
  
Valeur booléenne déterminant l'état de connectivité du cache. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de la définition de l'état de connectivité du cache.  <br/> |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission est utilisé pour remplacer ou restoreOffice les heuristiques de synchronisation pour le coût réseau et la consommation d'énergie. Lorsqu'il est connecté à un réseau 3G ou à un autre réseau à coût élevé, ou lorsqu'il fonctionne sur batterie ou qu'il est branché, Office peut choisir de bloquer le trafic réseau jusqu'à un temps plus opportun. Le consommateur de cette API peut l'utiliser pour remplacer les heuristiques Office et forcer la synchronisation à se produire.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Paramètres

 _nspType_
  
Indicateur qui définit le coût heuristique à remplacer. Voir [énumérAtion LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Indique s'il faut forcer la synchronisation, ce qui a pour effet de remplacer cette heuristique des coûts ou de ne pas la remplacer. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de la substitution de l'heuristique de synchronisation.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient:: Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Décharge le cache de l'objet COM et effectue des opérations de fermeture. [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelé avant la destruction de l'objet COM. Une fois appelée, aucune autre API ne peut être appelée, l'objet COM doit être détruit et un nouveau créé si vous souhaitez poursuivre les opérations. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Paramètres

Aucun.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de l'échec de l'initialisation.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interface IEnumLSCEvent

Cette interface représente une liste d'événements ILSCEvent.
  
**Fonctions membres publiques**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent:: FNext

Extrait l'événement suivant de la liste des événements.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Paramètres

 _ppiLSCEvent_
  
Pointeur vers une interface ILSCEvent.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Il n'y a pas plus d'événements.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent:: Reset

Rétablit l'énumérateur sur le premier événement.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Paramètres

Aucun.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
### <a name="interface-ilscevent"></a>Interface ILSCEvent

Cette interface représente un événement de synchronisation. Toutes les informations relatives à l'événement peuvent être récupérées à partir de l'interface.
  
**Fonctions membres publiques**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent:: GetConflictStatus

Notez que cette valeur est renseignée lorsque [ILSCLocalSyncClient:: GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, et non lorsque l'événement a été créé, de sorte que vous n'aurez que l'état actuel du fichier, et non l'état du fichier lorsque l'état du conflit a changé. 
  
Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Paramètres

 _pfIsInConflict_
  
État de conflit actuel du fichier associé à l'événement.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent:: GetError

Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Paramètres

 _pnError_
  
L'erreur associée à cet événement.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent:: GetETag

Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Paramètres

 _pbstrETag_
  
ETag associé à cet événement
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent:: GetEventType

Obtient le type de cet événement.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Paramètres

 _pnEventType_
  
Type d'événement de cet événement. Voir [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs valides. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent:: GetLocalWorkingPath

Obtient le chemin de travail local de cet événement.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Paramètres

 _pbstrLocalWorkingPath_
  
Chemin d'accès local du fichier auquel cet événement se rapporte. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent:: GetResourceID

Obtient l'ID de ressource de l'événement.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _pbstrResourceID_
  
ResourceID du fichier associé à cet événement.
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent:: GetResourceIDAttempted

Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnFilePathConflict. Lorsqu'un appel à [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoquerait un chemin d'accès Web ou une collision de chemin d'accès local avec un autre fichier dans le cache de fichiers Office, ce l'événement est généré. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Paramètres

 _pbstrResourceIDAttempted_
  
IDRessource à l'origine de l'événement à obtenir. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent:: GetSyncErrorType

Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Paramètres

 _pnSyncErrorType_
  
Type d'erreur associé à cet événement. Voir [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs potentielles. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent:: GetWebPath

Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Paramètres

 _pbstrWebPath_
  
Spécifie le chemin d'accès Web associé à cet événement. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK. 
  
### <a name="interface-ilscevent2"></a>Interface ILSCEvent2

Cette interface contient des informations supplémentaires sur un événement de synchronisation.
  
**Fonctions membres publiques**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2:: GetErrorChain

Obtient les informations de chaîne d'erreur relatives à un événement de synchronisation.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Paramètres

 _pbstrErrorChain_
  
Chaîne contenant les informations de chaîne d'erreur. Ne doit pas être null. 
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_NOTIMPL  <br/> |La version installée d'Office ne prend pas en charge cette interface  <br/> |
|E_INVALIDARG  <br/> |Une ou plusieurs valeurs de paramètres ne sont pas valides.  <br/> |
|E_FAIL  <br/> |Les informations de chaîne d'erreur ne sont pas disponibles.  <br/> |
|S_OK  <br/> |L'appel a réussi.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interface IPartnerActivityCallback

Cette interface fournit une fonction de rappel à l'objet COM CSISyncClient.
  
**Fonctions membres publiques**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback:: EventOccurred

Il s'agit d'une fonction de rappel sur l'objet donné à l'objet COM CsiSyncClient. Lorsqu'un événement se produit (voir [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les types d'événements valides), l'objet com CsiSyncClient appelle cette méthode, en signalant le consommateur. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Paramètres

 _eEventTypeOccurred_
  
Type d'événement de cet événement. Voir [énumérAtion LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les valeurs valides. 
  
##### <a name="return-values"></a>Valeurs de retour

Renvoie toujours S_OK.
  
## <a name="enumerations"></a>Énumérations

CSISyncClient utilise les énumérations suivantes.
  
### <a name="enum-lsceventsyncerrortype"></a>Énumération LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Cette énumération spécifie les catégories d'erreurs qui peuvent se produire lors de la synchronisation d'un fichier.
  
|Sa|Description|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |L'erreur de synchronisation de cet événement était inattendue et peut nécessiter une attention particulière. Par défaut, l'utilisateur peut être amené à intervenir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |L'erreur de synchronisation de cet événement n'a pas besoin de tenir compte d'une attention particulière. Office le gérera automatiquement.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |L'erreur de synchronisation de cet événement nécessite qu'un utilisateur le résolve. Par exemple, l'erreur de conflit de fusion nécessite un utilisateur pour ouvrir le document et le fusionner.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |L'erreur de synchronisation de cet événement nécessite l'intervention du consommateur, mais ne doit pas exiger une attention particulière de l'utilisateur.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |L'erreur de synchronisation de cet événement nécessite que le consommateur intervienne en tant que cas particulier.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Énumération LSCEventType
<a name="Enum_LSCEventType"> </a>

Cette énumération spécifie le type d'événements pouvant se produire pour un fichier particulier.
  
|Sa|Description|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Des modifications ont été apportées à un fichier local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Un utilisateur A ouvert un fichier.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Fin du téléchargement des modifications de fichier à partir du serveur.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Fin du chargement des modifications apportées au fichier sur le serveur.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |L'état de conflit de fusion d'un fichier a changé.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Un fichier a été ajouté.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Un fichier a été supprimé.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |La synchronisation a été activée pour les fichiers d'un utilisateur.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Début du téléchargement des modifications de fichier à partir du serveur.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Début du chargement des modifications apportées au fichier sur le serveur.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Cet événement est généré lorsqu'un appel à [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque une collision de chemin d'accès Web ou de chemin d'accès local avec un autre fichier dans le Cache de fichiers Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Énumération LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Cette énumération spécifie le type d'événements pouvant se produire. Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d'événement.
  
|Sa|Description|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Une ILSCEvent s'est produite. Le consommateur doit appeler [ILSCLocalSyncClient:: GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour extraire les données.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Les extensions de fichiers prises en charge ont été modifiées. Le consommateur doit appeler [ILSCLocalSyncClient:: GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions prises en charge.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Énumération LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Cette énumération spécifie les indicateurs utilisés pour une analyse heuristique des coûts réseau. 

|Sa|Description|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True si la heuristique des coûts pour les réseaux onéreux (par exemple, 3G) est remplacée.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True si l'heuristique de coût pour l'utilisation de l'énergie (par exemple, une batterie) est remplacée.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Énumération LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Cette énumération est utilisée pour représenter l'état de synchronisation d'un fichier. 
  
|Sa|Description|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True s'il y a des données en attente d'envoi au fichier serveur.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True s'il y a des données en attente de téléchargement à partir du fichier du serveur.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True si le Bureau de données a sur le fichier dans son cache est la dernière copie des données sur le disque.  <br/> |
   

