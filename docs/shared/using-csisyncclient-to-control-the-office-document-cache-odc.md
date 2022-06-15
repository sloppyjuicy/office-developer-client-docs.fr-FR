---
title: Utilisation de CSISyncClient pour contrôler le cache de documents Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Découvrez comment utiliser CSISyncClient pour contrôler le cache de documents Office (ODC).
ms.openlocfilehash: 1435277122a74c484766ee2a3cc44df179e61b3d
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083870"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Utilisation de CSISyncClient pour contrôler le cache de documents Office (ODC)

Découvrez comment utiliser CSISyncClient pour contrôler le cache de documents Office (ODC).
  
CSISyncClient est un serveur COM out-of-proc (CsiSyncClient.exe) qui permet à Microsoft OneDrive de contrôler le comportement du cache de documents Office (ODC). Par exemple, OneDrive pouvez faire appel à l’ODC via CSISyncClient pour charger et télécharger des fichiers vers et à partir de points de terminaison compatibles MS-FSSHTTP. Cela permet d’utiliser des fonctionnalités avancées soutenues par le service dans Office, telles que la co-création et les transitions transparentes entre hors connexion et en ligne.
  
CsiSyncClient est disponible dans Office Desktop (x86 et x64). Remarque : Bien que les versions plus récentes de Office puissent être livrées avec CsiSyncClient, le processus sera utilisé uniquement pour la compatibilité descendante. L’interface CsiSyncClient et la méthodologie de contrôle de l’ODC changeront dans les versions ultérieures de Office.
  
L’ID de classe est actuellement configuré pour répondre uniquement à OneDrive.
  
L’objet COM est utilisable en tant que serveur COM out-of-proc et s’exécute dans CsiSyncClient.exe. En raison des limitations d’Access (que l’ODC utilise), il est fourni avec le type de bit que Office entre, donc x64 Office signifie un objet COM x64 ou x86 Office signifie un objet COM x86. Pour contourner cette limitation, en spécifiant CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance, l’objet COM sera hébergé en tant que serveur COM out-of-proc, ce qui permet une compatibilité entre bits.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient utilise les interfaces suivantes.
  
### <a name="interface-ilsclocalsyncclient"></a>Interface ILSCLocalSyncClient

Il s’agit de l’interface principale utilisée pour synchroniser les fichiers dans Office.
  
