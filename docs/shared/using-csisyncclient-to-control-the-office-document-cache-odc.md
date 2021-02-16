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
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="805a9-103">Utilisation de CSISyncClient pour contrôler le cache de documents Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="805a9-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="805a9-104">Découvrez comment utiliser CSISyncClient pour contrôler le cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="805a9-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="805a9-105">CSISyncClient est un serveur COM hors processus (CsiSyncClient.exe) qui permet à Microsoft OneDrive de contrôler le comportement du cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="805a9-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="805a9-106">Par exemple, OneDrive peut appeler l’ODC via CSISyncClient pour télécharger des fichiers vers et depuis des points de terminaison MS-FSSHTTP activés.</span><span class="sxs-lookup"><span data-stu-id="805a9-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="805a9-107">Cela permet d’activer des fonctionnalités avancées de service dans Office, telles que la co-auteur et les transitions transparentes de hors connexion à en ligne.</span><span class="sxs-lookup"><span data-stu-id="805a9-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="805a9-108">CsiSyncClient est disponible dans Bureau Office (x86 et x64).</span><span class="sxs-lookup"><span data-stu-id="805a9-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="805a9-109">Remarque : bien que les versions plus récentes d’Office soient disponibles avec CsiSyncClient, le processus est utilisé uniquement pour la compatibilité avec les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="805a9-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="805a9-110">L’interface CsiSyncClient et la méthodologie de contrôle de l’ODC changeront dans les futures versions d’Office.</span><span class="sxs-lookup"><span data-stu-id="805a9-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="805a9-111">L’ID de classe est actuellement définie pour répondre uniquement à OneDrive.</span><span class="sxs-lookup"><span data-stu-id="805a9-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="805a9-112">L’objet COM est utilisable en tant que serveur COM hors processus et s’exécute dans CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="805a9-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="805a9-113">En raison des limitations liées à Access (que l’ODC utilise), il est livré avec le type de bits qu’Office entre, donc x64 Office signifie un objet COM x64, ou x86 Office signifie un objet COM x86.</span><span class="sxs-lookup"><span data-stu-id="805a9-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="805a9-114">Pour contourner cette limitation, en spécifiant CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance, l’objet COM sera hébergé en tant que serveur COM hors processus, ce qui permettra la compatibilité entre bits.</span><span class="sxs-lookup"><span data-stu-id="805a9-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="805a9-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="805a9-115">Interfaces</span></span>

