---
title: Utilisation de CSISyncClient pour contrôler le cache Office document (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Découvrez comment utiliser CSISyncClient pour contrôler le cache Office document (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346255"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="0915e-103">Utilisation de CSISyncClient pour contrôler le cache Office document (ODC)</span><span class="sxs-lookup"><span data-stu-id="0915e-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="0915e-104">Découvrez comment utiliser CSISyncClient pour contrôler le cache Office document (ODC).</span><span class="sxs-lookup"><span data-stu-id="0915e-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="0915e-105">CSISyncClient est un serveur COM hors processus (CsiSyncClient.exe) qui permet aux Microsoft OneDrive de contrôler le comportement du cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="0915e-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="0915e-106">Par exemple, OneDrive peut appeler l’ODC via CSISyncClient pour télécharger des fichiers vers et depuis des points de terminaison MS-FSSHTTP activés.</span><span class="sxs-lookup"><span data-stu-id="0915e-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="0915e-107">Cela permet d’activer des fonctionnalités avancées de service Office, telles que la co-auteur et les transitions transparentes de hors connexion à en ligne.</span><span class="sxs-lookup"><span data-stu-id="0915e-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="0915e-108">CsiSyncClient est disponible dans Office bureau (x86 et x64).</span><span class="sxs-lookup"><span data-stu-id="0915e-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="0915e-109">Remarque : bien que les versions plus récentes de Office soient disponibles avec CsiSyncClient, le processus sera utilisé uniquement pour la compatibilité avec les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="0915e-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="0915e-110">L’interface CsiSyncClient et la méthodologie de contrôle de l’ODC changeront dans les futures versions de Office.</span><span class="sxs-lookup"><span data-stu-id="0915e-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="0915e-111">L’ID de classe est actuellement définie pour répondre uniquement aux OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0915e-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="0915e-112">L’objet COM est utilisable en tant que serveur COM hors processus et s’exécute dans CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="0915e-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="0915e-113">En raison des limitations liées à Access (que l’ODC utilise), il est livré avec le type de bits que Office entre, donc x64 Office signifie un objet COM x64, ou x86 Office signifie un objet COM x86.</span><span class="sxs-lookup"><span data-stu-id="0915e-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="0915e-114">Pour contourner cette limitation, en spécifiant CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance, l’objet COM sera hébergé en tant que serveur COM hors processus, ce qui permettra la compatibilité entre bits.</span><span class="sxs-lookup"><span data-stu-id="0915e-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="0915e-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="0915e-115">Interfaces</span></span>

<span data-ttu-id="0915e-116">CSISyncClient utilise les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="0915e-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="0915e-117">Interface ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="0915e-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="0915e-118">Il s’agit de l’interface principale utilisée pour synchroniser les fichiers dans Office.</span><span class="sxs-lookup"><span data-stu-id="0915e-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="0915e-119">ProgID : Office. LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="0915e-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="0915e-120">CLSID : {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="0915e-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="0915e-121">TypeLib : {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="0915e-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="0915e-122">L’objet COM exposé est utilisé comme serveur hors processus.</span><span class="sxs-lookup"><span data-stu-id="0915e-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="0915e-123">Spécifier CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet la compatibilité entre les processus 64bits et 32bits.</span><span class="sxs-lookup"><span data-stu-id="0915e-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="0915e-124">Une fois que vous avez co-créé l’objet COM, vous devez d’abord appeler [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="0915e-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="0915e-125">Une [fois qu’ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) s’est terminé correctement, vous pouvez appeler n’importe quelle API aussi souvent que vous le souhaitez et dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="0915e-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="0915e-126">Vous pouvez également appeler [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="0915e-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="0915e-127">Les exceptions au paragraphe précédent sont [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="0915e-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="0915e-128">Après avoir appelé [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l’objet COM, vous devez détruire cet objet et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="0915e-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="0915e-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprime votre sous-cache, supprime toutes les informations de fichier associées dans le cache, mais laisse les documents sur le disque.</span><span class="sxs-lookup"><span data-stu-id="0915e-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="0915e-130">Il laisse également l’état intact pour communiquer avec le cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="0915e-131">Cela vous permet d’appeler [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) à nouveau pour créer un cache sans avoir à détruire et recréer l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="0915e-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="0915e-132">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="0915e-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="0915e-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="0915e-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="0915e-134">DeleteFile est utilisé pour supprimer les informations de fichier du cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="0915e-135">Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="0915e-136">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-136">Parameters</span></span>

 <span data-ttu-id="0915e-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="0915e-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="0915e-138">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="0915e-139">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-140">Return values</span></span>

|<span data-ttu-id="0915e-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-141">Value</span></span>|<span data-ttu-id="0915e-142">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-144">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-146">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-148">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="0915e-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="0915e-150">Le ResourceID donné n’est pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-152">Initialize has not been successfully called in the past.</span><span class="sxs-lookup"><span data-stu-id="0915e-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="0915e-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="0915e-154">Le fichier est actuellement synchronisé ou ouvert et ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="0915e-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="0915e-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-155">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-156">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="0915e-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="0915e-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="0915e-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="0915e-159">GetChanges renvoie un éumérateur d’objets ILSCEvent et renvoie également un jeton qui est donné à l’appel suivant à GetChanges, en supposant que le consommateur a traitée l’ensemble d’événements précédent.</span><span class="sxs-lookup"><span data-stu-id="0915e-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="0915e-160">Les événements  _avant le nPreviousChangesToken_ spécifié sont supprimés et indisponibles.</span><span class="sxs-lookup"><span data-stu-id="0915e-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="0915e-161">S’il n’existe aucun événement à traiter,  _pnCurrentChangesToken_ doit avoir la même valeur que  _nPreviousChangesToken,_ mais  _ppiEvents_ sera toujours définie.</span><span class="sxs-lookup"><span data-stu-id="0915e-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="0915e-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-162">Parameters</span></span>

 <span data-ttu-id="0915e-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="0915e-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="0915e-164">Identifie l’événement qui a été le dernier traitement par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="0915e-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="0915e-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="0915e-166">Identifie l’événement le plus récent remis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="0915e-167">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-167">Must not be null.</span></span>
  
 <span data-ttu-id="0915e-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="0915e-168">_ppiEvents_</span></span>
  
<span data-ttu-id="0915e-169">Un éumérateur pour les événements transmis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="0915e-170">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-171">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-171">Return values</span></span>

|<span data-ttu-id="0915e-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-172">Value</span></span>|<span data-ttu-id="0915e-173">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-175">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-177">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-180">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-181">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="0915e-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="0915e-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="0915e-183">GetClientNetworkSyncPermission est utilisé pour demander si la synchronisation heuristique de Office pour l’utilisation du coût et de l’alimentation du réseau est override.</span><span class="sxs-lookup"><span data-stu-id="0915e-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="0915e-184">Lorsqu’il est sur un réseau 3G ou un autre réseau à coût élevé, ou lorsqu’il est en cours d’exécution sur batterie ou qu’il est branché, Office peut choisir de bloquer le trafic réseau jusqu’à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="0915e-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="0915e-185">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-185">Parameters</span></span>

 <span data-ttu-id="0915e-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="0915e-186">_nspType_</span></span>
  
<span data-ttu-id="0915e-187">Indicateur qui définit le coût heuristique à interroger.</span><span class="sxs-lookup"><span data-stu-id="0915e-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="0915e-188">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="0915e-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="0915e-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="0915e-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="0915e-190">Spécifie si l’heuristique de coût demandée est actuellement ou non.</span><span class="sxs-lookup"><span data-stu-id="0915e-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="0915e-191">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-192">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-192">Return values</span></span>

|<span data-ttu-id="0915e-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-193">Value</span></span>|<span data-ttu-id="0915e-194">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-196">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-198">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-201">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-202">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="0915e-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="0915e-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="0915e-204">GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique : s’il existe dans le cache, s’il est en attente de communication avec la copie sur le serveur et si Office 2013 dispose des données les plus à jour de la copie locale.</span><span class="sxs-lookup"><span data-stu-id="0915e-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="0915e-205">Il nécessite un indicateur au niveau du bit des [valeurs Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations que l’objet COM CsiSyncClient doit interroger.</span><span class="sxs-lookup"><span data-stu-id="0915e-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="0915e-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-206">Parameters</span></span>

 <span data-ttu-id="0915e-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="0915e-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="0915e-208">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="0915e-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="0915e-209">Cette valeur doit être non vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="0915e-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="0915e-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="0915e-211">Indicateur qui définit les informations à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="0915e-211">A flag which defines what information to return.</span></span> <span data-ttu-id="0915e-212">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="0915e-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="0915e-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="0915e-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="0915e-214">Chaîne qui identifie l’emplacement du fichier identifié par  _bstrResourceID_ sur le client.</span><span class="sxs-lookup"><span data-stu-id="0915e-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="0915e-215">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-215">Must not be null.</span></span> 
  
 <span data-ttu-id="0915e-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="0915e-216">_pbstrETag_</span></span>
  
<span data-ttu-id="0915e-217">Chaîne qui contiendra l’eTag pour le fichier identifié par  _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="0915e-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="0915e-218">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-218">Must not be null.</span></span> 
  
 <span data-ttu-id="0915e-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="0915e-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="0915e-220">Indicateur qui contiendra l’état demandé via  _sfRequestedStatus_ pour le fichier identifié par  _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="0915e-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="0915e-221">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-221">Must not be null.</span></span> <span data-ttu-id="0915e-222">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="0915e-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-223">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-223">Return values</span></span>

|<span data-ttu-id="0915e-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-224">Value</span></span>|<span data-ttu-id="0915e-225">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-227">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-229">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="0915e-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="0915e-231">Les informations de fichier spécifiées par  _bstrResourceID_ n’existent pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0915e-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="0915e-233">LSCStatusFlag_LocalFileUnchanged a été demandé ou le fichier spécifié par  _bstrResourceID_ est verrouillé ou manquant.</span><span class="sxs-lookup"><span data-stu-id="0915e-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="0915e-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-236">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-237">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="0915e-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="0915e-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="0915e-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="0915e-240">GetSupportedFileExtensions renvoie une liste des extensions de fichier délimitées par des pipelines qui sont actuellement pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="0915e-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="0915e-241">Notez que cette liste peut changer et que le consommateur est informé d’une modification via l’objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured).</span><span class="sxs-lookup"><span data-stu-id="0915e-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="0915e-242">Voici un exemple de chaîne renvoyée : « |docx|docm|pptx| »</span><span class="sxs-lookup"><span data-stu-id="0915e-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="0915e-243">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-243">Parameters</span></span>

 <span data-ttu-id="0915e-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="0915e-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="0915e-245">Chaîne à définir avec un ensemble délimité par des pipelines d’extensions de fichier pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="0915e-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="0915e-246">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-247">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-247">Return values</span></span>

|<span data-ttu-id="0915e-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-248">Value</span></span>|<span data-ttu-id="0915e-249">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-251">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-253">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-256">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-257">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="0915e-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="0915e-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="0915e-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="0915e-260">Initialize doit être la première méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="0915e-260">Initialize must be the first method called.</span></span> <span data-ttu-id="0915e-261">Dans le cas contraire, toutes les autres API retournent E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="0915e-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="0915e-262">L’appel d’Initialize sur un objet déjà initialisé renvoie S_OK et ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="0915e-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="0915e-263">Si E_LSC_CACHEMISMATCH est renvoyé, l’appelant peut appeler [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé à l’suppliedID donné.</span><span class="sxs-lookup"><span data-stu-id="0915e-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="0915e-264">Toutefois, dans ce cas, d’autres API retournent toujours E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="0915e-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="0915e-265">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-265">Parameters</span></span>

 <span data-ttu-id="0915e-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="0915e-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="0915e-267">Identifie le consommateur et le cache à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0915e-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="0915e-268">Doit être non vide avec un maximum de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="0915e-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="0915e-269">_bstrProgID_</span></span>
  
<span data-ttu-id="0915e-270">Identifie l’objet COM du consommateur pour la communication double.</span><span class="sxs-lookup"><span data-stu-id="0915e-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="0915e-271">Doit être non vide avec un maximum de 39 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="0915e-272">Pour plus d’informations sur les ProgID, voir Clé [ \< ProgID. \> ](https://docs.microsoft.com/windows/desktop/com/-progid--key)</span><span class="sxs-lookup"><span data-stu-id="0915e-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="0915e-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="0915e-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="0915e-274">Identifie la racine du répertoire dans lequel les fichiers locaux seront stockés.</span><span class="sxs-lookup"><span data-stu-id="0915e-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="0915e-275">Doit être non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="0915e-276">Le répertoire doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="0915e-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="0915e-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="0915e-277">_pEventCallback_</span></span>
  
<span data-ttu-id="0915e-278">Interface de rappel que CsiSyncClient notifiera des modifications.</span><span class="sxs-lookup"><span data-stu-id="0915e-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="0915e-279">Voir IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="0915e-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="0915e-280">Cette valeur ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="0915e-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="0915e-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="0915e-282">Renvoie si un nouveau cache a été créé.</span><span class="sxs-lookup"><span data-stu-id="0915e-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="0915e-283">Si aucun cache n’est associé au SuppliedID, un cache est créé.</span><span class="sxs-lookup"><span data-stu-id="0915e-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="0915e-284">Cette valeur ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-285">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-285">Return values</span></span>

|<span data-ttu-id="0915e-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-286">Value</span></span>|<span data-ttu-id="0915e-287">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-289">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-291">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="0915e-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="0915e-293">Un ID Fourni est déjà associé à un cache, mais possède un ProgId ou FileSystemDirectoryHint différent de celui fourni.</span><span class="sxs-lookup"><span data-stu-id="0915e-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="0915e-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="0915e-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="0915e-295">FileSystemDirectoryHint (ou un sous-dossier) existe déjà sur un autre cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="0915e-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="0915e-297">Le ProgID existe déjà sur un autre cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-298">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-299">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="0915e-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="0915e-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="0915e-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="0915e-302">LocalFileChange est utilisé pour indiquer à l’objet COM CsiSyncClient de tenter de télécharger le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="0915e-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="0915e-303">La méthode prépare le fichier pour le chargement, y compris la lecture du contenu actuel du fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="0915e-304">Si un chargement est déjà en attente, le chargement précédent est ignoré et le nouveau contenu est préparé pour le chargement.</span><span class="sxs-lookup"><span data-stu-id="0915e-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="0915e-305">Si le fichier est ouvert pour modification dans une application, cette méthode retourne S_OK sans préparer le fichier pour téléchargement (l’application doit déjà faire cette étape en cas de modifications).</span><span class="sxs-lookup"><span data-stu-id="0915e-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="0915e-306">Cette méthode autorise les téléchargements s’il a été marqué comme téléchargements bloqués précédemment (voir [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="0915e-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="0915e-307">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-307">Parameters</span></span>

 <span data-ttu-id="0915e-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="0915e-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="0915e-309">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="0915e-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="0915e-310">Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="0915e-311">Ce chemin d’accès doit se trouver dans l’arborescence du répertoire spécifiée par FileSystemDirectoryHint lorsque l’appel à [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué.</span><span class="sxs-lookup"><span data-stu-id="0915e-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="0915e-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="0915e-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="0915e-313">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="0915e-314">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="0915e-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="0915e-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="0915e-316">Chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="0915e-317">Cette valeur doit être une URL non vide et valide, mais ne doit pas INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="0915e-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-318">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-318">Return values</span></span>

|<span data-ttu-id="0915e-319">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-319">Value</span></span>|<span data-ttu-id="0915e-320">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-322">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-324">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="0915e-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="0915e-326">Le fichier spécifié par  _bstrFileSystemPath_ présente un ID de ressource différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="0915e-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="0915e-327">Un événement de type LSCEventType_OnFilePathConflict envoyé lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="0915e-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="0915e-328">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="0915e-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="0915e-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="0915e-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="0915e-330">Le fichier a été supprimé en milieu d’opération.</span><span class="sxs-lookup"><span data-stu-id="0915e-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="0915e-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="0915e-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="0915e-332">L’extension de fichier donnée n’est pas prise en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="0915e-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="0915e-333">Voir [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="0915e-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="0915e-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="0915e-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="0915e-335">L’objet COM n’a pas programmé de chargement, car le fichier dans le cache a connu les modifications les plus récentes à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="0915e-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="0915e-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0915e-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="0915e-337">Le fichier spécifié par  _bstrFileSystemPath_ est manquant ou verrouillé.</span><span class="sxs-lookup"><span data-stu-id="0915e-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="0915e-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="0915e-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="0915e-339">L’objet FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="0915e-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="0915e-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="0915e-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="0915e-343">Le fichier spécifié par  _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="0915e-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="0915e-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="0915e-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="0915e-345">Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="0915e-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="0915e-347">WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="0915e-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-348">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-349">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="0915e-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="0915e-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="0915e-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="0915e-352">RenameFile associera une nouvelle URL et un chemin local pour un ResourceID donné.</span><span class="sxs-lookup"><span data-stu-id="0915e-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="0915e-353">Si le fichier spécifié par ResourceID n’existe pas déjà dans le cache, une tentative de création et de marque pour téléchargement est réalisée.</span><span class="sxs-lookup"><span data-stu-id="0915e-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="0915e-354">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-354">Parameters</span></span>

 <span data-ttu-id="0915e-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="0915e-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="0915e-356">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="0915e-357">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="0915e-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="0915e-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="0915e-359">Chaîne qui spécifie le nouveau chemin d’accès local pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="0915e-360">Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="0915e-361">Ce chemin d’accès doit se trouver dans l’arborescence du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="0915e-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="0915e-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="0915e-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="0915e-363">Chaîne qui spécifie la nouvelle URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="0915e-364">Cette valeur doit être une URL valide non vide, mais ne doit pas INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="0915e-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="0915e-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="0915e-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="0915e-366">Spécifie si les téléchargements vers le nouvel emplacement sont actuellement autorisés.</span><span class="sxs-lookup"><span data-stu-id="0915e-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-367">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-367">Return values</span></span>

|<span data-ttu-id="0915e-368">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-368">Value</span></span>|<span data-ttu-id="0915e-369">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-371">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-373">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="0915e-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="0915e-375">_BstrNewFileSystemPath_ ou _bstrNewWebPath_ existent déjà sur un autre fichier dans n’importe quel cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="0915e-376">Un événement de type LSCEventType_OnFilePathConflict envoyé lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="0915e-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="0915e-377">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="0915e-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="0915e-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="0915e-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="0915e-379">Les informations de fichier ont été supprimées du cache pendant l’exécution de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0915e-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="0915e-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="0915e-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="0915e-381">L’objet FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="0915e-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="0915e-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="0915e-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="0915e-385">Le fichier spécifié est actuellement synchronisé dans une application Office’application.</span><span class="sxs-lookup"><span data-stu-id="0915e-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="0915e-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-386">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-387">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="0915e-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="0915e-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="0915e-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="0915e-390">ResetCache supprime le cache associé au SuppliedID fourni lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="0915e-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="0915e-391">Cela inclut toutes les informations de fichier, mais laisse les fichiers à la fois sur le client et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="0915e-392">Cette méthode laisse également l’objet dans un état partiellement nonnitialisé.</span><span class="sxs-lookup"><span data-stu-id="0915e-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="0915e-393">Les seuls appels valides après cela sont [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="0915e-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="0915e-394">Cette méthode PEUT être appelée si Initialize échoue et renvoie E_LSC_CACHEMISMATCH et supprime le cache associé à l’suppliedID fourni avec l’appel qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="0915e-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="0915e-395">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0915e-395">Parameters</span></span>

<span data-ttu-id="0915e-396">Aucun</span><span class="sxs-lookup"><span data-stu-id="0915e-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-397">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-397">Return values</span></span>

|<span data-ttu-id="0915e-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-398">Value</span></span>|<span data-ttu-id="0915e-399">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-401">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="0915e-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-404">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-405">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="0915e-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="0915e-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="0915e-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="0915e-408">ServerFileChange indique à l’objet COM CsiSyncClient de marquer le fichier spécifié pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="0915e-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="0915e-409">Si le fichier est ouvert dans une application Office pour modification, cette méthode retourne S_OK sans marquer le fichier pour téléchargement (l’application doit déjà faire cette étape en cas de modifications).</span><span class="sxs-lookup"><span data-stu-id="0915e-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="0915e-410">Cette méthode autorise les téléchargements s’il a été marqué comme téléchargements bloqués précédemment (voir RenameFile).</span><span class="sxs-lookup"><span data-stu-id="0915e-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="0915e-411">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0915e-411">Parameters</span></span>

|<span data-ttu-id="0915e-412">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0915e-412">Parameter</span></span>|<span data-ttu-id="0915e-413">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="0915e-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="0915e-415">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="0915e-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="0915e-416">Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="0915e-417">Ce chemin d’accès doit se trouver dans l’arborescence du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="0915e-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="0915e-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="0915e-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="0915e-419">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="0915e-420">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="0915e-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="0915e-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="0915e-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="0915e-422">Chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="0915e-423">Cette valeur doit être une URL valide non vide, mais ne doit pas INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="0915e-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="0915e-424">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-424">Return values</span></span>

|<span data-ttu-id="0915e-425">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-425">Value</span></span>|<span data-ttu-id="0915e-426">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-428">Échec de la mise en place de l’état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="0915e-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="0915e-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="0915e-430">Le fichier spécifié par  _bstrFileSystemPath_ présente un ID de ressource différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="0915e-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="0915e-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="0915e-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="0915e-432">L’extension de fichier donnée n’est pas prise en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="0915e-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="0915e-433">Voir GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="0915e-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="0915e-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="0915e-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="0915e-435">Le fichier a été supprimé en milieu d’opération.</span><span class="sxs-lookup"><span data-stu-id="0915e-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="0915e-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-437">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="0915e-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="0915e-439">L’objet FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="0915e-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="0915e-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="0915e-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="0915e-443">Le fichier spécifié par  _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="0915e-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="0915e-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="0915e-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="0915e-445">Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="0915e-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="0915e-447">WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="0915e-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-448">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-449">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="0915e-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="0915e-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="0915e-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="0915e-452">Définit le cache dans un état en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="0915e-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="0915e-453">S’il est hors connexion, Office ne tente pas de communiquer avec le serveur pour les fichiers de ce cache, quel que soit le paramètre _fBlockUploads_ de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="0915e-454">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-454">Parameters</span></span>

 <span data-ttu-id="0915e-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="0915e-455">_fIsOnline_</span></span>
  
<span data-ttu-id="0915e-456">Booléen déterminant l’état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-457">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-457">Return values</span></span>

|<span data-ttu-id="0915e-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-458">Value</span></span>|<span data-ttu-id="0915e-459">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-461">Échec de la mise en place de l’état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="0915e-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="0915e-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-463">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-466">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-467">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="0915e-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="0915e-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="0915e-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="0915e-470">SetClientNetworkSyncPermission est utilisé pour remplacer ou restaurer l’heuristique de synchronisation d’Office pour l’utilisation du coût et de l’alimentation du réseau.</span><span class="sxs-lookup"><span data-stu-id="0915e-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="0915e-471">Lorsqu’il est sur un réseau 3G ou un autre réseau à coût élevé, ou lorsqu’il est en cours d’exécution sur batterie ou qu’il est branché, Office peut choisir de bloquer le trafic réseau jusqu’à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="0915e-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="0915e-472">Le consommateur de cette API peut l’utiliser pour remplacer Office’heuristique et forcer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="0915e-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="0915e-473">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-473">Parameters</span></span>

 <span data-ttu-id="0915e-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="0915e-474">_nspType_</span></span>
  
<span data-ttu-id="0915e-475">Indicateur qui définit le coût heuristique à remplacer.</span><span class="sxs-lookup"><span data-stu-id="0915e-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="0915e-476">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="0915e-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="0915e-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="0915e-477">_fEnableSync_</span></span>
  
<span data-ttu-id="0915e-478">Spécifie s’il faut forcer la synchronisation, en remplacement de ce coût heuristique, ou de ne plus la remplacer.</span><span class="sxs-lookup"><span data-stu-id="0915e-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-479">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-479">Return values</span></span>

|<span data-ttu-id="0915e-480">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-480">Value</span></span>|<span data-ttu-id="0915e-481">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-483">Échec du remplacement de la synchronisation heuristique.</span><span class="sxs-lookup"><span data-stu-id="0915e-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="0915e-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-486">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-487">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="0915e-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="0915e-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="0915e-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="0915e-490">Décharge le cache de l’objet COM et effectue des opérations de fermeture.</span><span class="sxs-lookup"><span data-stu-id="0915e-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="0915e-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelé avant la destruction de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="0915e-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="0915e-492">Une fois appelé, aucune autre API ne peut être appelée, l’objet COM DOIT être détruit et un nouvel objet créé si vous souhaitez poursuivre les opérations.</span><span class="sxs-lookup"><span data-stu-id="0915e-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="0915e-493">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0915e-493">Parameters</span></span>

<span data-ttu-id="0915e-494">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0915e-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-495">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-495">Return values</span></span>

|<span data-ttu-id="0915e-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-496">Value</span></span>|<span data-ttu-id="0915e-497">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-499">Échec de l’uninitialisation.</span><span class="sxs-lookup"><span data-stu-id="0915e-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="0915e-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0915e-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="0915e-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="0915e-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="0915e-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-502">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-503">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="0915e-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="0915e-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="0915e-505">Cette interface représente une liste d’événements ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="0915e-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="0915e-506">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="0915e-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="0915e-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="0915e-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="0915e-508">Extrait l’événement suivant de la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="0915e-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="0915e-509">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-509">Parameters</span></span>

 <span data-ttu-id="0915e-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="0915e-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="0915e-511">Pointeur vers une interface ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="0915e-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-512">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-512">Return values</span></span>

|<span data-ttu-id="0915e-513">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-513">Value</span></span>|<span data-ttu-id="0915e-514">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-516">Il n’y a plus d’événements.</span><span class="sxs-lookup"><span data-stu-id="0915e-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="0915e-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-517">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-518">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="0915e-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="0915e-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="0915e-520">Réinitialise l’éumérateur au premier événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="0915e-521">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0915e-521">Parameters</span></span>

<span data-ttu-id="0915e-522">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0915e-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-523">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-523">Return values</span></span>

<span data-ttu-id="0915e-524">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="0915e-525">Interface ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="0915e-525">Interface ILSCEvent</span></span>

<span data-ttu-id="0915e-526">Cette interface représente un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="0915e-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="0915e-527">Toutes les informations sur l’événement peuvent être récupérées à partir de l’interface.</span><span class="sxs-lookup"><span data-stu-id="0915e-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="0915e-528">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="0915e-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="0915e-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="0915e-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="0915e-530">Notez que cette valeur est remplie lorsque [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, et non lorsque l’événement a été créé, vous n’aurez donc que l’état actuel du fichier, et non l’état du fichier lorsque l’état du conflit a changé.</span><span class="sxs-lookup"><span data-stu-id="0915e-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="0915e-531">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="0915e-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="0915e-532">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-532">Parameters</span></span>

 <span data-ttu-id="0915e-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="0915e-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="0915e-534">État actuel du conflit du fichier associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-535">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-535">Return values</span></span>

<span data-ttu-id="0915e-536">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="0915e-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="0915e-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="0915e-538">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="0915e-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="0915e-539">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-539">Parameters</span></span>

 <span data-ttu-id="0915e-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="0915e-540">_pnError_</span></span>
  
<span data-ttu-id="0915e-541">Erreur associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-542">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-542">Return values</span></span>

<span data-ttu-id="0915e-543">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="0915e-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="0915e-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="0915e-545">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="0915e-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="0915e-546">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-546">Parameters</span></span>

 <span data-ttu-id="0915e-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="0915e-547">_pbstrETag_</span></span>
  
<span data-ttu-id="0915e-548">ETag associé à cet événement</span><span class="sxs-lookup"><span data-stu-id="0915e-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-549">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-549">Return values</span></span>

<span data-ttu-id="0915e-550">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="0915e-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="0915e-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="0915e-552">Obtient le type de cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="0915e-553">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-553">Parameters</span></span>

 <span data-ttu-id="0915e-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="0915e-554">_pnEventType_</span></span>
  
<span data-ttu-id="0915e-555">Type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-555">The event type of this event.</span></span> <span data-ttu-id="0915e-556">Voir [Enum LSCEventType pour les](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="0915e-557">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-558">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-558">Return values</span></span>

|<span data-ttu-id="0915e-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-559">Value</span></span>|<span data-ttu-id="0915e-560">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-562">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-563">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-564">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="0915e-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="0915e-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="0915e-566">Obtient le chemin d’accès de travail local pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="0915e-567">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-567">Parameters</span></span>

 <span data-ttu-id="0915e-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="0915e-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="0915e-569">Chemin d’accès local du fichier auquel appartient cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-570">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-570">Return values</span></span>

<span data-ttu-id="0915e-571">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="0915e-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="0915e-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="0915e-573">Obtient l’ID de ressource pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="0915e-574">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-574">Parameters</span></span>

 <span data-ttu-id="0915e-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="0915e-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="0915e-576">ResourceID du fichier associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="0915e-577">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-577">Return values</span></span>

<span data-ttu-id="0915e-578">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="0915e-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="0915e-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="0915e-580">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="0915e-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="0915e-581">Lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoquerait une collision de chemin Web ou de chemin local avec un autre fichier dans le cache de fichiers Office, cet événement est généré.</span><span class="sxs-lookup"><span data-stu-id="0915e-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="0915e-582">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-582">Parameters</span></span>

 <span data-ttu-id="0915e-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="0915e-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="0915e-584">ResourceID à l’origine de la générer.</span><span class="sxs-lookup"><span data-stu-id="0915e-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="0915e-585">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-586">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-586">Return values</span></span>

<span data-ttu-id="0915e-587">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="0915e-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="0915e-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="0915e-589">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="0915e-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="0915e-590">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-590">Parameters</span></span>

 <span data-ttu-id="0915e-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="0915e-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="0915e-592">Type d’erreur associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-592">The error type associated with this event.</span></span> <span data-ttu-id="0915e-593">Voir [Enum LSCEventType pour](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) les valeurs potentielles.</span><span class="sxs-lookup"><span data-stu-id="0915e-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="0915e-594">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-595">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-595">Return values</span></span>

|<span data-ttu-id="0915e-596">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-596">Value</span></span>|<span data-ttu-id="0915e-597">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-599">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-600">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-601">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="0915e-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="0915e-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="0915e-603">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="0915e-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="0915e-604">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-604">Parameters</span></span>

 <span data-ttu-id="0915e-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="0915e-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="0915e-606">Spécifie le chemin d’accès Web associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="0915e-607">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-608">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-608">Return values</span></span>

<span data-ttu-id="0915e-609">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="0915e-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="0915e-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="0915e-611">Cette interface contient des informations supplémentaires sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="0915e-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="0915e-612">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="0915e-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="0915e-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="0915e-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="0915e-614">Obtient les informations de chaîne d’erreur sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="0915e-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="0915e-615">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-615">Parameters</span></span>

 <span data-ttu-id="0915e-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="0915e-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="0915e-617">Chaîne qui doit contenir les informations de la chaîne d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0915e-617">A string to hold the error chain information.</span></span> <span data-ttu-id="0915e-618">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="0915e-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-619">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-619">Return values</span></span>

|<span data-ttu-id="0915e-620">Valeur</span><span class="sxs-lookup"><span data-stu-id="0915e-620">Value</span></span>|<span data-ttu-id="0915e-621">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="0915e-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="0915e-623">La version installée de Office ne prend pas en charge cette interface</span><span class="sxs-lookup"><span data-stu-id="0915e-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="0915e-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0915e-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0915e-625">Une ou plusieurs valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="0915e-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0915e-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="0915e-627">Les informations sur la chaîne d’erreur ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="0915e-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="0915e-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="0915e-628">S_OK</span></span>  <br/> |<span data-ttu-id="0915e-629">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0915e-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="0915e-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="0915e-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="0915e-631">Cette interface fournit une fonction de rappel à l’objet COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="0915e-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="0915e-632">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="0915e-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="0915e-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="0915e-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="0915e-634">Il s’agit d’une fonction de rappel sur l’objet donné à l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="0915e-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="0915e-635">Lorsqu’un événement se produit (voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les types d’événements valides), l’objet COM CsiSyncClient appellera cette méthode, ce qui aura pour effet d’insérable le consommateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="0915e-636">Parameters</span><span class="sxs-lookup"><span data-stu-id="0915e-636">Parameters</span></span>

 <span data-ttu-id="0915e-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="0915e-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="0915e-638">Type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-638">The event type of this event.</span></span> <span data-ttu-id="0915e-639">Voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="0915e-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="0915e-640">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0915e-640">Return values</span></span>

<span data-ttu-id="0915e-641">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="0915e-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="0915e-642">Énumérations</span><span class="sxs-lookup"><span data-stu-id="0915e-642">Enumerations</span></span>

<span data-ttu-id="0915e-643">CSISyncClient utilise les éumérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="0915e-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="0915e-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="0915e-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="0915e-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="0915e-646">Cette éumération spécifie les catégories d’erreurs qui peuvent se produire lors de la synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="0915e-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="0915e-647">Enumerator</span></span>|<span data-ttu-id="0915e-648">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="0915e-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="0915e-650">L’erreur de synchronisation de cet événement était inattendue et peut nécessiter une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="0915e-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="0915e-651">Par défaut, l’utilisateur peut être dans l’obligation d’intervenir.</span><span class="sxs-lookup"><span data-stu-id="0915e-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="0915e-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="0915e-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="0915e-653">L’erreur de synchronisation de cet événement n’a pas besoin d’être prise en compte.</span><span class="sxs-lookup"><span data-stu-id="0915e-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="0915e-654">Office le gérera automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0915e-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="0915e-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="0915e-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="0915e-656">L’erreur de synchronisation de cet événement nécessite qu’un utilisateur le résolve.</span><span class="sxs-lookup"><span data-stu-id="0915e-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="0915e-657">Par exemple, une erreur de conflit de fusion nécessite qu’un utilisateur ouvre le document et le fusionne.</span><span class="sxs-lookup"><span data-stu-id="0915e-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="0915e-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="0915e-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="0915e-659">L’erreur de synchronisation de cet événement oblige le consommateur à intervenir, mais ne doit pas nécessiter une attention particulière de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="0915e-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="0915e-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="0915e-661">L’erreur de synchronisation de cet événement oblige le consommateur à intervenir en tant que cas particulier.</span><span class="sxs-lookup"><span data-stu-id="0915e-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="0915e-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="0915e-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="0915e-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="0915e-663">Enum LSCEventType</span></span>
<span data-ttu-id="0915e-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="0915e-665">Cette éumération spécifie le type d’événements qui peuvent se produire pour un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="0915e-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="0915e-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="0915e-666">Enumerator</span></span>|<span data-ttu-id="0915e-667">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="0915e-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="0915e-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="0915e-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="0915e-670">Des modifications ont été apportées à un fichier local.</span><span class="sxs-lookup"><span data-stu-id="0915e-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="0915e-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="0915e-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="0915e-672">Un utilisateur a ouvert un fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="0915e-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="0915e-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="0915e-674">Fin du téléchargement des modifications de fichier à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="0915e-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="0915e-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="0915e-676">Fin du téléchargement des modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="0915e-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="0915e-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="0915e-678">L’état de conflit de fusion d’un fichier a changé.</span><span class="sxs-lookup"><span data-stu-id="0915e-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="0915e-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="0915e-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="0915e-680">Un fichier a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="0915e-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="0915e-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="0915e-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="0915e-682">Un fichier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="0915e-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="0915e-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="0915e-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="0915e-684">La synchronisation a été activée pour les fichiers d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0915e-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="0915e-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="0915e-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="0915e-686">Commencé à télécharger les modifications de fichier à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="0915e-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="0915e-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="0915e-688">Commencé à charger les modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="0915e-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="0915e-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="0915e-690">Cet événement est généré lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque une collision entre le chemin Web ou le chemin local avec un autre fichier dans le cache de fichiers Office.</span><span class="sxs-lookup"><span data-stu-id="0915e-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="0915e-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="0915e-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="0915e-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="0915e-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="0915e-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="0915e-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="0915e-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="0915e-695">Cette éumération spécifie le type d’événements qui peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="0915e-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="0915e-696">Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="0915e-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="0915e-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="0915e-697">Enumerator</span></span>|<span data-ttu-id="0915e-698">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="0915e-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="0915e-700">Un événement ILSCEvent s’est produit.</span><span class="sxs-lookup"><span data-stu-id="0915e-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="0915e-701">Le consommateur doit appeler [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="0915e-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="0915e-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="0915e-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="0915e-703">Les extensions de fichier pris en charge ont changé.</span><span class="sxs-lookup"><span data-stu-id="0915e-703">The supported file extensions have changed.</span></span> <span data-ttu-id="0915e-704">Le consommateur doit appeler [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0915e-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="0915e-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="0915e-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="0915e-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="0915e-707">Cette éumération spécifie les indicateurs utilisés pour une heuristique de coût réseau.</span><span class="sxs-lookup"><span data-stu-id="0915e-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="0915e-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="0915e-708">Enumerator</span></span>|<span data-ttu-id="0915e-709">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="0915e-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="0915e-711">Cette valeur a la valeur True si le coût heuristique des réseaux coûteux (tels que 3G) est bas prix.</span><span class="sxs-lookup"><span data-stu-id="0915e-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="0915e-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="0915e-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="0915e-713">Cette valeur a la valeur True si le coût heuristique de l’utilisation de l’alimentation (par exemple, une batterie) est bas prix.</span><span class="sxs-lookup"><span data-stu-id="0915e-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="0915e-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="0915e-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="0915e-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="0915e-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="0915e-716">Cette éumération est utilisée pour représenter l’état de synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="0915e-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="0915e-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="0915e-717">Enumerator</span></span>|<span data-ttu-id="0915e-718">Description</span><span class="sxs-lookup"><span data-stu-id="0915e-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915e-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="0915e-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="0915e-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="0915e-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="0915e-721">True s’il existe des données en attente à envoyer au fichier serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="0915e-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="0915e-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="0915e-723">True s’il existe des données en attente à télécharger à partir du fichier serveur.</span><span class="sxs-lookup"><span data-stu-id="0915e-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="0915e-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="0915e-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="0915e-725">Cette valeur a la valeur True Office données présentes sur le fichier dans son cache est la copie la plus récente des données sur disque.</span><span class="sxs-lookup"><span data-stu-id="0915e-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