- ProgID : Office. LocalSyncClient
- CLSID : {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib : {66CDD37F-D313-4e81-8C31-4198F3E42C3C}

L’objet COM exposé est utilisé comme serveur hors processus. Spécifier CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet une compatibilité entre les processus 64 bits et 32 bits.
  
Une fois que vous avez cocréé l’objet COM, vous DEVEZ d’abord appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . Une fois [qu’ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a réussi, vous pouvez appeler n’importe quelle API aussi souvent que vous le souhaitez et dans n’importe quel ordre. Vous pouvez également appeler [ILSCLocalSyncClient::Initialiser](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela ne fait rien.
  
Les exceptions au paragraphe précédent sont [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Après avoir appelé [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l’objet COM, vous DEVEZ détruire cet objet et en créer un. [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprime votre sous-ache, supprime toutes les informations de fichier associées dans le cache, mais laisse les documents sur le disque. Il laisse également l’état intact pour la communication avec le cache. Cela vous permet d’appeler [ILSCLocalSyncClient::Initialiser](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) à nouveau pour créer un cache sans avoir à détruire et recréer l’objet COM.
  
**Fonctions membres publiques**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile est utilisé pour supprimer les informations de fichier du cache. Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
Chaîne qui identifie l’ID de ressource du fichier. Cette valeur doit être non vide avec un maximum de 128 caractères.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_LSC_FILENOTFOUND  <br/> |L’ID de ressource donné n’est pas dans le cache. |
|E_LSC_NOTINITIALIZED  <br/> |L’initialisation n’a pas été appelée avec succès dans le passé. |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier est actuellement en cours de synchronisation ou ouvert et ne peut pas être supprimé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges

<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges retourne un énumérateur d’objets ILSCEvent et retourne également un jeton qui est donné à l’appel suivant à GetChanges, en supposant que le consommateur a traité l’ensemble d’événements précédent. Les événements avant _le nPreviousChangesToken_ spécifié seront supprimés et indisponibles. S’il n’y a aucun événement à traiter, _pnCurrentChangesToken_ doit avoir la même valeur que _nPreviousChangesToken_, mais _ppiEvents_ est toujours défini.
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Paramètres

 _nPreviousChangesToken_
  
Identifie l’événement qui a été traité pour la dernière fois par le consommateur.
  
 _pnCurrentChangesToken_
  
Identifie l’événement le plus récent remis au consommateur. Ne doit pas être null.
  
 _ppiEvents_
  
Énumérateur des événements remis au consommateur. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission est utilisé pour déterminer si les heuristiques de synchronisation de Office pour le coût réseau et l’utilisation de l’alimentation sont remplacées. Lorsque vous êtes sur un 3G ou un autre réseau à coût élevé, ou lorsque vous exécutez sur batterie plutôt que d’être branché, Office pouvez choisir de bloquer le trafic réseau jusqu’à un moment plus opportun.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Paramètres

 _nspType_
  
Indicateur qui définit le coût heuristique à interroger. Consultez [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _pfSyncEnabled_
  
Spécifie si le coût heuristique demandé est actuellement remplacé ou non. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique : s’il existe dans le cache, s’il a une communication en attente avec la copie du serveur et si Office 2013 contient les données les plus récentes de la copie locale. Il nécessite un indicateur au niveau du bit des valeurs [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations que l’objet COM CsiSyncClient doit rechercher.
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
Chaîne qui identifie le fichier sur le client. Cette valeur doit être non vide, avec un maximum de 128 caractères.
  
 _sfRequestedStatus_
  
Indicateur qui définit les informations à retourner. Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).
  
 _pbstrFileSystemPath_
  
Chaîne qui identifie l’emplacement du fichier identifié par _bstrResourceID_ sur le client. Ne doit pas être null.
  
 _pbstrETag_
  
Chaîne qui contiendra l’eTag pour le fichier identifié par _bstrResourceID_. Ne doit pas être null.
  
 _psfFileStatus_
  
Indicateur qui contiendra l’état demandé via _sfRequestedStatus_ pour le fichier identifié par _bstrResourceID_. Ne doit pas être null. Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_FILENOTFOUND  <br/> |Les informations de fichier spécifiées par _bstrResourceID_ n’existent pas dans le cache. |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged a été demandé ou le fichier spécifié par _bstrResourceID_ est verrouillé ou manquant. |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions

<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions retourne une liste d’extensions de fichier délimitées par un canal qui sont actuellement prises en charge par l’objet COM CsiSyncClient. Notez que cette liste peut changer et que le consommateur est averti d’une modification via l’objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured).
  
Voici un exemple de chaîne retournée : « |docx|docm|pptx| »
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Paramètres

 _pbstrSupportedFileExtensions_
  
Chaîne à définir avec un ensemble délimité par un canal d’extensions de fichier pris en charge par l’objet COM CsiSyncClient. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize

<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize doit être la première méthode appelée. Sinon, toutes les autres API retournent E_LSC_NOTINITIALIZED. L’appel d’Initialize sur un objet déjà initialisé retourne S_OK et ne fait rien. Si E_LSC_CACHEMISMATCH est retourné, l’appelant peut appeler [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé à l’ID fourni donné. Toutefois, dans ce cas, d’autres API retournent toujours E_LSC_NOTINITIALIZED.
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Paramètres

 _bstrSuppliedID_
  
Identifie le consommateur et le cache à utiliser. Doit être non vide avec un maximum de 32 caractères.
  
 _bstrProgID_
  
Identifie l’objet COM du consommateur pour la communication bidirectionnelle. Doit être non vide avec un maximum de 39 caractères. Pour plus d’informations sur les progID, consultez [\<ProgID\> La clé](/windows/win32/com/-progid--key) .
  
 _bstrFileSystemDirectoryHint_
  
Identifie la racine du répertoire dans laquelle les fichiers locaux seront stockés. Doit être non vide avec un maximum de 256 caractères. Le répertoire doit déjà exister.
  
 _pEventCallback_
  
Interface de rappel que CsiSyncClient notifiera en cas de modifications. Voir IPartnerActivityCallback::EventOccurred. Cette valeur ne doit pas être null.
  
 _pfCreatedNewCache_
  
Retourne si un nouveau cache a été créé. Si aucun cache n’est associé à l’ID fourni, un cache est créé. Cette valeur ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_CACHEMISMATCH  <br/> |Un ProvidedID a déjà un cache associé, mais a un ProgId ou FileSystemDirectoryHint différent de celui fourni. |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |FileSystemDirectoryHint (ou un sous-dossier) existe déjà sur un autre cache. |
|E_LAC_PROGIDCONFLICT  <br/> |Le ProgID existe déjà sur un autre cache. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange

<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange est utilisé pour indiquer à l’objet COM CsiSyncClient de tenter de charger le fichier spécifié. La méthode prépare le fichier pour le chargement, y compris la lecture du contenu actuel du fichier. Si un chargement est déjà en attente, le chargement précédent est ignoré et le nouveau contenu préparé pour le chargement. Si le fichier est ouvert pour modification dans une application, cette méthode retourne S_OK sans préparer le fichier pour le chargement (l’application doit déjà effectuer cette étape en cas de modifications).
  
Cette méthode autorise les chargements s’ils ont été marqués comme des chargements bloqués précédemment (voir [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _bstrFileSystemPath_
  
Chaîne qui identifie le fichier sur le client. Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères. Ce chemin d’accès doit se trouver dans l’arborescence de répertoires spécifiée par FileSystemDirectoryHint lorsque l’appel à [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué.
  
 _bstrResourceID_
  
Chaîne qui identifie l’ID de ressource du fichier. Cette valeur doit être non vide avec un maximum de 128 caractères.
  
 _bstrWebPath_
  
Chaîne qui identifie le fichier sur le serveur. Cette valeur doit être une URL non vide et valide, mais pas plus INTERNET_MAX_URL_LENGTH, comme défini par <https://support.microsoft.com/kb/208427>.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_CONFLICTINGFILE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ a un ResourceID différent de celui spécifié. Un événement de type LSCEventType_OnFilePathConflict est envoyé lorsque cette erreur est retournée. Voir [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges). |
|E_LSC_FILENOTFOUND  <br/> |Le fichier a été supprimé au milieu de l’opération. |
|E_LSC_FILENOTSUPPORTED  <br/> |L’extension de fichier donnée n’est pas prise en charge par l’objet COM CsiSyncClient. Voir [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions). |
|E_LSC_FILEUPTODATE  <br/> |L’objet COM n’a pas planifié de chargement, car le fichier dans le cache avait les modifications les plus récentes du disque. |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ est manquant ou verrouillé. |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |FileSystemPath donné ne se trouve pas sous la racine de répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize. |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|E_LSC_PATHMISMATCH  <br/> |Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié. |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur. |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Le WebPath fourni se trouve sous un autre cache. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile

<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile associe une nouvelle URL et un chemin d’accès local pour un ResourceID donné. Si le fichier spécifié par l’ID de ressource n’existe pas déjà dans le cache, une tentative est effectuée pour le créer et le marquer pour téléchargement.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Paramètres

 _bstrResourceID_
  
Chaîne qui identifie l’ID de ressource du fichier. Cette valeur doit être non vide avec un maximum de 128 caractères.
  
 _bstrNewFileSystemPath_
  
Chaîne qui spécifie le nouveau chemin d’accès local pour le fichier. Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères. Ce chemin d’accès doit se trouver dans l’arborescence de répertoires spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.
  
 _bstrNewWebPath_
  
Chaîne qui spécifie la nouvelle URL du fichier. Cette valeur doit être une URL valide non vide, mais pas plus INTERNET_MAX_URL_LENGTH, comme défini par <https://support.microsoft.com/kb/208427>.
  
 _fBlockUploads_
  
Spécifie si les chargements vers le nouvel emplacement sont actuellement autorisés.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_CONFLICTINGFILE  <br/> |_BstrNewFileSystemPath_ ou _bstrNewWebPath_ existent déjà sur un autre fichier dans n’importe quel cache. Un événement de type LSCEventType_OnFilePathConflict est envoyé lorsque cette erreur est retournée. Voir [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges). |
|E_LSC_FILENOTFOUND  <br/> |Les informations de fichier ont été supprimées du cache pendant l’exécution de cette méthode. |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |FileSystemPath donné ne se trouve pas sous la racine de répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize. |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié est en cours de synchronisation dans une application Office. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache

<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache supprime le cache associé à l’ID fourni lors de l’initialisation. Cela inclut toutes les informations de fichier, mais laisse les fichiers sur le client et le serveur. Cette méthode laisse également l’objet dans un état partiellement non initialisé. Les seuls appels valides après cela sont [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Cette méthode peut être appelée si Initialize échoue et retourne E_LSC_CACHEMISMATCH et supprime le cache associé à l’ID fourni avec l’appel ayant échoué.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Paramètres

Aucun
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |L’appel n’a pas réussi. |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange

<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange indique à l’objet CSISyncClient COM de marquer le fichier spécifié pour téléchargement. Si le fichier est ouvert dans une application Office à modifier, cette méthode retourne S_OK sans marquer le fichier pour téléchargement (l’application doit déjà effectuer cette étape en cas de modifications).
  
Cette méthode autorise les téléchargements s’ils ont été marqués comme téléchargements bloqués précédemment (voir RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Chaîne qui identifie le fichier sur le client. Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères. Ce chemin d’accès doit se trouver dans l’arborescence de répertoires spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize. |
|bstrResourceID  <br/> |Chaîne qui identifie l’ID de ressource du fichier. Cette valeur doit être non vide avec un maximum de 128 caractères. |
|bstrWebPath  <br/> |Chaîne qui identifie le fichier sur le serveur. Cette valeur doit être une URL valide non vide, mais pas plus INTERNET_MAX_URL_LENGTH, comme défini par <https://support.microsoft.com/kb/208427>. |

##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de définition de l’état de connectivité du cache. |
|E_LSC_CONFLICTINGFILE  <br/> |Le fichier spécifié par _bstrFileSystemPath_ a un ResourceID différent de celui spécifié. |
|E_LSC_FILENOTSUPPORTED  <br/> |L’extension de fichier donnée n’est pas prise en charge par l’objet COM CsiSyncClient. Consultez GetSupportedFileExtensions. |
|E_LSC_FILENOTFOUND  <br/> |Le fichier a été supprimé au milieu de l’opération. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |FileSystemPath donné ne se trouve pas sous la racine de répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize. |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|E_LSC_PATHMISMATCH  <br/> |Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié. |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur. |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Le WebPath fourni se trouve sous un autre cache. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState

<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Définit le cache dans un état en ligne ou hors connexion. En mode hors connexion, Office ne tente pas de communiquer avec le serveur pour les fichiers de ce cache, quel que soit le paramètre _fBlockUploads_ de chaque fichier individuel.
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Paramètres

 _fIsOnline_
  
Valeur booléenne déterminant l’état de connectivité du cache.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de définition de l’état de connectivité du cache. |
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission

<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission est utilisé pour remplacer ou restaurer l’heuristique de synchronisation d’Office pour le coût réseau et l’utilisation de l’alimentation. Lorsque vous êtes sur un 3G ou un autre réseau à coût élevé, ou lorsque vous exécutez sur batterie plutôt que d’être branché, Office pouvez choisir de bloquer le trafic réseau jusqu’à un moment plus opportun. Le consommateur de cette API peut l’utiliser pour remplacer les heuristiques de Office et forcer la synchronisation à se produire.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Paramètres

 _nspType_
  
Indicateur qui définit le coût heuristique à remplacer. Consultez [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Spécifie s’il faut forcer la synchronisation, remplaçant ainsi ce coût heuristique, ou pour ne plus le remplacer.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec du remplacement de l’heuristique de synchronisation. |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize

<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Décharge le cache de l’objet COM et effectue des opérations de fermeture. [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelé avant de détruire l’objet COM. Une fois appelé, aucune autre API ne peut être appelée, l’objet COM DOIT être détruit et un nouvel objet doit être créé si vous souhaitez poursuivre les opérations.
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Paramètres

Aucun.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Échec de l’initialisation. |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé. |
|S_OK  <br/> |L'appel a réussi. |

### <a name="interface-ienumlscevent"></a>Interface IEnumLSCEvent

Cette interface représente une liste d’événements ILSCEvent.
  
**Fonctions membres publiques**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Récupère l’événement suivant à partir de la liste des événements.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Paramètres

 _ppiLSCEvent_
  
Pointeur vers une interface ILSCEvent.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_FAIL  <br/> |Il n’y a plus d’événements. |
|S_OK  <br/> |L’appel a réussi. |

#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Réinitialise l’énumérateur au premier événement.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Paramètres

Aucun.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
### <a name="interface-ilscevent"></a>Interface ILSCEvent

Cette interface représente un événement de synchronisation. Toutes les informations sur l’événement peuvent être récupérées à partir de l’interface.
  
**Fonctions membres publiques**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Notez que cette valeur est remplie quand [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, et non quand l’événement a été créé. Vous n’aurez donc que l’état actuel du fichier, et non l’état du fichier lorsque l’état du conflit a changé.
  
Cette valeur est remplie uniquement lorsque [l’enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnLocalConflictStateChanged.
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Paramètres

 _pfIsInConflict_
  
État actuel du conflit du fichier associé à l’événement.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Cette valeur est remplie uniquement lorsque [l’enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Paramètres

 _pnError_
  
Erreur associée à cet événement.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Cette valeur est remplie uniquement lorsque [l’enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Paramètres

 _pbstrETag_
  
ETag associé à cet événement
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Obtient le type de cet événement.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Paramètres

 _pnEventType_
  
Type d’événement de cet événement. Consultez [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour connaître les valeurs valides. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|S_OK  <br/> |L’appel a réussi. |

#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Obtient le chemin d’accès de travail local pour cet événement.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Paramètres

 _pbstrLocalWorkingPath_
  
Chemin d’accès local du fichier auquel cet événement se rapporte.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Obtient l’ID de ressource pour l’événement.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Paramètres

 _pbstrResourceID_
  
ID de ressource du fichier associé à cet événement.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Cette valeur est remplie uniquement lorsque [l’enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict. Lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange) ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque une collision de chemin d’accès web ou de chemin local avec un autre fichier dans le cache de fichiers Office, cet événement est généré.
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Paramètres

 _pbstrResourceIDAttempted_
  
ID de ressource qui a provoqué la génération de cet événement. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Cette valeur est remplie uniquement lorsque [l’enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Paramètres

 _pnSyncErrorType_
  
Type d’erreur associé à cet événement. Consultez [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour connaître les valeurs potentielles. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_INVALIDARG  <br/> |Un ou plusieurs paramètres ne sont pas valides. |
|S_OK  <br/> |L’appel a réussi. |

#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Cette valeur est remplie uniquement lorsque [l’enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Paramètres

 _pbstrWebPath_
  
Spécifie le chemin d’accès web associé à cet événement. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
### <a name="interface-ilscevent2"></a>Interface ILSCEvent2

Cette interface contient des informations supplémentaires sur un événement de synchronisation.
  
**Fonctions membres publiques**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Obtient les informations de chaîne d’erreur sur un événement de synchronisation.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Paramètres

 _pbstrErrorChain_
  
Chaîne pour contenir les informations de chaîne d’erreur. Ne doit pas être null.
  
##### <a name="return-values"></a>Valeurs de retour

|Valeur|Description|
|:-----|:-----|
|E_NOTIMPL  <br/> |La version installée de Office ne prend pas en charge cette interface  <br/> |
|E_INVALIDARG  <br/> |Une ou plusieurs des valeurs de paramètre ne sont pas valides. |
|E_FAIL  <br/> |Les informations de chaîne d’erreur ne sont pas disponibles. |
|S_OK  <br/> |L’appel a réussi. |

### <a name="interface-ipartneractivitycallback"></a>Interface IPartnerActivityCallback

Cette interface fournit une fonction de rappel à l’objet COM CSISyncClient.
  
**Fonctions membres publiques**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Il s’agit d’une fonction de rappel sur l’objet donné à l’objet CSISyncClient COM. Lorsqu’un événement se produit (voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les types d’événements valides), l’objet CSISyncClient COM appelle cette méthode, signalant le consommateur.
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Paramètres

 _eEventTypeOccurred_
  
Type d’événement de cet événement. Consultez [Enum LSCEventTypeOccurred pour connaître](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) les valeurs valides.
  
##### <a name="return-values"></a>Valeurs de retour

Retourne toujours S_OK.
  
## <a name="enumerations"></a>Énumérations

CSISyncClient utilise les énumérations suivantes.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType

<a name="Enum_LSCEventSyncErrorType"> </a>

Cette énumération spécifie les catégories d’erreurs qui peuvent se produire lors de la synchronisation d’un fichier.
  
|Énumérateur|Description|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |L’erreur de synchronisation de cet événement était inattendue et peut nécessiter une attention particulière. Par défaut, l’utilisateur peut être amené à intervenir. |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |L’erreur de synchronisation de cet événement n’a pas besoin d’une attention particulière. Office le gérera automatiquement. |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |L’erreur de synchronisation de cet événement nécessite qu’un utilisateur le résolvent. Par exemple, une erreur de conflit de fusion nécessite qu’un utilisateur ouvre le document et le fusionne. |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |L’erreur de synchronisation de cet événement oblige le consommateur à intervenir, mais ne doit pas nécessiter de considération particulière de la part de l’utilisateur. |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |L’erreur de synchronisation de cet événement nécessite que le consommateur intervienne en tant que cas particulier. |
|LSCEventSyncErrorType_Max  <br/> ||

### <a name="enum-lsceventtype"></a>Enum LSCEventType

<a name="Enum_LSCEventType"> </a>

Cette énumération spécifie le type d’événements qui peuvent se produire pour un fichier particulier.
  
|Énumérateur|Description|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Des modifications ont été apportées à un fichier local. |
|LSCEventType_OnOpenedByUser  <br/> |Un utilisateur a ouvert un fichier. |
|LSCEventType_OnServerChangesDownloaded  <br/> |Téléchargement terminé des modifications de fichier à partir du serveur. |
|LSCEventType_OnLocalChangesUploaded  <br/> |Chargement terminé des modifications de fichier sur le serveur. |
|LSCEventType_OnLocalConflictStateChanged  <br/> |L’état de conflit de fusion d’un fichier a changé. |
|LSCEventType_OnFileAdded  <br/> |Un fichier a été ajouté. |
|LSCEventType_OnFileDeleted  <br/> |Un fichier a été supprimé. |
|LSCEventType_OnSyncEnabled  <br/> |La synchronisation a été activée pour les fichiers d’un utilisateur. |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Démarrage du téléchargement des modifications de fichier à partir du serveur. |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Démarrage du chargement des modifications de fichier sur le serveur. |
|LSCEventType_OnFilePathConflict  <br/> |Cet événement est généré lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange) ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque une collision de chemin d’accès web ou de chemin local avec un autre fichier dans le cache de fichiers Office. |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||

### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred

<a name="Enum_LSCEventTypeOccurred"> </a>

Cette énumération spécifie le type d’événements qui peuvent se produire. Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d’événement.
  
|Énumérateur|Description|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Un événement ILSCEvent s’est produit. Le consommateur doit appeler [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour récupérer les données. |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Les extensions de fichier prises en charge ont changé. Le consommateur doit appeler [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions prises en charge. |

### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType

<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Cette énumération spécifie les indicateurs utilisés pour un coût réseau heuristique.

|Énumérateur|Description|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True si le coût heuristique pour les réseaux coûteux (tels que 3G) est remplacé. |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True si le coût heuristique de l’utilisation de l’alimentation (par exemple, une batterie) est remplacé. |

### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag

<a name="Enum_LSCStatusFlag"> </a>

Cette énumération est utilisée pour représenter l’état de synchronisation d’un fichier.
  
|Énumérateur|Description|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True s’il existe des données en attente à envoyer au fichier serveur. |
|LSCStatusFlag_DownloadPending  <br/> |True s’il existe des données en attente à télécharger à partir du fichier serveur. |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True si les données Office ont sur le fichier dans son cache est la copie la plus récente des données sur le disque. |