<span data-ttu-id="805a9-116">CSISyncClient utilise les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="805a9-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="805a9-117">Interface ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="805a9-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="805a9-118">Il s’agit de l’interface principale utilisée pour synchroniser des fichiers dans Office.</span><span class="sxs-lookup"><span data-stu-id="805a9-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="805a9-119">ProgID : Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="805a9-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="805a9-120">CLSID : {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="805a9-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="805a9-121">TypeLib : {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="805a9-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="805a9-122">L’objet COM exposé est utilisé comme serveur hors processus.</span><span class="sxs-lookup"><span data-stu-id="805a9-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="805a9-123">Spécifier CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet la compatibilité entre les processus 64bits et 32bits.</span><span class="sxs-lookup"><span data-stu-id="805a9-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="805a9-124">Une fois que vous avez co-créé l’objet COM, vous devez d’abord appeler [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="805a9-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="805a9-125">Une [fois qu’ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) s’est terminé correctement, vous pouvez appeler n’importe quelle API aussi souvent que vous le souhaitez et dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="805a9-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="805a9-126">Vous pouvez également appeler [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="805a9-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="805a9-127">Les exceptions au paragraphe précédent sont [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="805a9-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="805a9-128">Après avoir appelé [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l’objet COM, vous devez détruire cet objet et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="805a9-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="805a9-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprime votre sous-cache, supprime toutes les informations de fichier associées dans le cache, mais laisse les documents sur le disque.</span><span class="sxs-lookup"><span data-stu-id="805a9-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="805a9-130">Il laisse également l’état intact pour communiquer avec le cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="805a9-131">Cela vous permet d’appeler à nouveau [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) pour créer un cache sans avoir à détruire et recréer l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="805a9-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="805a9-132">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="805a9-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="805a9-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="805a9-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="805a9-134">DeleteFile est utilisé pour supprimer les informations de fichier du cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="805a9-135">Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="805a9-136">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-136">Parameters</span></span>

 <span data-ttu-id="805a9-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="805a9-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="805a9-138">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="805a9-139">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-140">Return values</span></span>

|<span data-ttu-id="805a9-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-141">Value</span></span>|<span data-ttu-id="805a9-142">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-144">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-146">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-148">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="805a9-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="805a9-150">Le ResourceID donné n’est pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-152">Initialize has not been successfully called in the past.</span><span class="sxs-lookup"><span data-stu-id="805a9-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="805a9-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="805a9-154">Le fichier est actuellement synchronisé ou ouvert et ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="805a9-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="805a9-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-155">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-156">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="805a9-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="805a9-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="805a9-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="805a9-159">GetChanges renvoie un éumérateur d’objets ILSCEvent et renvoie également un jeton qui est donné à l’appel suivant à GetChanges, en supposant que le consommateur a traitée l’ensemble d’événements précédent.</span><span class="sxs-lookup"><span data-stu-id="805a9-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="805a9-160">Les événements  _avant le nPreviousChangesToken_ spécifié sont supprimés et indisponibles.</span><span class="sxs-lookup"><span data-stu-id="805a9-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="805a9-161">S’il n’existe aucun événement à traiter,  _pnCurrentChangesToken_ doit avoir la même valeur que  _nPreviousChangesToken,_ mais  _ppiEvents_ sera toujours définie.</span><span class="sxs-lookup"><span data-stu-id="805a9-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="805a9-162">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-162">Parameters</span></span>

 <span data-ttu-id="805a9-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="805a9-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="805a9-164">Identifie l’événement qui a été le dernier traitement par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="805a9-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="805a9-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="805a9-166">Identifie l’événement le plus récent remis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="805a9-167">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-167">Must not be null.</span></span>
  
 <span data-ttu-id="805a9-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="805a9-168">_ppiEvents_</span></span>
  
<span data-ttu-id="805a9-169">Un éumérateur pour les événements transmis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="805a9-170">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-171">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-171">Return values</span></span>

|<span data-ttu-id="805a9-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-172">Value</span></span>|<span data-ttu-id="805a9-173">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-175">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-177">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-180">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-181">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="805a9-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="805a9-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="805a9-183">GetClientNetworkSyncPermission est utilisé pour demander si les heuristiques de synchronisation d’Office pour l’utilisation du coût et de l’alimentation du réseau sont overrides.</span><span class="sxs-lookup"><span data-stu-id="805a9-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="805a9-184">Lorsqu’il est sur un réseau 3G ou un autre réseau à coût élevé, ou lorsqu’il est en cours d’exécution sur batterie ou branché, Office peut choisir de bloquer le trafic réseau jusqu’à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="805a9-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="805a9-185">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-185">Parameters</span></span>

 <span data-ttu-id="805a9-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="805a9-186">_nspType_</span></span>
  
<span data-ttu-id="805a9-187">Indicateur qui définit le coût heuristique à interroger.</span><span class="sxs-lookup"><span data-stu-id="805a9-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="805a9-188">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="805a9-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="805a9-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="805a9-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="805a9-190">Spécifie si le coût heuristique demandé est actuellement ou non pris en compte.</span><span class="sxs-lookup"><span data-stu-id="805a9-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="805a9-191">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-192">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-192">Return values</span></span>

|<span data-ttu-id="805a9-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-193">Value</span></span>|<span data-ttu-id="805a9-194">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-196">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-198">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-201">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-202">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="805a9-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="805a9-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="805a9-204">GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique : s’il existe dans le cache, s’il est en attente de communication avec la copie sur le serveur et si Office 2013 dispose des données les plus à jour de la copie locale.</span><span class="sxs-lookup"><span data-stu-id="805a9-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="805a9-205">Il nécessite un indicateur de bits de [valeurs Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations que l’objet COM CsiSyncClient doit interroger.</span><span class="sxs-lookup"><span data-stu-id="805a9-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="805a9-206">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-206">Parameters</span></span>

 <span data-ttu-id="805a9-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="805a9-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="805a9-208">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="805a9-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="805a9-209">Cette valeur doit être non vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="805a9-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="805a9-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="805a9-211">Indicateur qui définit les informations à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="805a9-211">A flag which defines what information to return.</span></span> <span data-ttu-id="805a9-212">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="805a9-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="805a9-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="805a9-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="805a9-214">Chaîne qui identifie l’emplacement du fichier identifié par  _bstrResourceID_ sur le client.</span><span class="sxs-lookup"><span data-stu-id="805a9-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="805a9-215">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-215">Must not be null.</span></span> 
  
 <span data-ttu-id="805a9-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="805a9-216">_pbstrETag_</span></span>
  
<span data-ttu-id="805a9-217">Chaîne qui contiendra l’eTag pour le fichier identifié par  _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="805a9-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="805a9-218">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-218">Must not be null.</span></span> 
  
 <span data-ttu-id="805a9-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="805a9-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="805a9-220">Indicateur qui contiendra l’état demandé via  _sfRequestedStatus_ pour le fichier identifié par  _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="805a9-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="805a9-221">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-221">Must not be null.</span></span> <span data-ttu-id="805a9-222">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="805a9-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-223">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-223">Return values</span></span>

|<span data-ttu-id="805a9-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-224">Value</span></span>|<span data-ttu-id="805a9-225">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-227">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-229">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="805a9-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="805a9-231">Les informations de fichier spécifiées par  _bstrResourceID_ n’existent pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="805a9-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="805a9-233">LSCStatusFlag_LocalFileUnchanged a été demandé ou le fichier spécifié par  _bstrResourceID_ est verrouillé ou manquant.</span><span class="sxs-lookup"><span data-stu-id="805a9-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="805a9-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-236">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-237">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="805a9-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="805a9-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="805a9-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="805a9-240">GetSupportedFileExtensions renvoie une liste des extensions de fichier délimitées par des pipelines qui sont actuellement pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="805a9-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="805a9-241">Notez que cette liste peut changer et que le consommateur est informé d’une modification via l’objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured).</span><span class="sxs-lookup"><span data-stu-id="805a9-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="805a9-242">Voici un exemple de chaîne renvoyée : « |docx|docm|pptx| »</span><span class="sxs-lookup"><span data-stu-id="805a9-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="805a9-243">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-243">Parameters</span></span>

 <span data-ttu-id="805a9-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="805a9-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="805a9-245">Chaîne à définir avec un ensemble délimité par des pipelines d’extensions de fichier pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="805a9-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="805a9-246">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-247">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-247">Return values</span></span>

|<span data-ttu-id="805a9-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-248">Value</span></span>|<span data-ttu-id="805a9-249">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-251">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-253">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-256">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-257">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="805a9-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="805a9-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="805a9-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="805a9-260">Initialize doit être la première méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="805a9-260">Initialize must be the first method called.</span></span> <span data-ttu-id="805a9-261">Dans le cas contraire, toutes les autres API retournent E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="805a9-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="805a9-262">L’appel d’Initialize sur un objet déjà initialisé renvoie S_OK et ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="805a9-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="805a9-263">Si E_LSC_CACHEMISMATCH est renvoyé, l’appelant peut appeler [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé à l’suppliedID donné.</span><span class="sxs-lookup"><span data-stu-id="805a9-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="805a9-264">Toutefois, dans ce cas, d’autres API retournent toujours E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="805a9-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="805a9-265">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-265">Parameters</span></span>

 <span data-ttu-id="805a9-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="805a9-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="805a9-267">Identifie le consommateur et le cache à utiliser.</span><span class="sxs-lookup"><span data-stu-id="805a9-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="805a9-268">Doit être non vide avec un maximum de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="805a9-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="805a9-269">_bstrProgID_</span></span>
  
<span data-ttu-id="805a9-270">Identifie l’objet COM du consommateur pour la communication double.</span><span class="sxs-lookup"><span data-stu-id="805a9-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="805a9-271">Doit être non vide avec un maximum de 39 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="805a9-272">Pour plus d’informations sur les ProgID, voir Clé [ \< ProgID. \> ](https://docs.microsoft.com/windows/desktop/com/-progid--key)</span><span class="sxs-lookup"><span data-stu-id="805a9-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="805a9-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="805a9-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="805a9-274">Identifie la racine du répertoire dans lequel les fichiers locaux seront stockés.</span><span class="sxs-lookup"><span data-stu-id="805a9-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="805a9-275">Doit être non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="805a9-276">Le répertoire doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="805a9-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="805a9-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="805a9-277">_pEventCallback_</span></span>
  
<span data-ttu-id="805a9-278">Interface de rappel que CsiSyncClient notifiera des modifications.</span><span class="sxs-lookup"><span data-stu-id="805a9-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="805a9-279">Voir IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="805a9-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="805a9-280">Cette valeur ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="805a9-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="805a9-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="805a9-282">Renvoie si un nouveau cache a été créé.</span><span class="sxs-lookup"><span data-stu-id="805a9-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="805a9-283">Si aucun cache n’est associé au SuppliedID, un cache est créé.</span><span class="sxs-lookup"><span data-stu-id="805a9-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="805a9-284">Cette valeur ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-285">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-285">Return values</span></span>

|<span data-ttu-id="805a9-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-286">Value</span></span>|<span data-ttu-id="805a9-287">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-289">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-291">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="805a9-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="805a9-293">Un ID Fourni est déjà associé à un cache, mais possède un ProgId ou FileSystemDirectoryHint différent de celui fourni.</span><span class="sxs-lookup"><span data-stu-id="805a9-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="805a9-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="805a9-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="805a9-295">FileSystemDirectoryHint (ou un sous-dossier) existe déjà sur un autre cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="805a9-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="805a9-297">Le ProgID existe déjà sur un autre cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-298">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-299">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="805a9-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="805a9-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="805a9-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="805a9-302">LocalFileChange est utilisé pour indiquer à l’objet COM CsiSyncClient de tenter de télécharger le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="805a9-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="805a9-303">La méthode prépare le fichier pour le chargement, y compris la lecture du contenu actuel du fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="805a9-304">Si un chargement est déjà en attente, le chargement précédent est ignoré et le nouveau contenu est préparé pour le chargement.</span><span class="sxs-lookup"><span data-stu-id="805a9-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="805a9-305">Si le fichier est ouvert pour modification dans une application, cette méthode retourne S_OK sans préparer le fichier pour le chargement (l’application doit déjà faire cette étape en cas de modifications).</span><span class="sxs-lookup"><span data-stu-id="805a9-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="805a9-306">Cette méthode autorise les téléchargements s’il a été marqué comme téléchargements bloqués précédemment (voir [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="805a9-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="805a9-307">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-307">Parameters</span></span>

 <span data-ttu-id="805a9-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="805a9-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="805a9-309">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="805a9-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="805a9-310">Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="805a9-311">Ce chemin d’accès doit se trouver dans l’arborescence du répertoire spécifiée par FileSystemDirectoryHint lorsque l’appel à [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué.</span><span class="sxs-lookup"><span data-stu-id="805a9-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="805a9-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="805a9-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="805a9-313">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="805a9-314">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="805a9-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="805a9-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="805a9-316">Chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="805a9-317">Cette valeur doit être une URL non vide et valide, mais ne doit pas INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="805a9-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-318">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-318">Return values</span></span>

|<span data-ttu-id="805a9-319">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-319">Value</span></span>|<span data-ttu-id="805a9-320">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-322">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-324">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="805a9-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="805a9-326">Le fichier spécifié par  _bstrFileSystemPath_ présente un ID de ressource différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="805a9-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="805a9-327">Un événement de type LSCEventType_OnFilePathConflict envoyé lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="805a9-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="805a9-328">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="805a9-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="805a9-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="805a9-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="805a9-330">Le fichier a été supprimé en milieu d’opération.</span><span class="sxs-lookup"><span data-stu-id="805a9-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="805a9-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="805a9-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="805a9-332">L’extension de fichier donnée n’est pas prise en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="805a9-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="805a9-333">Voir [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="805a9-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="805a9-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="805a9-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="805a9-335">L’objet COM n’a pas programmé de chargement, car le fichier dans le cache a connu les modifications les plus récentes à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="805a9-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="805a9-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="805a9-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="805a9-337">Le fichier spécifié par  _bstrFileSystemPath_ est manquant ou verrouillé.</span><span class="sxs-lookup"><span data-stu-id="805a9-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="805a9-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="805a9-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="805a9-339">L’objet FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="805a9-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="805a9-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="805a9-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="805a9-343">Le fichier spécifié par  _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="805a9-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="805a9-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="805a9-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="805a9-345">Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="805a9-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="805a9-347">WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="805a9-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-348">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-349">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="805a9-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="805a9-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="805a9-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="805a9-352">RenameFile associera une nouvelle URL et un chemin local pour un ResourceID donné.</span><span class="sxs-lookup"><span data-stu-id="805a9-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="805a9-353">Si le fichier spécifié par ResourceID n’existe pas déjà dans le cache, une tentative est réalisée pour le créer et le marquer pour téléchargement.</span><span class="sxs-lookup"><span data-stu-id="805a9-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="805a9-354">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-354">Parameters</span></span>

 <span data-ttu-id="805a9-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="805a9-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="805a9-356">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="805a9-357">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="805a9-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="805a9-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="805a9-359">Chaîne qui spécifie le nouveau chemin d’accès local pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="805a9-360">Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="805a9-361">Ce chemin d’accès doit se trouver dans l’arborescence du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="805a9-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="805a9-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="805a9-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="805a9-363">Chaîne qui spécifie la nouvelle URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="805a9-364">Cette valeur doit être une URL valide non vide, mais ne doit pas INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="805a9-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="805a9-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="805a9-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="805a9-366">Spécifie si les téléchargements vers le nouvel emplacement sont actuellement autorisés.</span><span class="sxs-lookup"><span data-stu-id="805a9-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-367">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-367">Return values</span></span>

|<span data-ttu-id="805a9-368">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-368">Value</span></span>|<span data-ttu-id="805a9-369">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-371">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-373">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="805a9-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="805a9-375">_BstrNewFileSystemPath_ ou _bstrNewWebPath_ existent déjà sur un autre fichier dans n’importe quel cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="805a9-376">Un événement de type LSCEventType_OnFilePathConflict envoyé lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="805a9-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="805a9-377">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="805a9-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="805a9-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="805a9-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="805a9-379">Les informations de fichier ont été supprimées du cache pendant l’exécution de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="805a9-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="805a9-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="805a9-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="805a9-381">L’objet FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="805a9-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="805a9-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="805a9-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="805a9-385">Le fichier spécifié est actuellement synchronisé dans une application Office.</span><span class="sxs-lookup"><span data-stu-id="805a9-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="805a9-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-386">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-387">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="805a9-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="805a9-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="805a9-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="805a9-390">ResetCache supprime le cache associé au SuppliedID fourni lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="805a9-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="805a9-391">Cela inclut toutes les informations de fichier, mais laisse les fichiers à la fois sur le client et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="805a9-392">Cette méthode laisse également l’objet dans un état partiellement nonnitialisé.</span><span class="sxs-lookup"><span data-stu-id="805a9-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="805a9-393">Les seuls appels valides après cela sont [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="805a9-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="805a9-394">Cette méthode PEUT être appelée si Initialize échoue et renvoie E_LSC_CACHEMISMATCH, et supprime le cache associé au SuppliedID fourni avec l’appel ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="805a9-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="805a9-395">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-395">Parameters</span></span>

<span data-ttu-id="805a9-396">Aucun</span><span class="sxs-lookup"><span data-stu-id="805a9-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-397">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-397">Return values</span></span>

|<span data-ttu-id="805a9-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-398">Value</span></span>|<span data-ttu-id="805a9-399">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-401">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="805a9-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-404">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-405">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="805a9-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="805a9-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="805a9-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="805a9-408">ServerFileChange indique à l’objet COM CsiSyncClient de marquer le fichier spécifié pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="805a9-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="805a9-409">Si le fichier est ouvert dans une application Office pour modification, cette méthode retourne S_OK sans marquer le fichier pour téléchargement (l’application doit déjà faire cette étape en cas de modifications).</span><span class="sxs-lookup"><span data-stu-id="805a9-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="805a9-410">Cette méthode autorise les téléchargements s’il a été marqué comme téléchargements bloqués précédemment (voir RenameFile).</span><span class="sxs-lookup"><span data-stu-id="805a9-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="805a9-411">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-411">Parameters</span></span>

|<span data-ttu-id="805a9-412">Paramètre</span><span class="sxs-lookup"><span data-stu-id="805a9-412">Parameter</span></span>|<span data-ttu-id="805a9-413">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="805a9-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="805a9-415">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="805a9-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="805a9-416">Cette valeur doit être un chemin local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="805a9-417">Ce chemin d’accès doit se trouver dans l’arborescence du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="805a9-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="805a9-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="805a9-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="805a9-419">Chaîne qui identifie l’resourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="805a9-420">Cette valeur doit être non vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="805a9-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="805a9-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="805a9-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="805a9-422">Chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="805a9-423">Cette valeur doit être une URL valide non vide, mais ne doit pas INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="805a9-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="805a9-424">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-424">Return values</span></span>

|<span data-ttu-id="805a9-425">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-425">Value</span></span>|<span data-ttu-id="805a9-426">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-428">Échec de la mise en place de l’état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="805a9-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="805a9-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="805a9-430">Le fichier spécifié par  _bstrFileSystemPath_ présente un ID de ressource différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="805a9-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="805a9-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="805a9-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="805a9-432">L’extension de fichier donnée n’est pas prise en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="805a9-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="805a9-433">Voir GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="805a9-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="805a9-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="805a9-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="805a9-435">Le fichier a été supprimé en milieu d’opération.</span><span class="sxs-lookup"><span data-stu-id="805a9-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="805a9-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-437">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="805a9-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="805a9-439">L’objet FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifiée par FileSystemDirectoryHint lors de l’appel à Initialize.</span><span class="sxs-lookup"><span data-stu-id="805a9-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="805a9-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="805a9-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="805a9-443">Le fichier spécifié par  _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="805a9-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="805a9-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="805a9-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="805a9-445">Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="805a9-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="805a9-447">WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="805a9-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-448">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-449">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="805a9-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="805a9-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="805a9-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="805a9-452">Définit le cache dans un état en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="805a9-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="805a9-453">En mode hors connexion, Office ne tentera pas de communiquer avec le serveur pour les fichiers de ce cache, quel que soit le paramètre  _fBlockUploads_ de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="805a9-454">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-454">Parameters</span></span>

 <span data-ttu-id="805a9-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="805a9-455">_fIsOnline_</span></span>
  
<span data-ttu-id="805a9-456">Booléen déterminant l’état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-457">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-457">Return values</span></span>

|<span data-ttu-id="805a9-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-458">Value</span></span>|<span data-ttu-id="805a9-459">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-461">Échec de la mise en place de l’état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="805a9-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="805a9-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-463">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-466">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-467">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="805a9-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="805a9-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="805a9-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="805a9-470">SetClientNetworkSyncPermission est utilisé pour remplacer ou restaurer l’heuristique de synchronisation d’Office pour l’utilisation du coût et de l’alimentation du réseau.</span><span class="sxs-lookup"><span data-stu-id="805a9-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="805a9-471">Lorsqu’il est sur un réseau 3G ou un autre réseau à coût élevé, ou lorsqu’il est en cours d’exécution sur batterie ou branché, Office peut choisir de bloquer le trafic réseau jusqu’à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="805a9-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="805a9-472">Le consommateur de cette API peut l’utiliser pour remplacer l’heuristique d’Office et forcer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="805a9-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="805a9-473">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-473">Parameters</span></span>

 <span data-ttu-id="805a9-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="805a9-474">_nspType_</span></span>
  
<span data-ttu-id="805a9-475">Indicateur qui définit le coût heuristique à remplacer.</span><span class="sxs-lookup"><span data-stu-id="805a9-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="805a9-476">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="805a9-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="805a9-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="805a9-477">_fEnableSync_</span></span>
  
<span data-ttu-id="805a9-478">Spécifie s’il faut forcer la synchronisation, en remplacement de ce coût heuristique, ou de ne plus la remplacer.</span><span class="sxs-lookup"><span data-stu-id="805a9-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-479">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-479">Return values</span></span>

|<span data-ttu-id="805a9-480">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-480">Value</span></span>|<span data-ttu-id="805a9-481">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-483">Échec du remplacement de la synchronisation heuristique.</span><span class="sxs-lookup"><span data-stu-id="805a9-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="805a9-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-486">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-487">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="805a9-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="805a9-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="805a9-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="805a9-490">Décharge le cache de l’objet COM et effectue des opérations de fermeture.</span><span class="sxs-lookup"><span data-stu-id="805a9-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="805a9-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelé avant la destruction de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="805a9-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="805a9-492">Une fois appelé, aucune autre API ne peut être appelée, l’objet COM DOIT être détruit et un nouvel objet créé si vous souhaitez poursuivre les opérations.</span><span class="sxs-lookup"><span data-stu-id="805a9-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="805a9-493">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-493">Parameters</span></span>

<span data-ttu-id="805a9-494">Aucun.</span><span class="sxs-lookup"><span data-stu-id="805a9-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-495">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-495">Return values</span></span>

|<span data-ttu-id="805a9-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-496">Value</span></span>|<span data-ttu-id="805a9-497">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-499">Échec de l’uninitialisation.</span><span class="sxs-lookup"><span data-stu-id="805a9-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="805a9-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="805a9-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="805a9-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="805a9-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="805a9-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-502">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-503">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="805a9-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="805a9-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="805a9-505">Cette interface représente une liste d’événements ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="805a9-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="805a9-506">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="805a9-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="805a9-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="805a9-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="805a9-508">Extrait l’événement suivant de la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="805a9-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="805a9-509">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-509">Parameters</span></span>

 <span data-ttu-id="805a9-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="805a9-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="805a9-511">Pointeur vers une interface ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="805a9-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-512">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-512">Return values</span></span>

|<span data-ttu-id="805a9-513">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-513">Value</span></span>|<span data-ttu-id="805a9-514">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-516">Il n’y a plus d’événements.</span><span class="sxs-lookup"><span data-stu-id="805a9-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="805a9-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-517">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-518">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="805a9-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="805a9-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="805a9-520">Réinitialise l’éumérateur au premier événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="805a9-521">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-521">Parameters</span></span>

<span data-ttu-id="805a9-522">Aucun.</span><span class="sxs-lookup"><span data-stu-id="805a9-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-523">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-523">Return values</span></span>

<span data-ttu-id="805a9-524">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="805a9-525">Interface ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="805a9-525">Interface ILSCEvent</span></span>

<span data-ttu-id="805a9-526">Cette interface représente un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="805a9-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="805a9-527">Toutes les informations sur l’événement peuvent être récupérées à partir de l’interface.</span><span class="sxs-lookup"><span data-stu-id="805a9-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="805a9-528">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="805a9-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="805a9-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="805a9-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="805a9-530">Notez que cette valeur est remplie lorsque [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, et non lorsque l’événement a été créé, vous n’aurez donc que l’état actuel du fichier, et non l’état du fichier lorsque l’état du conflit a changé.</span><span class="sxs-lookup"><span data-stu-id="805a9-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="805a9-531">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="805a9-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="805a9-532">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-532">Parameters</span></span>

 <span data-ttu-id="805a9-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="805a9-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="805a9-534">État actuel du conflit du fichier associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-535">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-535">Return values</span></span>

<span data-ttu-id="805a9-536">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="805a9-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="805a9-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="805a9-538">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="805a9-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="805a9-539">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-539">Parameters</span></span>

 <span data-ttu-id="805a9-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="805a9-540">_pnError_</span></span>
  
<span data-ttu-id="805a9-541">Erreur associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-542">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-542">Return values</span></span>

<span data-ttu-id="805a9-543">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="805a9-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="805a9-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="805a9-545">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="805a9-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="805a9-546">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-546">Parameters</span></span>

 <span data-ttu-id="805a9-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="805a9-547">_pbstrETag_</span></span>
  
<span data-ttu-id="805a9-548">ETag associé à cet événement</span><span class="sxs-lookup"><span data-stu-id="805a9-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-549">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-549">Return values</span></span>

<span data-ttu-id="805a9-550">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="805a9-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="805a9-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="805a9-552">Obtient le type de cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="805a9-553">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-553">Parameters</span></span>

 <span data-ttu-id="805a9-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="805a9-554">_pnEventType_</span></span>
  
<span data-ttu-id="805a9-555">Type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-555">The event type of this event.</span></span> <span data-ttu-id="805a9-556">Voir [Enum LSCEventType pour les](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="805a9-557">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-558">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-558">Return values</span></span>

|<span data-ttu-id="805a9-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-559">Value</span></span>|<span data-ttu-id="805a9-560">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-562">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-563">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-564">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="805a9-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="805a9-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="805a9-566">Obtient le chemin d’accès de travail local pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="805a9-567">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-567">Parameters</span></span>

 <span data-ttu-id="805a9-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="805a9-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="805a9-569">Chemin d’accès local du fichier auquel appartient cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-570">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-570">Return values</span></span>

<span data-ttu-id="805a9-571">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="805a9-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="805a9-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="805a9-573">Obtient l’ID de ressource pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="805a9-574">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-574">Parameters</span></span>

 <span data-ttu-id="805a9-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="805a9-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="805a9-576">ResourceID du fichier associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="805a9-577">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-577">Return values</span></span>

<span data-ttu-id="805a9-578">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="805a9-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="805a9-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="805a9-580">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="805a9-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="805a9-581">Lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoquerait une collision de chemin Web ou de chemin local avec un autre fichier dans le cache de fichiers Office, cet événement est généré.</span><span class="sxs-lookup"><span data-stu-id="805a9-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="805a9-582">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-582">Parameters</span></span>

 <span data-ttu-id="805a9-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="805a9-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="805a9-584">ResourceID qui a généré cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="805a9-585">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-586">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-586">Return values</span></span>

<span data-ttu-id="805a9-587">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="805a9-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="805a9-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="805a9-589">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="805a9-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="805a9-590">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-590">Parameters</span></span>

 <span data-ttu-id="805a9-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="805a9-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="805a9-592">Type d’erreur associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-592">The error type associated with this event.</span></span> <span data-ttu-id="805a9-593">Voir [Enum LSCEventType pour](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) les valeurs potentielles.</span><span class="sxs-lookup"><span data-stu-id="805a9-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="805a9-594">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-595">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-595">Return values</span></span>

|<span data-ttu-id="805a9-596">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-596">Value</span></span>|<span data-ttu-id="805a9-597">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-599">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-600">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-601">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="805a9-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="805a9-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="805a9-603">Cette valeur est remplie uniquement lorsque l’enum [LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="805a9-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="805a9-604">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-604">Parameters</span></span>

 <span data-ttu-id="805a9-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="805a9-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="805a9-606">Spécifie le chemin d’accès Web associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="805a9-607">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-608">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-608">Return values</span></span>

<span data-ttu-id="805a9-609">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="805a9-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="805a9-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="805a9-611">Cette interface contient des informations supplémentaires sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="805a9-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="805a9-612">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="805a9-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="805a9-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="805a9-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="805a9-614">Obtient les informations de chaîne d’erreur sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="805a9-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="805a9-615">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-615">Parameters</span></span>

 <span data-ttu-id="805a9-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="805a9-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="805a9-617">Chaîne qui doit contenir les informations de la chaîne d’erreur.</span><span class="sxs-lookup"><span data-stu-id="805a9-617">A string to hold the error chain information.</span></span> <span data-ttu-id="805a9-618">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="805a9-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-619">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-619">Return values</span></span>

|<span data-ttu-id="805a9-620">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a9-620">Value</span></span>|<span data-ttu-id="805a9-621">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="805a9-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="805a9-623">La version installée d’Office ne prend pas en charge cette interface</span><span class="sxs-lookup"><span data-stu-id="805a9-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="805a9-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="805a9-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="805a9-625">Une ou plusieurs valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="805a9-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="805a9-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="805a9-627">Les informations sur la chaîne d’erreur ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="805a9-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="805a9-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="805a9-628">S_OK</span></span>  <br/> |<span data-ttu-id="805a9-629">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="805a9-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="805a9-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="805a9-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="805a9-631">Cette interface fournit une fonction de rappel à l’objet COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="805a9-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="805a9-632">**Fonctions de membre public**</span><span class="sxs-lookup"><span data-stu-id="805a9-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="805a9-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="805a9-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="805a9-634">Il s’agit d’une fonction de rappel sur l’objet donné à l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="805a9-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="805a9-635">Lorsqu’un événement se produit (voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les types d’événements valides), l’objet COM CsiSyncClient appellera cette méthode, ce qui aura pour effet d’insérable le consommateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="805a9-636">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a9-636">Parameters</span></span>

 <span data-ttu-id="805a9-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="805a9-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="805a9-638">Type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-638">The event type of this event.</span></span> <span data-ttu-id="805a9-639">Voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="805a9-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="805a9-640">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="805a9-640">Return values</span></span>

<span data-ttu-id="805a9-641">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="805a9-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="805a9-642">Énumérations</span><span class="sxs-lookup"><span data-stu-id="805a9-642">Enumerations</span></span>

<span data-ttu-id="805a9-643">CSISyncClient utilise les éumérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="805a9-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="805a9-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="805a9-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="805a9-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="805a9-646">Cette éumération spécifie les catégories d’erreurs qui peuvent se produire lors de la synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="805a9-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="805a9-647">Enumerator</span></span>|<span data-ttu-id="805a9-648">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="805a9-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="805a9-650">L’erreur de synchronisation de cet événement était inattendue et peut nécessiter une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="805a9-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="805a9-651">Par défaut, l’utilisateur peut être dans l’obligation d’intervenir.</span><span class="sxs-lookup"><span data-stu-id="805a9-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="805a9-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="805a9-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="805a9-653">L’erreur de synchronisation de cet événement n’a pas besoin d’être prise en compte.</span><span class="sxs-lookup"><span data-stu-id="805a9-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="805a9-654">Office le gère automatiquement.</span><span class="sxs-lookup"><span data-stu-id="805a9-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="805a9-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="805a9-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="805a9-656">L’erreur de synchronisation de cet événement nécessite qu’un utilisateur le résolve.</span><span class="sxs-lookup"><span data-stu-id="805a9-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="805a9-657">Par exemple, une erreur de conflit de fusion nécessite qu’un utilisateur ouvre le document et le fusionne.</span><span class="sxs-lookup"><span data-stu-id="805a9-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="805a9-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="805a9-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="805a9-659">L’erreur de synchronisation de cet événement oblige le consommateur à intervenir, mais ne doit pas nécessiter une attention particulière de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="805a9-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="805a9-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="805a9-661">L’erreur de synchronisation de cet événement oblige le consommateur à intervenir en tant que cas particulier.</span><span class="sxs-lookup"><span data-stu-id="805a9-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="805a9-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="805a9-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="805a9-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="805a9-663">Enum LSCEventType</span></span>
<span data-ttu-id="805a9-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="805a9-665">Cette éumération spécifie le type d’événements qui peuvent se produire pour un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="805a9-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="805a9-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="805a9-666">Enumerator</span></span>|<span data-ttu-id="805a9-667">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="805a9-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="805a9-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="805a9-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="805a9-670">Des modifications ont été apportées à un fichier local.</span><span class="sxs-lookup"><span data-stu-id="805a9-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="805a9-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="805a9-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="805a9-672">Un utilisateur a ouvert un fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="805a9-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="805a9-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="805a9-674">Fin du téléchargement des modifications de fichier à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="805a9-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="805a9-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="805a9-676">Fin du téléchargement des modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="805a9-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="805a9-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="805a9-678">L’état de conflit de fusion d’un fichier a changé.</span><span class="sxs-lookup"><span data-stu-id="805a9-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="805a9-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="805a9-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="805a9-680">Un fichier a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="805a9-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="805a9-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="805a9-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="805a9-682">Un fichier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="805a9-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="805a9-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="805a9-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="805a9-684">La synchronisation a été activée pour les fichiers d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="805a9-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="805a9-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="805a9-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="805a9-686">Commencé à télécharger les modifications de fichier à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="805a9-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="805a9-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="805a9-688">Commencé à charger les modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="805a9-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="805a9-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="805a9-690">Cet événement est généré lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque une collision entre le chemin Web ou le chemin local avec un autre fichier dans le cache de fichiers Office.</span><span class="sxs-lookup"><span data-stu-id="805a9-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="805a9-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="805a9-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="805a9-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="805a9-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="805a9-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="805a9-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="805a9-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="805a9-695">Cette éumération spécifie le type d’événements qui peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="805a9-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="805a9-696">Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="805a9-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="805a9-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="805a9-697">Enumerator</span></span>|<span data-ttu-id="805a9-698">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="805a9-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="805a9-700">Un événement ILSCEvent s’est produit.</span><span class="sxs-lookup"><span data-stu-id="805a9-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="805a9-701">Le consommateur doit appeler [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="805a9-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="805a9-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="805a9-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="805a9-703">Les extensions de fichier pris en charge ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="805a9-703">The supported file extensions have changed.</span></span> <span data-ttu-id="805a9-704">Le consommateur doit appeler [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions pris en charge.</span><span class="sxs-lookup"><span data-stu-id="805a9-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="805a9-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="805a9-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="805a9-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="805a9-707">Cette éumération spécifie les indicateurs utilisés pour une heuristique de coût réseau.</span><span class="sxs-lookup"><span data-stu-id="805a9-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="805a9-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="805a9-708">Enumerator</span></span>|<span data-ttu-id="805a9-709">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="805a9-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="805a9-711">Cette valeur a la valeur True si le coût heuristique des réseaux coûteux (tels que 3G) est bas prix.</span><span class="sxs-lookup"><span data-stu-id="805a9-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="805a9-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="805a9-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="805a9-713">Cette valeur a la valeur True si le coût heuristique de l’utilisation de l’alimentation (par exemple, une batterie) est bas prix.</span><span class="sxs-lookup"><span data-stu-id="805a9-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="805a9-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="805a9-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="805a9-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="805a9-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="805a9-716">Cette éumération est utilisée pour représenter l’état de synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="805a9-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="805a9-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="805a9-717">Enumerator</span></span>|<span data-ttu-id="805a9-718">Description</span><span class="sxs-lookup"><span data-stu-id="805a9-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="805a9-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="805a9-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="805a9-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="805a9-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="805a9-721">True s’il existe des données en attente à envoyer au fichier serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="805a9-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="805a9-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="805a9-723">True s’il existe des données en attente à télécharger à partir du fichier serveur.</span><span class="sxs-lookup"><span data-stu-id="805a9-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="805a9-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="805a9-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="805a9-725">True si les données d’Office ont sur le fichier dans son cache est la copie la plus récente des données sur le disque.</span><span class="sxs-lookup"><span data-stu-id="805a9-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

