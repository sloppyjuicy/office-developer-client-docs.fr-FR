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
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="87005-103">Utilisation de CSISyncClient pour contrôler le Cache de documents Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="87005-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="87005-104">Découvrez comment utiliser CSISyncClient pour contrôler le Cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="87005-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="87005-105">CSISyncClient est un serveur COM out-of-process (CsiSyncClient.exe) qui permet à Microsoft OneDrive contrôler le comportement de la Cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="87005-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="87005-106">Par exemple, OneDrive peut-être faire appel à la ODC via CSISyncClient pour télécharger des fichiers vers et depuis les systèmes d’extrémité MS-FSSHTTP est activé.</span><span class="sxs-lookup"><span data-stu-id="87005-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="87005-107">Cela permet de garantie service fonctionnalités avancées dans Office, telles que les transitions de co-création et transparentes d’en mode hors connexion à en ligne.</span><span class="sxs-lookup"><span data-stu-id="87005-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="87005-108">CsiSyncClient est disponible dans Office Desktop (x86 et x64).</span><span class="sxs-lookup"><span data-stu-id="87005-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="87005-109">Remarque : Alors que les nouvelles versions d’Office peuvent livrées avec CsiSyncClient, le processus sera utilisé pour la compatibilité descendante uniquement.</span><span class="sxs-lookup"><span data-stu-id="87005-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="87005-110">L’interface CsiSyncClient et la méthodologie de contrôler le ODC seront modifié dans les futures versions de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="87005-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="87005-111">L’identificateur de classe est actuellement définie pour répondre uniquement à OneDrive.</span><span class="sxs-lookup"><span data-stu-id="87005-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="87005-112">L’objet COM est utilisable comme serveur COM out-of-proc et s’exécute dans CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="87005-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="87005-113">En raison de limitations avec Access (qui le ODC utilise), il est fourni avec le type de bit Office est fourni dans ce x64 Office signifie un x64 objet COM ou x86 Office signifie un x86 objet COM.</span><span class="sxs-lookup"><span data-stu-id="87005-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="87005-114">Pour contourner cette limitation, spécification CLSCTX_LOCAL_SERVER comme partie de l’interface CoCreateInstance aura l’objet COM être hébergé en tant qu’un serveur COM out-of-process, autoriser la compatibilité cross-nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="87005-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="87005-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="87005-115">Interfaces</span></span>

<span data-ttu-id="87005-116">CSISyncClient utilise les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="87005-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="87005-117">Interface ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="87005-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="87005-118">Il s’agit de l’interface principale utilisée pour synchroniser des fichiers dans Office.</span><span class="sxs-lookup"><span data-stu-id="87005-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="87005-119">ProgID : Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="87005-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="87005-120">CLSID : {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="87005-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="87005-121">Bibliothèque de types : {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="87005-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="87005-122">L’objet COM qui est exposé est utilisé comme un serveur out-of-Process.</span><span class="sxs-lookup"><span data-stu-id="87005-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="87005-123">Spécification CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet de compatibilité entre les processus 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="87005-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="87005-124">Une fois que vous avez créé conjointement l’objet COM, vous devez d’abord appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="87005-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="87005-125">Une fois que [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) est terminée, vous pouvez appeler n’importe quelle API aussi souvent que vous le souhaitez et dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="87005-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="87005-126">Vous pouvez également appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="87005-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="87005-127">Les exceptions pour le paragraphe précédent sont [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="87005-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="87005-128">Une fois que vous appelez [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l’objet COM, vous devez détruire cet objet et créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="87005-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="87005-129">[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprimer votre subcache, supprimez toutes les informations de fichier associé dans le cache, mais laissez les documents sur le disque.</span><span class="sxs-lookup"><span data-stu-id="87005-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="87005-130">Il également conserve l’état pour communiquer avec le cache.</span><span class="sxs-lookup"><span data-stu-id="87005-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="87005-131">Cela vous permet d’appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) à nouveau pour créer un nouveau cache sans devoir supprimer et recréer l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="87005-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="87005-132">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="87005-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="87005-133">ILSCLocalSyncClient::DeleteFile</span><span class="sxs-lookup"><span data-stu-id="87005-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="87005-134">DeleteFile est utilisée pour supprimer les informations du fichier à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="87005-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="87005-135">Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="87005-136">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-136">Parameters</span></span>

 <span data-ttu-id="87005-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="87005-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="87005-138">Chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="87005-139">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-140">Return values</span></span>

|<span data-ttu-id="87005-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-141">Value</span></span>|<span data-ttu-id="87005-142">Description</span><span class="sxs-lookup"><span data-stu-id="87005-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-144">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-146">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-148">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="87005-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="87005-150">Le ResourceID donné n’est pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="87005-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="87005-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-152">Initialize n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="87005-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="87005-154">Le fichier est en cours de synchronisation ou ouvrir et ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="87005-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="87005-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-155">S_OK</span></span>  <br/> |<span data-ttu-id="87005-156">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="87005-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="87005-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="87005-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-158"></span></span>

<span data-ttu-id="87005-159">GetChanges retourne un énumérateur des objets ILSCEvent et retourne également un jeton qui est donné à l’appel suivant à GetChanges, en supposant que le consommateur a traité l’ensemble d’événements précédent.</span><span class="sxs-lookup"><span data-stu-id="87005-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="87005-160">Événements avant le _nPreviousChangesToken_ spécifié seront supprimés et non disponible.</span><span class="sxs-lookup"><span data-stu-id="87005-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="87005-161">S’il n’y a aucun événement à traiter, _pnCurrentChangesToken_ doit être la même valeur que _nPreviousChangesToken_, mais _ppiEvents_ sera toujours définie.</span><span class="sxs-lookup"><span data-stu-id="87005-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="87005-162">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-162">Parameters</span></span>

 <span data-ttu-id="87005-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="87005-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="87005-164">Identifie l’événement qui a été traitée en dernier par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="87005-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="87005-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="87005-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="87005-166">Identifie l’événement le plus récent est transmise au consommateur.</span><span class="sxs-lookup"><span data-stu-id="87005-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="87005-167">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-167">Must not be null.</span></span>
  
 <span data-ttu-id="87005-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="87005-168">_ppiEvents_</span></span>
  
<span data-ttu-id="87005-169">Énumérateur pour les événements remis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="87005-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="87005-170">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-171">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-171">Return values</span></span>

|<span data-ttu-id="87005-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-172">Value</span></span>|<span data-ttu-id="87005-173">Description</span><span class="sxs-lookup"><span data-stu-id="87005-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-175">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-177">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-179">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-180">S_OK</span></span>  <br/> |<span data-ttu-id="87005-181">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="87005-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="87005-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="87005-183">GetClientNetworkSyncPermission est utilisée pour interroger si heuristique synchronisation du bureau pour réseau coût et consommation d’énergie sont remplacées.</span><span class="sxs-lookup"><span data-stu-id="87005-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="87005-184">Sur un 3G ou un autre réseau coûteuses, ou lors de l’exécution sur la batterie et branché, Office peut choisir de bloquer le trafic réseau jusqu'à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="87005-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="87005-185">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-185">Parameters</span></span>

 <span data-ttu-id="87005-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="87005-186">_nspType_</span></span>
  
<span data-ttu-id="87005-187">Indicateur qui définit le heuristique de coût de requête.</span><span class="sxs-lookup"><span data-stu-id="87005-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="87005-188">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="87005-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="87005-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="87005-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="87005-190">Spécifie si l’heuristique coût demandé est actuellement remplacé ou non.</span><span class="sxs-lookup"><span data-stu-id="87005-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="87005-191">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-192">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-192">Return values</span></span>

|<span data-ttu-id="87005-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-193">Value</span></span>|<span data-ttu-id="87005-194">Description</span><span class="sxs-lookup"><span data-stu-id="87005-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-196">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-198">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-200">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-201">S_OK</span></span>  <br/> |<span data-ttu-id="87005-202">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="87005-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="87005-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="87005-204">GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique : si elle existe dans le cache, si elle est en attente de la communication avec la copie sur le serveur, et si Office 2013 possède le plus jusqu'à les données de date de la copie locale.</span><span class="sxs-lookup"><span data-stu-id="87005-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="87005-205">Il nécessite un indicateur de bits des valeurs [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations de l’objet COM CsiSyncClient consiste à interroger.</span><span class="sxs-lookup"><span data-stu-id="87005-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="87005-206">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-206">Parameters</span></span>

 <span data-ttu-id="87005-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="87005-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="87005-208">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="87005-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="87005-209">Cette valeur doit être vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="87005-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="87005-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="87005-211">Indicateur qui définit les informations à retourner.</span><span class="sxs-lookup"><span data-stu-id="87005-211">A flag which defines what information to return.</span></span> <span data-ttu-id="87005-212">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="87005-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="87005-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="87005-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="87005-214">Chaîne qui identifie l’emplacement du fichier identifié par _bstrResourceID_ sur le client.</span><span class="sxs-lookup"><span data-stu-id="87005-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="87005-215">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-215">Must not be null.</span></span> 
  
 <span data-ttu-id="87005-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="87005-216">_pbstrETag_</span></span>
  
<span data-ttu-id="87005-217">Chaîne qui contient l’eTag pour le fichier identifié par _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="87005-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="87005-218">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-218">Must not be null.</span></span> 
  
 <span data-ttu-id="87005-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="87005-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="87005-220">Indicateur qui contiendra le statut demandé par le biais de _sfRequestedStatus_ pour le fichier identifié par _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="87005-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="87005-221">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-221">Must not be null.</span></span> <span data-ttu-id="87005-222">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="87005-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-223">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-223">Return values</span></span>

|<span data-ttu-id="87005-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-224">Value</span></span>|<span data-ttu-id="87005-225">Description</span><span class="sxs-lookup"><span data-stu-id="87005-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-227">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-229">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="87005-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="87005-231">Les informations du fichier spécifiées par _bstrResourceID_ n’existent pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="87005-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="87005-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="87005-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="87005-233">LSCStatusFlag_LocalFileUnchanged a été demandé, ou le fichier spécifié par _bstrResourceID_ est verrouillé ou manquant.</span><span class="sxs-lookup"><span data-stu-id="87005-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="87005-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-235">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-236">S_OK</span></span>  <br/> |<span data-ttu-id="87005-237">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="87005-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="87005-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="87005-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-239"></span></span>

<span data-ttu-id="87005-240">GetSupportedFileExtensions renvoie une liste délimitée par des canaux des extensions de fichiers qui sont actuellement pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="87005-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="87005-241">Notez que cette liste peut modifier et le consommateur serez ainsi averti d’une modification par le biais de l’objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured).</span><span class="sxs-lookup"><span data-stu-id="87005-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="87005-242">Un exemple de la chaîne renvoyée se présente comme suit : « | docx | docm | pptx | »</span><span class="sxs-lookup"><span data-stu-id="87005-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="87005-243">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-243">Parameters</span></span>

 <span data-ttu-id="87005-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="87005-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="87005-245">Chaîne à définir avec un ensemble d’extensions de fichiers pris en charge par l’objet COM CsiSyncClient délimité par canal.</span><span class="sxs-lookup"><span data-stu-id="87005-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="87005-246">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-247">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-247">Return values</span></span>

|<span data-ttu-id="87005-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-248">Value</span></span>|<span data-ttu-id="87005-249">Description</span><span class="sxs-lookup"><span data-stu-id="87005-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-251">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-253">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-255">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-256">S_OK</span></span>  <br/> |<span data-ttu-id="87005-257">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="87005-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="87005-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="87005-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-259"></span></span>

<span data-ttu-id="87005-260">Initialize doit être la première méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="87005-260">Initialize must be the first method called.</span></span> <span data-ttu-id="87005-261">Dans le cas contraire, toutes les autres API renverra E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="87005-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="87005-262">L’appel de Initialize sur un objet déjà initialisé renvoie S_OK et n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="87005-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="87005-263">Si E_LSC_CACHEMISMATCH est renvoyée, l’appelant peut appeler [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé à le SuppliedID donné.</span><span class="sxs-lookup"><span data-stu-id="87005-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="87005-264">Toutefois, dans ce cas autres API retournera encore E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="87005-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="87005-265">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-265">Parameters</span></span>

 <span data-ttu-id="87005-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="87005-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="87005-267">Identifie le consommateur et qui mettent en cache à utiliser.</span><span class="sxs-lookup"><span data-stu-id="87005-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="87005-268">Doit être vide avec un maximum de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="87005-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="87005-269">_bstrProgID_</span></span>
  
<span data-ttu-id="87005-270">Identifie un objet COM de la consommation de communication bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="87005-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="87005-271">Doit être vide avec un maximum de 39 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="87005-272">Voir [ \<ProgID\> clé](https://docs.microsoft.com/en-us/windows/desktop/com/-progid--key) pour plus d’informations sur le ProgID.</span><span class="sxs-lookup"><span data-stu-id="87005-272">See [\<ProgID\> Key](https://docs.microsoft.com/en-us/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="87005-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="87005-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="87005-274">Identifie la racine du répertoire dans lequel seront stockés les fichiers locaux.</span><span class="sxs-lookup"><span data-stu-id="87005-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="87005-275">Doit être vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="87005-276">Le répertoire doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="87005-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="87005-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="87005-277">_pEventCallback_</span></span>
  
<span data-ttu-id="87005-278">L’interface de rappel qui avertit CsiSyncClient sur les modifications.</span><span class="sxs-lookup"><span data-stu-id="87005-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="87005-279">Voir IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="87005-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="87005-280">Cette valeur ne doit pas être nulle.</span><span class="sxs-lookup"><span data-stu-id="87005-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="87005-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="87005-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="87005-282">Renvoie si un nouveau cache a été créé.</span><span class="sxs-lookup"><span data-stu-id="87005-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="87005-283">Si le cache n’est associé à la SuppliedID, un sera créé.</span><span class="sxs-lookup"><span data-stu-id="87005-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="87005-284">Cette valeur ne doit pas être nulle.</span><span class="sxs-lookup"><span data-stu-id="87005-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-285">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-285">Return values</span></span>

|<span data-ttu-id="87005-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-286">Value</span></span>|<span data-ttu-id="87005-287">Description</span><span class="sxs-lookup"><span data-stu-id="87005-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-289">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-291">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="87005-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="87005-293">Un SuppliedID déjà possède un cache qui lui est associé, mais dispose d’un ProgId ou FileSystemDirectoryHint différentes de celles qui sont fournies.</span><span class="sxs-lookup"><span data-stu-id="87005-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="87005-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="87005-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="87005-295">Le FileSystemDirectoryHint (ou un sous-dossier) existe déjà sur un cache différent.</span><span class="sxs-lookup"><span data-stu-id="87005-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="87005-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="87005-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="87005-297">Le ProgID existe déjà sur un cache différent.</span><span class="sxs-lookup"><span data-stu-id="87005-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="87005-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-298">S_OK</span></span>  <br/> |<span data-ttu-id="87005-299">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="87005-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="87005-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="87005-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-301"></span></span>

<span data-ttu-id="87005-302">LocalFileChange est utilisée pour indiquer à l’objet COM CsiSyncClient pour essayer de télécharger le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="87005-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="87005-303">La méthode prépare le fichier à télécharger, y compris le contenu du fichier en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="87005-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="87005-304">Si un téléchargement est déjà en attente, téléchargement précédent sera ignoré et le nouveau contenu préparé pour télécharger.</span><span class="sxs-lookup"><span data-stu-id="87005-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="87005-305">Si le fichier est ouvert pour modification dans une application, cette méthode renvoie S_OK sans préparer le fichier de téléchargement (l’application doit déjà effectuer cette étape si des modifications sont apportées).</span><span class="sxs-lookup"><span data-stu-id="87005-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="87005-306">Cette méthode permet volumineux s’il a été marqué comme télécharge bloqués précédemment (voir [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="87005-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="87005-307">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-307">Parameters</span></span>

 <span data-ttu-id="87005-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="87005-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="87005-309">Une chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="87005-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="87005-310">Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="87005-311">Ce chemin d’accès doit être dans l’arborescence du répertoire spécifié par le FileSystemDirectoryHint lors de l’appel à [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué.</span><span class="sxs-lookup"><span data-stu-id="87005-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="87005-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="87005-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="87005-313">Une chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="87005-314">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="87005-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="87005-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="87005-316">Une chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="87005-317">Cette valeur doit être URL non vide et valide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="87005-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-318">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-318">Return values</span></span>

|<span data-ttu-id="87005-319">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-319">Value</span></span>|<span data-ttu-id="87005-320">Description</span><span class="sxs-lookup"><span data-stu-id="87005-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-322">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-324">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="87005-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="87005-326">Le fichier spécifié par _bstrFileSystemPath_ a un autre ResourceID celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="87005-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="87005-327">Un événement de type LSCEventType_OnFilePathConflict est envoyée lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="87005-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="87005-328">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="87005-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="87005-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="87005-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="87005-330">Le fichier a été supprimée opération intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="87005-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="87005-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="87005-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="87005-332">L’extension de fichier donné n’est pas pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="87005-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="87005-333">Voir [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="87005-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="87005-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="87005-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="87005-335">L’objet COM n’avez pas prévu un téléchargement parce que le fichier dans le cache a des modifications les plus récentes à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="87005-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="87005-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="87005-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="87005-337">Le fichier spécifié par _bstrFileSystemPath_ est manquant ou verrouillé.</span><span class="sxs-lookup"><span data-stu-id="87005-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="87005-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="87005-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="87005-339">Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="87005-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="87005-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-341">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="87005-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="87005-343">Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="87005-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="87005-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="87005-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="87005-345">Le fichier spécifié déjà en attente de modification dans un cache différent et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="87005-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="87005-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="87005-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="87005-347">Le WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="87005-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="87005-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-348">S_OK</span></span>  <br/> |<span data-ttu-id="87005-349">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="87005-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="87005-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="87005-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-351"></span></span>

<span data-ttu-id="87005-352">RenameFile associe une nouvelle URL et le chemin d’accès local pour un ResourceID donné.</span><span class="sxs-lookup"><span data-stu-id="87005-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="87005-353">Si le fichier spécifié par le ResourceID n’existe pas déjà dans le cache, une tentative seront créer et marquer pour téléchargement.</span><span class="sxs-lookup"><span data-stu-id="87005-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="87005-354">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-354">Parameters</span></span>

 <span data-ttu-id="87005-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="87005-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="87005-356">Une chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="87005-357">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="87005-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="87005-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="87005-359">Chaîne qui spécifie le nouveau chemin d’accès local pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="87005-360">Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="87005-361">Ce chemin d’accès doit être dans l’arborescence spécifiée par le FileSystemDirectoryHint lors de l’appel à initialiser.</span><span class="sxs-lookup"><span data-stu-id="87005-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="87005-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="87005-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="87005-363">Chaîne qui spécifie la nouvelle URL pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="87005-364">Cette valeur doit être non vides URL valide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="87005-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="87005-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="87005-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="87005-366">Spécifie si les téléchargements vers le nouvel emplacement sont actuellement autorisées.</span><span class="sxs-lookup"><span data-stu-id="87005-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-367">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-367">Return values</span></span>

|<span data-ttu-id="87005-368">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-368">Value</span></span>|<span data-ttu-id="87005-369">Description</span><span class="sxs-lookup"><span data-stu-id="87005-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-371">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-373">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="87005-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="87005-375">Le _bstrNewFileSystemPath_ ou _bstrNewWebPath_ existent déjà sur un autre fichier dans n’importe quel cache.</span><span class="sxs-lookup"><span data-stu-id="87005-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="87005-376">Un événement de type LSCEventType_OnFilePathConflict est envoyée lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="87005-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="87005-377">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="87005-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="87005-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="87005-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="87005-379">Les informations du fichier a été supprimées du cache pendant l’exécution de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="87005-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="87005-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="87005-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="87005-381">Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="87005-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="87005-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-383">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="87005-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="87005-385">Le fichier spécifié est en cours de synchronisation dans une application Office.</span><span class="sxs-lookup"><span data-stu-id="87005-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="87005-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-386">S_OK</span></span>  <br/> |<span data-ttu-id="87005-387">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="87005-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="87005-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="87005-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-389"></span></span>

<span data-ttu-id="87005-390">ResetCache supprime le cache associé à le SuppliedID qui a été fournie dans Initialize.</span><span class="sxs-lookup"><span data-stu-id="87005-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="87005-391">Cela inclut toutes les informations sur les fichier, mais laisse les fichiers sur le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="87005-392">Cette méthode rend également l’objet dans un état partiellement non initialisé.</span><span class="sxs-lookup"><span data-stu-id="87005-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="87005-393">Les appels valides uniquement après ce sont [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="87005-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="87005-394">Cette méthode peut être appelée si Initialize échoue et renvoie E_LSC_CACHEMISMATCH et supprime le cache associé à le SuppliedID qui a été fournie avec l’appel défectueux.</span><span class="sxs-lookup"><span data-stu-id="87005-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="87005-395">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-395">Parameters</span></span>

<span data-ttu-id="87005-396">Aucune</span><span class="sxs-lookup"><span data-stu-id="87005-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-397">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-397">Return values</span></span>

|<span data-ttu-id="87005-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-398">Value</span></span>|<span data-ttu-id="87005-399">Description</span><span class="sxs-lookup"><span data-stu-id="87005-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-401">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="87005-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-403">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-404">S_OK</span></span>  <br/> |<span data-ttu-id="87005-405">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="87005-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="87005-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="87005-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-407"></span></span>

<span data-ttu-id="87005-408">ServerFileChange indique à l’objet COM CsiSyncClient pour marquer le fichier spécifié pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="87005-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="87005-409">Si le fichier est ouvert dans une application Office pour modifier, cette méthode renvoie S_OK sans marquage du fichier de téléchargement (l’application doit déjà effectuer cette étape si des modifications sont apportées).</span><span class="sxs-lookup"><span data-stu-id="87005-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="87005-410">Cette méthode permet téléchargements si elle a été marquée comme téléchargements bloqués précédemment (voir RenameFile).</span><span class="sxs-lookup"><span data-stu-id="87005-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="87005-411">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-411">Parameters</span></span>

|<span data-ttu-id="87005-412">Paramètre</span><span class="sxs-lookup"><span data-stu-id="87005-412">Parameter</span></span>|<span data-ttu-id="87005-413">Description</span><span class="sxs-lookup"><span data-stu-id="87005-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="87005-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="87005-415">Une chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="87005-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="87005-416">Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="87005-417">Ce chemin d’accès doit être dans l’arborescence spécifiée par le FileSystemDirectoryHint lors de l’appel à initialiser.</span><span class="sxs-lookup"><span data-stu-id="87005-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="87005-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="87005-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="87005-419">Une chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="87005-420">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="87005-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="87005-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="87005-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="87005-422">Une chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="87005-423">Cette valeur doit être une URL valide non vide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="87005-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="87005-424">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-424">Return values</span></span>

|<span data-ttu-id="87005-425">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-425">Value</span></span>|<span data-ttu-id="87005-426">Description</span><span class="sxs-lookup"><span data-stu-id="87005-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-428">Échec pour définir l’état de la connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="87005-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="87005-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="87005-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="87005-430">Le fichier spécifié par _bstrFileSystemPath_ a un autre ResourceID celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="87005-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="87005-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="87005-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="87005-432">L’extension de fichier donné n’est pas pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="87005-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="87005-433">Voir GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="87005-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="87005-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="87005-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="87005-435">Le fichier a été supprimé dans une opération intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="87005-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="87005-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-437">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="87005-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="87005-439">Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="87005-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="87005-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-441">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="87005-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="87005-443">Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="87005-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="87005-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="87005-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="87005-445">Le fichier spécifié a des modifications en attente dans un cache différent déjà et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="87005-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="87005-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="87005-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="87005-447">Le WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="87005-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="87005-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-448">S_OK</span></span>  <br/> |<span data-ttu-id="87005-449">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="87005-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="87005-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="87005-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-451"></span></span>

<span data-ttu-id="87005-452">Définit le cache dans un état en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="87005-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="87005-453">Si elle est en mode hors connexion, Office tentera pas à communiquer avec le serveur pour tous les fichiers dans ce cache, quel que soit le paramètre de _fBlockUploads_ de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="87005-454">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-454">Parameters</span></span>

 <span data-ttu-id="87005-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="87005-455">_fIsOnline_</span></span>
  
<span data-ttu-id="87005-456">Valeur de type boolean détermination de l’état de la connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="87005-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-457">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-457">Return values</span></span>

|<span data-ttu-id="87005-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-458">Value</span></span>|<span data-ttu-id="87005-459">Description</span><span class="sxs-lookup"><span data-stu-id="87005-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-461">Échec pour définir l’état de la connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="87005-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="87005-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-463">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-465">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-466">S_OK</span></span>  <br/> |<span data-ttu-id="87005-467">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="87005-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="87005-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="87005-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-469"></span></span>

<span data-ttu-id="87005-470">SetClientNetworkSyncPermission est utilisé pour substituer ou heuristique de synchronisation de restoreOffice pour réseau d’utilisation de coûts et d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="87005-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="87005-471">Sur un 3G ou un autre réseau coûteuses, ou lors de l’exécution sur la batterie et branché, Office peut choisir de bloquer le trafic réseau jusqu'à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="87005-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="87005-472">Le consommateur de cette API pouvez l’utiliser pour remplacer heuristique d’Office et de forcer la synchronisation ait lieu.</span><span class="sxs-lookup"><span data-stu-id="87005-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="87005-473">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-473">Parameters</span></span>

 <span data-ttu-id="87005-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="87005-474">_nspType_</span></span>
  
<span data-ttu-id="87005-475">Indicateur qui définit le heuristique coût à remplacer.</span><span class="sxs-lookup"><span data-stu-id="87005-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="87005-476">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="87005-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="87005-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="87005-477">_fEnableSync_</span></span>
  
<span data-ttu-id="87005-478">Spécifie s’il faut forcer la synchronisation, remplaçant ainsi que heuristique coût, ou remplacer n’est plus.</span><span class="sxs-lookup"><span data-stu-id="87005-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-479">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-479">Return values</span></span>

|<span data-ttu-id="87005-480">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-480">Value</span></span>|<span data-ttu-id="87005-481">Description</span><span class="sxs-lookup"><span data-stu-id="87005-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-483">Échec de la synchronisation heuristique de remplacer.</span><span class="sxs-lookup"><span data-stu-id="87005-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="87005-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-485">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-486">S_OK</span></span>  <br/> |<span data-ttu-id="87005-487">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="87005-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="87005-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="87005-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-489"></span></span>

<span data-ttu-id="87005-490">Décharge le cache de l’objet COM et effectuer des opérations de fermeture.</span><span class="sxs-lookup"><span data-stu-id="87005-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="87005-491">[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelée avant la destruction de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="87005-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="87005-492">Une fois appelée, aucune autre API ne peut être appelé, l’objet COM doit être détruit et créer une nouvelle si vous souhaitez continuer d’opérations.</span><span class="sxs-lookup"><span data-stu-id="87005-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="87005-493">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-493">Parameters</span></span>

<span data-ttu-id="87005-494">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87005-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-495">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-495">Return values</span></span>

|<span data-ttu-id="87005-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-496">Value</span></span>|<span data-ttu-id="87005-497">Description</span><span class="sxs-lookup"><span data-stu-id="87005-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-499">Échec d’annuler l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="87005-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="87005-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87005-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="87005-501">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="87005-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="87005-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-502">S_OK</span></span>  <br/> |<span data-ttu-id="87005-503">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="87005-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="87005-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="87005-505">Cette interface représente une liste d’événements ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="87005-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="87005-506">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="87005-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="87005-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="87005-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="87005-508">Récupère l’événement suivant à partir de la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="87005-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="87005-509">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-509">Parameters</span></span>

 <span data-ttu-id="87005-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="87005-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="87005-511">Pointeur vers une interface ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="87005-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-512">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-512">Return values</span></span>

|<span data-ttu-id="87005-513">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-513">Value</span></span>|<span data-ttu-id="87005-514">Description</span><span class="sxs-lookup"><span data-stu-id="87005-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-516">Il existe plus d’événements.</span><span class="sxs-lookup"><span data-stu-id="87005-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="87005-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-517">S_OK</span></span>  <br/> |<span data-ttu-id="87005-518">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="87005-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="87005-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="87005-520">Réinitialise l’énumérateur au premier événement.</span><span class="sxs-lookup"><span data-stu-id="87005-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="87005-521">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-521">Parameters</span></span>

<span data-ttu-id="87005-522">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87005-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-523">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-523">Return values</span></span>

<span data-ttu-id="87005-524">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="87005-525">Interface ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="87005-525">Interface ILSCEvent</span></span>

<span data-ttu-id="87005-526">Cette interface représente un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="87005-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="87005-527">Toutes les informations relatives à l’événement peuvent être récupérées à partir de l’interface.</span><span class="sxs-lookup"><span data-stu-id="87005-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="87005-528">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="87005-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="87005-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="87005-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="87005-530">Notez que cette valeur est renseignée lorsque [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, pas lorsque l’événement a été créé, vous devrez uniquement l’état actuel du fichier, pas l’état du fichier lors de la modification de l’état de conflit.</span><span class="sxs-lookup"><span data-stu-id="87005-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="87005-531">Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="87005-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="87005-532">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-532">Parameters</span></span>

 <span data-ttu-id="87005-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="87005-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="87005-534">L’état actuel de conflit du fichier associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="87005-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-535">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-535">Return values</span></span>

<span data-ttu-id="87005-536">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="87005-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="87005-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="87005-538">Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="87005-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="87005-539">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-539">Parameters</span></span>

 <span data-ttu-id="87005-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="87005-540">_pnError_</span></span>
  
<span data-ttu-id="87005-541">L’erreur associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-542">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-542">Return values</span></span>

<span data-ttu-id="87005-543">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="87005-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="87005-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="87005-545">Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="87005-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="87005-546">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-546">Parameters</span></span>

 <span data-ttu-id="87005-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="87005-547">_pbstrETag_</span></span>
  
<span data-ttu-id="87005-548">L’ETag associé à cet événement</span><span class="sxs-lookup"><span data-stu-id="87005-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-549">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-549">Return values</span></span>

<span data-ttu-id="87005-550">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="87005-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="87005-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="87005-552">Obtient le type de cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="87005-553">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-553">Parameters</span></span>

 <span data-ttu-id="87005-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="87005-554">_pnEventType_</span></span>
  
<span data-ttu-id="87005-555">Le type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-555">The event type of this event.</span></span> <span data-ttu-id="87005-556">Voir [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="87005-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="87005-557">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-558">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-558">Return values</span></span>

|<span data-ttu-id="87005-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-559">Value</span></span>|<span data-ttu-id="87005-560">Description</span><span class="sxs-lookup"><span data-stu-id="87005-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-562">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-563">S_OK</span></span>  <br/> |<span data-ttu-id="87005-564">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="87005-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="87005-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="87005-566">Obtient le chemin d’accès local de travail de cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="87005-567">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-567">Parameters</span></span>

 <span data-ttu-id="87005-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="87005-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="87005-569">Le chemin d’accès local du fichier à laquelle cet événement se rapporte.</span><span class="sxs-lookup"><span data-stu-id="87005-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-570">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-570">Return values</span></span>

<span data-ttu-id="87005-571">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="87005-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="87005-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="87005-573">Obtient l’ID de ressource pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="87005-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="87005-574">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-574">Parameters</span></span>

 <span data-ttu-id="87005-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="87005-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="87005-576">ResourceID du fichier associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="87005-577">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-577">Return values</span></span>

<span data-ttu-id="87005-578">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="87005-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="87005-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="87005-580">Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="87005-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="87005-581">Lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque un conflit de chemin d’accès Web ou le chemin d’accès Local avec un autre fichier dans le cache des fichiers Office, cela événement est généré.</span><span class="sxs-lookup"><span data-stu-id="87005-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="87005-582">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-582">Parameters</span></span>

 <span data-ttu-id="87005-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="87005-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="87005-584">ResourceID qui a provoqué cet événement sont générés.</span><span class="sxs-lookup"><span data-stu-id="87005-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="87005-585">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-586">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-586">Return values</span></span>

<span data-ttu-id="87005-587">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="87005-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="87005-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="87005-589">Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="87005-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="87005-590">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-590">Parameters</span></span>

 <span data-ttu-id="87005-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="87005-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="87005-592">Le type d’erreur associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-592">The error type associated with this event.</span></span> <span data-ttu-id="87005-593">Voir [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="87005-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="87005-594">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-595">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-595">Return values</span></span>

|<span data-ttu-id="87005-596">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-596">Value</span></span>|<span data-ttu-id="87005-597">Description</span><span class="sxs-lookup"><span data-stu-id="87005-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-599">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-600">S_OK</span></span>  <br/> |<span data-ttu-id="87005-601">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="87005-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="87005-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="87005-603">Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="87005-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="87005-604">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-604">Parameters</span></span>

 <span data-ttu-id="87005-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="87005-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="87005-606">Spécifie le chemin d’accès Web associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="87005-607">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-608">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-608">Return values</span></span>

<span data-ttu-id="87005-609">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="87005-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="87005-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="87005-611">Cette interface conserve des informations supplémentaires sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="87005-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="87005-612">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="87005-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="87005-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="87005-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="87005-614">Obtient les informations de la chaîne d’erreur sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="87005-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="87005-615">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-615">Parameters</span></span>

 <span data-ttu-id="87005-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="87005-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="87005-617">Une chaîne contenant les informations de la chaîne d’erreur.</span><span class="sxs-lookup"><span data-stu-id="87005-617">A string to hold the error chain information.</span></span> <span data-ttu-id="87005-618">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="87005-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-619">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-619">Return values</span></span>

|<span data-ttu-id="87005-620">Valeur</span><span class="sxs-lookup"><span data-stu-id="87005-620">Value</span></span>|<span data-ttu-id="87005-621">Description</span><span class="sxs-lookup"><span data-stu-id="87005-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="87005-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="87005-623">La version d’Office installée ne prend pas en charge cette interface</span><span class="sxs-lookup"><span data-stu-id="87005-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="87005-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="87005-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="87005-625">Un ou plusieurs des valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="87005-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="87005-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="87005-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="87005-627">Les informations de la chaîne d’erreur ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="87005-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="87005-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="87005-628">S_OK</span></span>  <br/> |<span data-ttu-id="87005-629">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="87005-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="87005-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="87005-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="87005-631">Cette interface fournit une fonction de rappel à l’objet COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="87005-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="87005-632">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="87005-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="87005-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="87005-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="87005-634">Il s’agit d’une fonction de rappel sur l’objet donné à l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="87005-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="87005-635">Il est prévu que lorsqu’un événement se produit (voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour des types d’événement valide), l’objet COM CsiSyncClient appeler cette méthode, le consommateur de signalisation.</span><span class="sxs-lookup"><span data-stu-id="87005-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="87005-636">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87005-636">Parameters</span></span>

 <span data-ttu-id="87005-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="87005-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="87005-638">Le type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="87005-638">The event type of this event.</span></span> <span data-ttu-id="87005-639">Voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="87005-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="87005-640">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="87005-640">Return values</span></span>

<span data-ttu-id="87005-641">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="87005-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="87005-642">Énumérations</span><span class="sxs-lookup"><span data-stu-id="87005-642">Enumerations</span></span>

<span data-ttu-id="87005-643">CSISyncClient utilise les énumérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="87005-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="87005-644">Énumération LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="87005-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="87005-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-645"></span></span>

<span data-ttu-id="87005-646">Cette énumération spécifie les catégories d’erreurs qui peuvent se produire lors de la synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="87005-647">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="87005-647">Enumerator</span></span>|<span data-ttu-id="87005-648">Description</span><span class="sxs-lookup"><span data-stu-id="87005-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="87005-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="87005-650">L’erreur de synchronisation de cet événement était inattendu et peut nécessiter une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="87005-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="87005-651">Par défaut, l’utilisateur peut avoir à intervenir.</span><span class="sxs-lookup"><span data-stu-id="87005-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="87005-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="87005-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="87005-653">L’erreur de synchronisation de cet événement ne doit pas une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="87005-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="87005-654">Office il gère automatiquement.</span><span class="sxs-lookup"><span data-stu-id="87005-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="87005-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="87005-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="87005-656">L’erreur de synchronisation de cet événement requiert un utilisateur pour le résoudre.</span><span class="sxs-lookup"><span data-stu-id="87005-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="87005-657">Par exemple, erreur de conflit de fusion requiert un utilisateur ouvrir le document et les fusionner.</span><span class="sxs-lookup"><span data-stu-id="87005-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="87005-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="87005-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="87005-659">L’erreur de synchronisation de cet événement requiert le consommateur intervenir, mais ne nécessitent ne pas une attention particulière par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="87005-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="87005-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="87005-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="87005-661">L’erreur de synchronisation de cet événement requiert le consommateur intervenir comme un cas spécial.</span><span class="sxs-lookup"><span data-stu-id="87005-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="87005-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="87005-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="87005-663">Énumération LSCEventType</span><span class="sxs-lookup"><span data-stu-id="87005-663">Enum LSCEventType</span></span>
<span data-ttu-id="87005-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-664"></span></span>

<span data-ttu-id="87005-665">Cette énumération spécifie le type d’événements qui peut se produire pour un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="87005-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="87005-666">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="87005-666">Enumerator</span></span>|<span data-ttu-id="87005-667">Description</span><span class="sxs-lookup"><span data-stu-id="87005-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="87005-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="87005-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="87005-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="87005-670">Modifications apportées à un fichier local.</span><span class="sxs-lookup"><span data-stu-id="87005-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="87005-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="87005-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="87005-672">Un utilisateur ouvre un fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="87005-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="87005-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="87005-674">Terminé le téléchargement des modifications de fichiers à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="87005-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="87005-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="87005-676">Terminé le téléchargement des modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="87005-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="87005-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="87005-678">L’état de conflit de fusion d’un fichier a changé.</span><span class="sxs-lookup"><span data-stu-id="87005-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="87005-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="87005-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="87005-680">Un fichier a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="87005-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="87005-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="87005-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="87005-682">Un fichier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="87005-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="87005-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="87005-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="87005-684">Synchronisation a été activée pour les fichiers d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="87005-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="87005-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="87005-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="87005-686">Démarrer le téléchargement des modifications de fichiers à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="87005-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="87005-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="87005-688">Démarrer le téléchargement des modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="87005-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="87005-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="87005-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="87005-690">Cet événement est généré lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque un conflit de chemin d’accès Web ou le chemin d’accès Local avec un autre fichier dans le Cache de fichiers Office.</span><span class="sxs-lookup"><span data-stu-id="87005-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="87005-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="87005-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="87005-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="87005-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="87005-693">Énumération LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="87005-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="87005-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-694"></span></span>

<span data-ttu-id="87005-695">Cette énumération spécifie le type des événements qui peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="87005-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="87005-696">Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="87005-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="87005-697">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="87005-697">Enumerator</span></span>|<span data-ttu-id="87005-698">Description</span><span class="sxs-lookup"><span data-stu-id="87005-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="87005-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="87005-700">Un ILSCEvent s’est produite.</span><span class="sxs-lookup"><span data-stu-id="87005-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="87005-701">Le consommateur doit appeler [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour extraire les données.</span><span class="sxs-lookup"><span data-stu-id="87005-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="87005-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="87005-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="87005-703">Les extensions de fichier prises en charge ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="87005-703">The supported file extensions have changed.</span></span> <span data-ttu-id="87005-704">Le consommateur doit appeler [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="87005-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="87005-705">Énumération LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="87005-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="87005-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-706"></span></span>

<span data-ttu-id="87005-707">Cette énumération spécifie les indicateurs utilisés pour une heuristique de coût du réseau.</span><span class="sxs-lookup"><span data-stu-id="87005-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="87005-708">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="87005-708">Enumerator</span></span>|<span data-ttu-id="87005-709">Description</span><span class="sxs-lookup"><span data-stu-id="87005-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="87005-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="87005-711">True si l’heuristique coût pour les réseaux coûteux (par exemple, 3 G) est remplacé.</span><span class="sxs-lookup"><span data-stu-id="87005-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="87005-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="87005-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="87005-713">True si l’heuristique coût consommation d’énergie (par exemple, une batterie) est remplacé.</span><span class="sxs-lookup"><span data-stu-id="87005-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="87005-714">Énumération LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="87005-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="87005-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="87005-715"></span></span>

<span data-ttu-id="87005-716">Cette énumération est utilisée pour représenter l’état de synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="87005-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="87005-717">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="87005-717">Enumerator</span></span>|<span data-ttu-id="87005-718">Description</span><span class="sxs-lookup"><span data-stu-id="87005-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="87005-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="87005-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="87005-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="87005-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="87005-721">True si les données à envoyer au fichier du serveur en attente.</span><span class="sxs-lookup"><span data-stu-id="87005-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="87005-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="87005-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="87005-723">True si les données à télécharger à partir du fichier de serveur en attente.</span><span class="sxs-lookup"><span data-stu-id="87005-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="87005-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="87005-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="87005-725">True si les données Office sur le fichier dans son cache est la plus récente copie des données sur le disque.</span><span class="sxs-lookup"><span data-stu-id="87005-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

