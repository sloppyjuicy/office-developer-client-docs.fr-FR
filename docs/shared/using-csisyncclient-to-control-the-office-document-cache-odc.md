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
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="339a2-103">Utilisation de CSISyncClient pour contrôler le cache de documents Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="339a2-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="339a2-104">Découvrez comment utiliser CSISyncClient pour contrôler le cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="339a2-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="339a2-105">CSISyncClient est un serveur COM out-of-proc (CsiSyncClient. exe) qui permet à Microsoft OneDrive de contrôler le comportement du cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="339a2-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="339a2-106">Par exemple, OneDrive peut appeler le ODC via CSISyncClient pour télécharger et télécharger des fichiers vers et à partir de points de terminaison compatibles avec MS FSSHTTP.</span><span class="sxs-lookup"><span data-stu-id="339a2-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="339a2-107">Cela permet d'activer les fonctionnalités avancées de service dans Office, telles que la co-création et les transitions transparentes de Offline vers Online.</span><span class="sxs-lookup"><span data-stu-id="339a2-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="339a2-108">CsiSyncClient est disponible dans Office Desktop (x86 et x64).</span><span class="sxs-lookup"><span data-stu-id="339a2-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="339a2-109">Remarque: tandis que les versions plus récentes d'Office peuvent être livrées avec CsiSyncClient, le processus sera utilisé uniquement à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="339a2-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="339a2-110">L'interface CsiSyncClient et la méthodologie de contrôle du ODC seront modifiées dans les versions ultérieures d'Office.</span><span class="sxs-lookup"><span data-stu-id="339a2-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="339a2-111">L'ID de classe est actuellement défini pour répondre uniquement à OneDrive.</span><span class="sxs-lookup"><span data-stu-id="339a2-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="339a2-112">L'objet COM est utilisable comme un serveur COM out-of-proc et s'exécute dans CsiSyncClient. exe.</span><span class="sxs-lookup"><span data-stu-id="339a2-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="339a2-113">En raison des limites liées à Access (que le service ODC utilise), il est fourni avec le type de bit qu'il contient, c'est pourquoi x64 Office signifie un objet COM x64, ou x86 Office signifie un objet COM x86.</span><span class="sxs-lookup"><span data-stu-id="339a2-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="339a2-114">Pour contourner cette limitation, la spécification de CLSCTX_LOCAL_SERVER dans le cadre de la fonction CoCreateInstance aura pour objet COM d'être hébergé en tant que serveur COM out-of-proc, ce qui permet la compatibilité entre les bits par tour.</span><span class="sxs-lookup"><span data-stu-id="339a2-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="339a2-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="339a2-115">Interfaces</span></span>

<span data-ttu-id="339a2-116">CSISyncClient utilise les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="339a2-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="339a2-117">Interface ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="339a2-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="339a2-118">Il s'agit de l'interface principale utilisée pour synchroniser les fichiers dans Office.</span><span class="sxs-lookup"><span data-stu-id="339a2-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="339a2-119">ProgID: Office. LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="339a2-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="339a2-120">CLSID: {14286318-B6CF-49A1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="339a2-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="339a2-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="339a2-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="339a2-122">L'objet COM qui est exposé est utilisé en tant que serveur out-of-proc.</span><span class="sxs-lookup"><span data-stu-id="339a2-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="339a2-123">La spécification de CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet la compatibilité entre les processus 64 bits et 32 bits.</span><span class="sxs-lookup"><span data-stu-id="339a2-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="339a2-124">Une fois que vous avez co-créé l'objet COM, vous devez appeler [d'abord ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="339a2-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="339a2-125">Une fois [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) s'est terminé avec succès, vous pouvez appeler n'importe quelle API autant de fois que vous le souhaitez et dans n'importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="339a2-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="339a2-126">Vous pouvez également appeler [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela n'a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="339a2-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="339a2-127">Les exceptions au paragraphe précédent sont [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="339a2-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="339a2-128">Une fois que vous avez appelé [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l'objet com, vous devez détruire cet objet et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="339a2-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="339a2-129">[ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprimera votre sous-cache, supprimez toutes les informations de fichier associées dans le cache, mais laissez les documents sur le disque.</span><span class="sxs-lookup"><span data-stu-id="339a2-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="339a2-130">Il laisse également l'état intact pour la communication avec le cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="339a2-131">Cela vous permet d'appeler [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) à nouveau pour créer un nouveau cache sans avoir à détruire et recréer l'objet com.</span><span class="sxs-lookup"><span data-stu-id="339a2-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="339a2-132">**Fonctions membres publiques**</span><span class="sxs-lookup"><span data-stu-id="339a2-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="339a2-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="339a2-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="339a2-134">DeleteFile est utilisé pour supprimer les informations de fichier du cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="339a2-135">Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="339a2-136">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-136">Parameters</span></span>

 <span data-ttu-id="339a2-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="339a2-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="339a2-138">La chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="339a2-139">Cette valeur ne doit pas être vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-140">Return values</span></span>

|<span data-ttu-id="339a2-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-141">Value</span></span>|<span data-ttu-id="339a2-142">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-144">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-146">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-148">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="339a2-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="339a2-150">Le ResourceID donné n'est pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-152">Initialize n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="339a2-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="339a2-154">Le fichier est en cours de synchronisation ou d'ouverture et ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="339a2-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="339a2-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-155">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-156">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="339a2-157">ILSCLocalSyncClient:: GetChanges</span><span class="sxs-lookup"><span data-stu-id="339a2-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="339a2-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-158"></span></span>

<span data-ttu-id="339a2-159">GetChanges renvoie un énumérateur d'objets ILSCEvent et renvoie également un jeton qui est attribué à l'appel suivant à GetChanges, en supposant que le consommateur a traité le jeu d'événements précédent.</span><span class="sxs-lookup"><span data-stu-id="339a2-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="339a2-160">Les événements précédant le _nPreviousChangesToken_ spécifié seront supprimés et indisponibles.</span><span class="sxs-lookup"><span data-stu-id="339a2-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="339a2-161">S'il n'y a aucun événement à traiter, _pnCurrentChangesToken_ doit avoir la même valeur que _NPreviousChangesToken_, mais _ppiEvents_ continuera à être défini.</span><span class="sxs-lookup"><span data-stu-id="339a2-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="339a2-162">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-162">Parameters</span></span>

 <span data-ttu-id="339a2-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="339a2-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="339a2-164">Identifie l'événement qui a été traité en dernier par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="339a2-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="339a2-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="339a2-166">Identifie l'événement le plus récent transmis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="339a2-167">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-167">Must not be null.</span></span>
  
 <span data-ttu-id="339a2-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="339a2-168">_ppiEvents_</span></span>
  
<span data-ttu-id="339a2-169">Un énumérateur pour les événements transmis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="339a2-170">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-171">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-171">Return values</span></span>

|<span data-ttu-id="339a2-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-172">Value</span></span>|<span data-ttu-id="339a2-173">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-175">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-177">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-179">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-180">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-181">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="339a2-182">ILSCLocalSyncClient:: GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="339a2-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="339a2-183">GetClientNetworkSyncPermission est utilisé pour demander si les heuristiques de synchronisation d'Office pour le coût réseau et la consommation d'énergie sont remplacées.</span><span class="sxs-lookup"><span data-stu-id="339a2-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="339a2-184">Lorsqu'il est connecté à un réseau 3G ou à un autre réseau à coût élevé, ou lorsqu'il fonctionne sur batterie ou qu'il est branché, Office peut choisir de bloquer le trafic réseau jusqu'à un temps plus opportun.</span><span class="sxs-lookup"><span data-stu-id="339a2-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="339a2-185">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-185">Parameters</span></span>

 <span data-ttu-id="339a2-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="339a2-186">_nspType_</span></span>
  
<span data-ttu-id="339a2-187">Indicateur qui définit le coût heuristique à interroger.</span><span class="sxs-lookup"><span data-stu-id="339a2-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="339a2-188">Voir [énumérAtion LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="339a2-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="339a2-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="339a2-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="339a2-190">Indique si la heuristique de coût demandée est actuellement remplacée ou non.</span><span class="sxs-lookup"><span data-stu-id="339a2-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="339a2-191">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-192">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-192">Return values</span></span>

|<span data-ttu-id="339a2-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-193">Value</span></span>|<span data-ttu-id="339a2-194">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-196">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-198">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-200">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-201">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-202">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="339a2-203">ILSCLocalSyncClient:: GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="339a2-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="339a2-204">GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique: s'il existe dans le cache, s'il est en attente de communication avec la copie du serveur et si Office 2013 a les données les plus à jour à partir de la copie locale.</span><span class="sxs-lookup"><span data-stu-id="339a2-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="339a2-205">Elle requiert un indicateur de bits des valeurs d' [énumérAtion LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations pour lesquelles l'objet com CsiSyncClient doit effectuer une requête.</span><span class="sxs-lookup"><span data-stu-id="339a2-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="339a2-206">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-206">Parameters</span></span>

 <span data-ttu-id="339a2-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="339a2-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="339a2-208">La chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="339a2-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="339a2-209">Cette valeur ne doit pas être vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="339a2-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="339a2-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="339a2-211">Indicateur qui définit les informations à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="339a2-211">A flag which defines what information to return.</span></span> <span data-ttu-id="339a2-212">Voir [énumérAtion LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="339a2-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="339a2-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="339a2-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="339a2-214">La chaîne qui identifie l'emplacement du fichier identifié par _bstrResourceID_ sur le client.</span><span class="sxs-lookup"><span data-stu-id="339a2-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="339a2-215">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-215">Must not be null.</span></span> 
  
 <span data-ttu-id="339a2-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="339a2-216">_pbstrETag_</span></span>
  
<span data-ttu-id="339a2-217">Chaîne qui contient l'eTag pour le fichier identifié par _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="339a2-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="339a2-218">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-218">Must not be null.</span></span> 
  
 <span data-ttu-id="339a2-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="339a2-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="339a2-220">Indicateur qui contiendra l'État demandé via _sfRequestedStatus_ pour le fichier identifié par _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="339a2-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="339a2-221">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-221">Must not be null.</span></span> <span data-ttu-id="339a2-222">Voir [énumérAtion LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="339a2-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-223">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-223">Return values</span></span>

|<span data-ttu-id="339a2-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-224">Value</span></span>|<span data-ttu-id="339a2-225">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-227">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-229">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="339a2-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="339a2-231">Les informations de fichier spécifiées par _bstrResourceID_ n'existent pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="339a2-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="339a2-233">LSCStatusFlag_LocalFileUnchanged a été demandé ou le fichier spécifié par _bstrResourceID_ est verrouillé ou manquant.</span><span class="sxs-lookup"><span data-stu-id="339a2-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="339a2-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-235">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-236">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-237">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="339a2-238">ILSCLocalSyncClient:: GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="339a2-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="339a2-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-239"></span></span>

<span data-ttu-id="339a2-240">GetSupportedFileExtensions renvoie une liste d'extensions de fichiers délimitées par des canaux qui sont actuellement prises en charge par l'objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="339a2-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="339a2-241">Notez que cette liste peut changer et que le consommateur est informé d'une modification via l'objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured).</span><span class="sxs-lookup"><span data-stu-id="339a2-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="339a2-242">Un exemple de la chaîne renvoyée est le suivant: "| docx | docm | pptx |"</span><span class="sxs-lookup"><span data-stu-id="339a2-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="339a2-243">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-243">Parameters</span></span>

 <span data-ttu-id="339a2-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="339a2-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="339a2-245">Chaîne à définir avec un jeu d'extensions de fichiers délimité par des canaux et pris en charge par l'objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="339a2-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="339a2-246">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-247">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-247">Return values</span></span>

|<span data-ttu-id="339a2-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-248">Value</span></span>|<span data-ttu-id="339a2-249">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-251">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-253">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-255">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-256">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-257">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="339a2-258">ILSCLocalSyncClient:: Initialize</span><span class="sxs-lookup"><span data-stu-id="339a2-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="339a2-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-259"></span></span>

<span data-ttu-id="339a2-260">Initialize doit être la première méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="339a2-260">Initialize must be the first method called.</span></span> <span data-ttu-id="339a2-261">Dans le cas contraire, toutes les autres API retournent E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="339a2-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="339a2-262">L'appel de la méthode Initialize sur un objet déjà initialisé renvoie S_OK et ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="339a2-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="339a2-263">Si E_LSC_CACHEMISMATCH est renvoyé, l'appelant peut appeler [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé au SuppliedID donné.</span><span class="sxs-lookup"><span data-stu-id="339a2-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="339a2-264">Toutefois, dans ce cas, d'autres API continuent de renvoyer E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="339a2-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="339a2-265">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-265">Parameters</span></span>

 <span data-ttu-id="339a2-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="339a2-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="339a2-267">Identifie le consommateur et le cache à utiliser.</span><span class="sxs-lookup"><span data-stu-id="339a2-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="339a2-268">Doit être vide avec un maximum de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="339a2-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="339a2-269">_bstrProgID_</span></span>
  
<span data-ttu-id="339a2-270">Identifie l'objet COM du consommateur pour la communication bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="339a2-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="339a2-271">Doit être vide avec un maximum de 39 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="339a2-272">Pour plus d'informations sur les ProgID, voir [ \<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) .</span><span class="sxs-lookup"><span data-stu-id="339a2-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="339a2-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="339a2-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="339a2-274">Identifie la racine du répertoire dans lequel les fichiers locaux seront stockés.</span><span class="sxs-lookup"><span data-stu-id="339a2-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="339a2-275">Doit être vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="339a2-276">Le répertoire doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="339a2-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="339a2-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="339a2-277">_pEventCallback_</span></span>
  
<span data-ttu-id="339a2-278">Interface de rappel que CsiSyncClient enverra sur les modifications.</span><span class="sxs-lookup"><span data-stu-id="339a2-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="339a2-279">Voir IPartnerActivityCallback:: EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="339a2-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="339a2-280">Cette valeur ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="339a2-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="339a2-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="339a2-282">Indique si un nouveau cache a été créé.</span><span class="sxs-lookup"><span data-stu-id="339a2-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="339a2-283">Si aucun cache n'est associé au SuppliedID, un cache est créé.</span><span class="sxs-lookup"><span data-stu-id="339a2-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="339a2-284">Cette valeur ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-285">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-285">Return values</span></span>

|<span data-ttu-id="339a2-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-286">Value</span></span>|<span data-ttu-id="339a2-287">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-289">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-291">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="339a2-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="339a2-293">Un SuppliedID est déjà associé à un cache, mais a un ProgId ou FileSystemDirectoryHint différent de ceux fournis.</span><span class="sxs-lookup"><span data-stu-id="339a2-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="339a2-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="339a2-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="339a2-295">Le FileSystemDirectoryHint (ou un sous-dossier) existe déjà dans un autre cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="339a2-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="339a2-297">Le ProgID existe déjà dans un autre cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-298">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-299">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="339a2-300">ILSCLocalSyncClient:: LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="339a2-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="339a2-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-301"></span></span>

<span data-ttu-id="339a2-302">LocalFileChange est utilisé pour indiquer à l'objet COM CsiSyncClient de tenter de télécharger le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="339a2-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="339a2-303">La méthode prépare le chargement du fichier, y compris la lecture du contenu actuel du fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="339a2-304">Si un chargement est déjà en attente, le téléchargement précédent est ignoré et le nouveau contenu préparé pour le chargement.</span><span class="sxs-lookup"><span data-stu-id="339a2-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="339a2-305">Si le fichier est ouvert pour modification dans une application, cette méthode renvoie S_OK sans préparer le fichier pour le chargement (l'application doit déjà effectuer cette étape s'il y a des modifications).</span><span class="sxs-lookup"><span data-stu-id="339a2-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="339a2-306">Cette méthode autorisera les téléchargements s'il a été marqué comme étant des téléchargements bloqués précédemment (voir [ILSCLocalSyncClient:: RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="339a2-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="339a2-307">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-307">Parameters</span></span>

 <span data-ttu-id="339a2-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="339a2-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="339a2-309">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="339a2-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="339a2-310">Cette valeur doit être un chemin d'accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="339a2-311">Ce chemin d'accès doit se trouver dans l'arborescence de répertoires spécifiée par l'FileSystemDirectoryHint lorsque l'appel à [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué.</span><span class="sxs-lookup"><span data-stu-id="339a2-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="339a2-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="339a2-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="339a2-313">Chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="339a2-314">Cette valeur ne doit pas être vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="339a2-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="339a2-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="339a2-316">Chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="339a2-317">Cette valeur doit être une URL non vide, valide, mais ne dépassant pas INTERNET_MAX_URL_LENGTH, comme défini https://support.microsoft.com/kb/208427par.</span><span class="sxs-lookup"><span data-stu-id="339a2-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-318">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-318">Return values</span></span>

|<span data-ttu-id="339a2-319">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-319">Value</span></span>|<span data-ttu-id="339a2-320">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-322">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-324">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="339a2-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="339a2-326">Le fichier spécifié par _bstrFileSystemPath_ a un ResourceId différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="339a2-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="339a2-327">Un événement de type LSCEventType_OnFilePathConflict est envoyé lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="339a2-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="339a2-328">Voir [ILSCLocalSyncClient:: GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="339a2-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="339a2-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="339a2-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="339a2-330">Le fichier a été supprimé au milieu des opérations.</span><span class="sxs-lookup"><span data-stu-id="339a2-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="339a2-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="339a2-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="339a2-332">L'extension de fichier donnée n'est pas prise en charge par l'objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="339a2-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="339a2-333">Voir [ILSCLocalSyncClient:: GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="339a2-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="339a2-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="339a2-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="339a2-335">L'objet COM n'a pas planifié de téléchargement, car le fichier dans le cache avait les modifications les plus récentes à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="339a2-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="339a2-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="339a2-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="339a2-337">Le fichier spécifié par _bstrFileSystemPath_ est manquant ou verrouillé.</span><span class="sxs-lookup"><span data-stu-id="339a2-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="339a2-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="339a2-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="339a2-339">Le FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifié par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.</span><span class="sxs-lookup"><span data-stu-id="339a2-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="339a2-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-341">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="339a2-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="339a2-343">Le fichier spécifié par _bstrResourceID_ a une FileSystemPath différente de celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="339a2-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="339a2-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="339a2-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="339a2-345">Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="339a2-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="339a2-347">Le chemin d'accès webPath fourni se trouve dans un autre cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-348">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-349">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="339a2-350">ILSCLocalSyncClient:: RenameFile</span><span class="sxs-lookup"><span data-stu-id="339a2-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="339a2-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-351"></span></span>

<span data-ttu-id="339a2-352">RenameFile associe une nouvelle URL et le chemin d'accès local d'un ResourceID donné.</span><span class="sxs-lookup"><span data-stu-id="339a2-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="339a2-353">Si le fichier spécifié par le ResourceID n'existe pas déjà dans le cache, une tentative est effectuée pour le créer et le marquer pour téléchargement.</span><span class="sxs-lookup"><span data-stu-id="339a2-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="339a2-354">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-354">Parameters</span></span>

 <span data-ttu-id="339a2-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="339a2-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="339a2-356">Chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="339a2-357">Cette valeur ne doit pas être vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="339a2-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="339a2-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="339a2-359">Valeur de type String qui spécifie le nouveau chemin d'accès local du fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="339a2-360">Cette valeur doit être un chemin d'accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="339a2-361">Ce chemin d'accès doit se trouver dans l'arborescence de répertoires spécifiée par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.</span><span class="sxs-lookup"><span data-stu-id="339a2-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="339a2-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="339a2-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="339a2-363">Valeur de type String qui spécifie la nouvelle URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="339a2-364">Cette valeur doit être une URL valide non vide, mais pas plus de INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="339a2-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="339a2-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="339a2-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="339a2-366">Indique si les téléchargements vers le nouvel emplacement sont autorisés actuellement.</span><span class="sxs-lookup"><span data-stu-id="339a2-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-367">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-367">Return values</span></span>

|<span data-ttu-id="339a2-368">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-368">Value</span></span>|<span data-ttu-id="339a2-369">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-371">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-373">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="339a2-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="339a2-375">Le _bstrNewFileSystemPath_ ou _bstrNewWebPath_ existe déjà dans un autre fichier dans n'importe quel cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="339a2-376">Un événement de type LSCEventType_OnFilePathConflict est envoyé lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="339a2-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="339a2-377">Voir [ILSCLocalSyncClient:: GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="339a2-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="339a2-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="339a2-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="339a2-379">Les informations de fichier ont été supprimées du cache pendant l'exécution de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="339a2-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="339a2-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="339a2-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="339a2-381">Le FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifié par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.</span><span class="sxs-lookup"><span data-stu-id="339a2-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="339a2-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-383">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="339a2-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="339a2-385">Le fichier spécifié est en cours de synchronisation dans une application Office.</span><span class="sxs-lookup"><span data-stu-id="339a2-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="339a2-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-386">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-387">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="339a2-388">ILSCLocalSyncClient:: ResetCache</span><span class="sxs-lookup"><span data-stu-id="339a2-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="339a2-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-389"></span></span>

<span data-ttu-id="339a2-390">ResetCache supprime le cache associé au SuppliedID qui a été fourni lors de l'initialisation.</span><span class="sxs-lookup"><span data-stu-id="339a2-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="339a2-391">Cela inclut toutes les informations du fichier, mais laisse les fichiers sur le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="339a2-392">Cette méthode laisse également l'objet dans un état partiellement non initialisé.</span><span class="sxs-lookup"><span data-stu-id="339a2-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="339a2-393">Les seuls appels valides une fois qu'il s'agit de [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="339a2-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="339a2-394">Cette méthode peut être appelée si Initialize échoue et renvoie E_LSC_CACHEMISMATCH, et supprime le cache associé au SuppliedID fourni avec l'appel qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="339a2-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="339a2-395">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-395">Parameters</span></span>

<span data-ttu-id="339a2-396">Aucun</span><span class="sxs-lookup"><span data-stu-id="339a2-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-397">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-397">Return values</span></span>

|<span data-ttu-id="339a2-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-398">Value</span></span>|<span data-ttu-id="339a2-399">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-401">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="339a2-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-403">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé correctement dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-404">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-405">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="339a2-406">ILSCLocalSyncClient:: ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="339a2-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="339a2-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-407"></span></span>

<span data-ttu-id="339a2-408">ServerFileChange indique à l'objet COM CsiSyncClient de marquer le fichier spécifié pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="339a2-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="339a2-409">Si le fichier est ouvert dans une application Office pour modification, cette méthode renvoie S_OK sans marquer le fichier pour téléchargement (l'application doit déjà effectuer cette étape s'il y a des modifications).</span><span class="sxs-lookup"><span data-stu-id="339a2-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="339a2-410">Cette méthode autorise les téléchargements si elle a été marquée comme téléchargements bloqués précédemment (voir RenameFile).</span><span class="sxs-lookup"><span data-stu-id="339a2-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="339a2-411">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-411">Parameters</span></span>

|<span data-ttu-id="339a2-412">Parameter</span><span class="sxs-lookup"><span data-stu-id="339a2-412">Parameter</span></span>|<span data-ttu-id="339a2-413">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="339a2-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="339a2-415">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="339a2-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="339a2-416">Cette valeur doit être un chemin d'accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="339a2-417">Ce chemin d'accès doit se trouver dans l'arborescence de répertoires spécifiée par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.</span><span class="sxs-lookup"><span data-stu-id="339a2-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="339a2-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="339a2-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="339a2-419">Chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="339a2-420">Cette valeur ne doit pas être vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="339a2-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="339a2-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="339a2-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="339a2-422">Chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="339a2-423">Cette valeur doit être une URL valide non vide, mais pas plus de INTERNET_MAX_URL_LENGTH, comme défini par https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="339a2-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="339a2-424">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-424">Return values</span></span>

|<span data-ttu-id="339a2-425">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-425">Value</span></span>|<span data-ttu-id="339a2-426">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-428">Échec de la définition de l'état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="339a2-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="339a2-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="339a2-430">Le fichier spécifié par _bstrFileSystemPath_ a un ResourceId différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="339a2-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="339a2-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="339a2-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="339a2-432">L'extension de fichier donnée n'est pas prise en charge par l'objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="339a2-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="339a2-433">Voir GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="339a2-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="339a2-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="339a2-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="339a2-435">Le fichier a été supprimé au milieu de l'opération.</span><span class="sxs-lookup"><span data-stu-id="339a2-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="339a2-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-437">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="339a2-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="339a2-439">Le FileSystemPath donné ne se trouve pas sous la racine du répertoire spécifié par FileSystemDirectoryHint lorsque l'appel à Initialize a été effectué.</span><span class="sxs-lookup"><span data-stu-id="339a2-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="339a2-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-441">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="339a2-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="339a2-443">Le fichier spécifié par _bstrResourceID_ a une FileSystemPath différente de celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="339a2-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="339a2-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="339a2-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="339a2-445">Le fichier spécifié a déjà des modifications en attente dans un autre cache et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="339a2-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="339a2-447">Le chemin d'accès webPath fourni se trouve dans un autre cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-448">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-449">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="339a2-450">ILSCLocalSyncClient:: SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="339a2-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="339a2-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-451"></span></span>

<span data-ttu-id="339a2-452">Définit le cache dans un État en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="339a2-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="339a2-453">Si ce n'est pas le cas, Office ne tentera pas de communiquer avec le serveur pour les fichiers de ce cache, quel que soit le paramètre _fBlockUploads_ de chaque fichier individuel.</span><span class="sxs-lookup"><span data-stu-id="339a2-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="339a2-454">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-454">Parameters</span></span>

 <span data-ttu-id="339a2-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="339a2-455">_fIsOnline_</span></span>
  
<span data-ttu-id="339a2-456">Valeur booléenne déterminant l'état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-457">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-457">Return values</span></span>

|<span data-ttu-id="339a2-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-458">Value</span></span>|<span data-ttu-id="339a2-459">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-461">Échec de la définition de l'état de connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="339a2-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="339a2-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-463">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-465">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-466">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-467">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="339a2-468">ILSCLocalSyncClient:: SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="339a2-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="339a2-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-469"></span></span>

<span data-ttu-id="339a2-470">SetClientNetworkSyncPermission est utilisé pour remplacer ou restoreOffice les heuristiques de synchronisation pour le coût réseau et la consommation d'énergie.</span><span class="sxs-lookup"><span data-stu-id="339a2-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="339a2-471">Lorsqu'il est connecté à un réseau 3G ou à un autre réseau à coût élevé, ou lorsqu'il fonctionne sur batterie ou qu'il est branché, Office peut choisir de bloquer le trafic réseau jusqu'à un temps plus opportun.</span><span class="sxs-lookup"><span data-stu-id="339a2-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="339a2-472">Le consommateur de cette API peut l'utiliser pour remplacer les heuristiques Office et forcer la synchronisation à se produire.</span><span class="sxs-lookup"><span data-stu-id="339a2-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="339a2-473">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-473">Parameters</span></span>

 <span data-ttu-id="339a2-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="339a2-474">_nspType_</span></span>
  
<span data-ttu-id="339a2-475">Indicateur qui définit le coût heuristique à remplacer.</span><span class="sxs-lookup"><span data-stu-id="339a2-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="339a2-476">Voir [énumérAtion LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="339a2-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="339a2-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="339a2-477">_fEnableSync_</span></span>
  
<span data-ttu-id="339a2-478">Indique s'il faut forcer la synchronisation, ce qui a pour effet de remplacer cette heuristique des coûts ou de ne pas la remplacer.</span><span class="sxs-lookup"><span data-stu-id="339a2-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-479">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-479">Return values</span></span>

|<span data-ttu-id="339a2-480">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-480">Value</span></span>|<span data-ttu-id="339a2-481">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-483">Échec de la substitution de l'heuristique de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="339a2-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="339a2-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-485">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-486">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-487">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="339a2-488">ILSCLocalSyncClient:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="339a2-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="339a2-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-489"></span></span>

<span data-ttu-id="339a2-490">Décharge le cache de l'objet COM et effectue des opérations de fermeture.</span><span class="sxs-lookup"><span data-stu-id="339a2-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="339a2-491">[ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelé avant la destruction de l'objet COM.</span><span class="sxs-lookup"><span data-stu-id="339a2-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="339a2-492">Une fois appelée, aucune autre API ne peut être appelée, l'objet COM doit être détruit et un nouveau créé si vous souhaitez poursuivre les opérations.</span><span class="sxs-lookup"><span data-stu-id="339a2-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="339a2-493">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-493">Parameters</span></span>

<span data-ttu-id="339a2-494">Aucun.</span><span class="sxs-lookup"><span data-stu-id="339a2-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-495">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-495">Return values</span></span>

|<span data-ttu-id="339a2-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-496">Value</span></span>|<span data-ttu-id="339a2-497">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-499">Échec de l'échec de l'initialisation.</span><span class="sxs-lookup"><span data-stu-id="339a2-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="339a2-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="339a2-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="339a2-501">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n'a pas été appelé avec succès dans le passé.</span><span class="sxs-lookup"><span data-stu-id="339a2-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="339a2-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-502">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-503">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="339a2-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="339a2-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="339a2-505">Cette interface représente une liste d'événements ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="339a2-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="339a2-506">**Fonctions membres publiques**</span><span class="sxs-lookup"><span data-stu-id="339a2-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="339a2-507">IEnumLSCEvent:: FNext</span><span class="sxs-lookup"><span data-stu-id="339a2-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="339a2-508">Extrait l'événement suivant de la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="339a2-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="339a2-509">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-509">Parameters</span></span>

 <span data-ttu-id="339a2-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="339a2-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="339a2-511">Pointeur vers une interface ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="339a2-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-512">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-512">Return values</span></span>

|<span data-ttu-id="339a2-513">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-513">Value</span></span>|<span data-ttu-id="339a2-514">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-516">Il n'y a pas plus d'événements.</span><span class="sxs-lookup"><span data-stu-id="339a2-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="339a2-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-517">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-518">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="339a2-519">IEnumLSCEvent:: Reset</span><span class="sxs-lookup"><span data-stu-id="339a2-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="339a2-520">Rétablit l'énumérateur sur le premier événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="339a2-521">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-521">Parameters</span></span>

<span data-ttu-id="339a2-522">Aucun.</span><span class="sxs-lookup"><span data-stu-id="339a2-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-523">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-523">Return values</span></span>

<span data-ttu-id="339a2-524">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="339a2-525">Interface ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="339a2-525">Interface ILSCEvent</span></span>

<span data-ttu-id="339a2-526">Cette interface représente un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="339a2-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="339a2-527">Toutes les informations relatives à l'événement peuvent être récupérées à partir de l'interface.</span><span class="sxs-lookup"><span data-stu-id="339a2-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="339a2-528">**Fonctions membres publiques**</span><span class="sxs-lookup"><span data-stu-id="339a2-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="339a2-529">ILSCEvent:: GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="339a2-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="339a2-530">Notez que cette valeur est renseignée lorsque [ILSCLocalSyncClient:: GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, et non lorsque l'événement a été créé, de sorte que vous n'aurez que l'état actuel du fichier, et non l'état du fichier lorsque l'état du conflit a changé.</span><span class="sxs-lookup"><span data-stu-id="339a2-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="339a2-531">Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="339a2-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="339a2-532">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-532">Parameters</span></span>

 <span data-ttu-id="339a2-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="339a2-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="339a2-534">État de conflit actuel du fichier associé à l'événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-535">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-535">Return values</span></span>

<span data-ttu-id="339a2-536">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="339a2-537">ILSCEvent:: GetError</span><span class="sxs-lookup"><span data-stu-id="339a2-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="339a2-538">Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="339a2-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="339a2-539">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-539">Parameters</span></span>

 <span data-ttu-id="339a2-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="339a2-540">_pnError_</span></span>
  
<span data-ttu-id="339a2-541">L'erreur associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-542">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-542">Return values</span></span>

<span data-ttu-id="339a2-543">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="339a2-544">ILSCEvent:: GetETag</span><span class="sxs-lookup"><span data-stu-id="339a2-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="339a2-545">Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="339a2-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="339a2-546">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-546">Parameters</span></span>

 <span data-ttu-id="339a2-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="339a2-547">_pbstrETag_</span></span>
  
<span data-ttu-id="339a2-548">ETag associé à cet événement</span><span class="sxs-lookup"><span data-stu-id="339a2-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-549">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-549">Return values</span></span>

<span data-ttu-id="339a2-550">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="339a2-551">ILSCEvent:: GetEventType</span><span class="sxs-lookup"><span data-stu-id="339a2-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="339a2-552">Obtient le type de cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="339a2-553">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-553">Parameters</span></span>

 <span data-ttu-id="339a2-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="339a2-554">_pnEventType_</span></span>
  
<span data-ttu-id="339a2-555">Type d'événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-555">The event type of this event.</span></span> <span data-ttu-id="339a2-556">Voir [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="339a2-557">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-558">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-558">Return values</span></span>

|<span data-ttu-id="339a2-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-559">Value</span></span>|<span data-ttu-id="339a2-560">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-562">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-563">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-564">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="339a2-565">ILSCEvent:: GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="339a2-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="339a2-566">Obtient le chemin de travail local de cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="339a2-567">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-567">Parameters</span></span>

 <span data-ttu-id="339a2-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="339a2-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="339a2-569">Chemin d'accès local du fichier auquel cet événement se rapporte.</span><span class="sxs-lookup"><span data-stu-id="339a2-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-570">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-570">Return values</span></span>

<span data-ttu-id="339a2-571">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="339a2-572">ILSCEvent:: GetResourceID</span><span class="sxs-lookup"><span data-stu-id="339a2-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="339a2-573">Obtient l'ID de ressource de l'événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="339a2-574">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-574">Parameters</span></span>

 <span data-ttu-id="339a2-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="339a2-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="339a2-576">ResourceID du fichier associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="339a2-577">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-577">Return values</span></span>

<span data-ttu-id="339a2-578">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="339a2-579">ILSCEvent:: GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="339a2-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="339a2-580">Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="339a2-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="339a2-581">Lorsqu'un appel à [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoquerait un chemin d'accès Web ou une collision de chemin d'accès local avec un autre fichier dans le cache de fichiers Office, ce l'événement est généré.</span><span class="sxs-lookup"><span data-stu-id="339a2-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="339a2-582">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-582">Parameters</span></span>

 <span data-ttu-id="339a2-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="339a2-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="339a2-584">IDRessource à l'origine de l'événement à obtenir.</span><span class="sxs-lookup"><span data-stu-id="339a2-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="339a2-585">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-586">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-586">Return values</span></span>

<span data-ttu-id="339a2-587">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="339a2-588">ILSCEvent:: GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="339a2-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="339a2-589">Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="339a2-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="339a2-590">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-590">Parameters</span></span>

 <span data-ttu-id="339a2-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="339a2-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="339a2-592">Type d'erreur associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-592">The error type associated with this event.</span></span> <span data-ttu-id="339a2-593">Voir [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs potentielles.</span><span class="sxs-lookup"><span data-stu-id="339a2-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="339a2-594">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-595">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-595">Return values</span></span>

|<span data-ttu-id="339a2-596">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-596">Value</span></span>|<span data-ttu-id="339a2-597">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-599">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-600">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-601">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="339a2-602">ILSCEvent:: GetWebPath</span><span class="sxs-lookup"><span data-stu-id="339a2-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="339a2-603">Cette valeur est renseignée uniquement lorsque l' [énumérAtion LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l'événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="339a2-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="339a2-604">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-604">Parameters</span></span>

 <span data-ttu-id="339a2-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="339a2-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="339a2-606">Spécifie le chemin d'accès Web associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="339a2-607">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-608">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-608">Return values</span></span>

<span data-ttu-id="339a2-609">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="339a2-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="339a2-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="339a2-611">Cette interface contient des informations supplémentaires sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="339a2-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="339a2-612">**Fonctions membres publiques**</span><span class="sxs-lookup"><span data-stu-id="339a2-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="339a2-613">ILSCEvent2:: GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="339a2-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="339a2-614">Obtient les informations de chaîne d'erreur relatives à un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="339a2-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="339a2-615">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-615">Parameters</span></span>

 <span data-ttu-id="339a2-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="339a2-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="339a2-617">Chaîne contenant les informations de chaîne d'erreur.</span><span class="sxs-lookup"><span data-stu-id="339a2-617">A string to hold the error chain information.</span></span> <span data-ttu-id="339a2-618">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="339a2-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-619">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-619">Return values</span></span>

|<span data-ttu-id="339a2-620">Valeur</span><span class="sxs-lookup"><span data-stu-id="339a2-620">Value</span></span>|<span data-ttu-id="339a2-621">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="339a2-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="339a2-623">La version installée d'Office ne prend pas en charge cette interface</span><span class="sxs-lookup"><span data-stu-id="339a2-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="339a2-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="339a2-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="339a2-625">Une ou plusieurs valeurs de paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="339a2-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="339a2-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="339a2-627">Les informations de chaîne d'erreur ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="339a2-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="339a2-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="339a2-628">S_OK</span></span>  <br/> |<span data-ttu-id="339a2-629">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="339a2-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="339a2-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="339a2-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="339a2-631">Cette interface fournit une fonction de rappel à l'objet COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="339a2-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="339a2-632">**Fonctions membres publiques**</span><span class="sxs-lookup"><span data-stu-id="339a2-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="339a2-633">IPartnerActivityCallback:: EventOccurred</span><span class="sxs-lookup"><span data-stu-id="339a2-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="339a2-634">Il s'agit d'une fonction de rappel sur l'objet donné à l'objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="339a2-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="339a2-635">Lorsqu'un événement se produit (voir [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les types d'événements valides), l'objet com CsiSyncClient appelle cette méthode, en signalant le consommateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="339a2-636">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339a2-636">Parameters</span></span>

 <span data-ttu-id="339a2-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="339a2-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="339a2-638">Type d'événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-638">The event type of this event.</span></span> <span data-ttu-id="339a2-639">Voir [énumérAtion LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="339a2-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="339a2-640">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="339a2-640">Return values</span></span>

<span data-ttu-id="339a2-641">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="339a2-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="339a2-642">Énumérations</span><span class="sxs-lookup"><span data-stu-id="339a2-642">Enumerations</span></span>

<span data-ttu-id="339a2-643">CSISyncClient utilise les énumérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="339a2-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="339a2-644">Énumération LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="339a2-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="339a2-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-645"></span></span>

<span data-ttu-id="339a2-646">Cette énumération spécifie les catégories d'erreurs qui peuvent se produire lors de la synchronisation d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="339a2-647">Sa</span><span class="sxs-lookup"><span data-stu-id="339a2-647">Enumerator</span></span>|<span data-ttu-id="339a2-648">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="339a2-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="339a2-650">L'erreur de synchronisation de cet événement était inattendue et peut nécessiter une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="339a2-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="339a2-651">Par défaut, l'utilisateur peut être amené à intervenir.</span><span class="sxs-lookup"><span data-stu-id="339a2-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="339a2-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="339a2-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="339a2-653">L'erreur de synchronisation de cet événement n'a pas besoin de tenir compte d'une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="339a2-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="339a2-654">Office le gérera automatiquement.</span><span class="sxs-lookup"><span data-stu-id="339a2-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="339a2-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="339a2-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="339a2-656">L'erreur de synchronisation de cet événement nécessite qu'un utilisateur le résolve.</span><span class="sxs-lookup"><span data-stu-id="339a2-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="339a2-657">Par exemple, l'erreur de conflit de fusion nécessite un utilisateur pour ouvrir le document et le fusionner.</span><span class="sxs-lookup"><span data-stu-id="339a2-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="339a2-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="339a2-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="339a2-659">L'erreur de synchronisation de cet événement nécessite l'intervention du consommateur, mais ne doit pas exiger une attention particulière de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="339a2-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="339a2-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="339a2-661">L'erreur de synchronisation de cet événement nécessite que le consommateur intervienne en tant que cas particulier.</span><span class="sxs-lookup"><span data-stu-id="339a2-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="339a2-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="339a2-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="339a2-663">Énumération LSCEventType</span><span class="sxs-lookup"><span data-stu-id="339a2-663">Enum LSCEventType</span></span>
<span data-ttu-id="339a2-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-664"></span></span>

<span data-ttu-id="339a2-665">Cette énumération spécifie le type d'événements pouvant se produire pour un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="339a2-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="339a2-666">Sa</span><span class="sxs-lookup"><span data-stu-id="339a2-666">Enumerator</span></span>|<span data-ttu-id="339a2-667">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="339a2-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="339a2-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="339a2-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="339a2-670">Des modifications ont été apportées à un fichier local.</span><span class="sxs-lookup"><span data-stu-id="339a2-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="339a2-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="339a2-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="339a2-672">Un utilisateur A ouvert un fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="339a2-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="339a2-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="339a2-674">Fin du téléchargement des modifications de fichier à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="339a2-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="339a2-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="339a2-676">Fin du chargement des modifications apportées au fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="339a2-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="339a2-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="339a2-678">L'état de conflit de fusion d'un fichier a changé.</span><span class="sxs-lookup"><span data-stu-id="339a2-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="339a2-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="339a2-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="339a2-680">Un fichier a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="339a2-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="339a2-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="339a2-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="339a2-682">Un fichier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="339a2-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="339a2-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="339a2-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="339a2-684">La synchronisation a été activée pour les fichiers d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="339a2-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="339a2-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="339a2-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="339a2-686">Début du téléchargement des modifications de fichier à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="339a2-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="339a2-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="339a2-688">Début du chargement des modifications apportées au fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="339a2-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="339a2-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="339a2-690">Cet événement est généré lorsqu'un appel à [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque une collision de chemin d'accès Web ou de chemin d'accès local avec un autre fichier dans le Cache de fichiers Office.</span><span class="sxs-lookup"><span data-stu-id="339a2-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="339a2-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="339a2-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="339a2-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="339a2-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="339a2-693">Énumération LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="339a2-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="339a2-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-694"></span></span>

<span data-ttu-id="339a2-695">Cette énumération spécifie le type d'événements pouvant se produire.</span><span class="sxs-lookup"><span data-stu-id="339a2-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="339a2-696">Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d'événement.</span><span class="sxs-lookup"><span data-stu-id="339a2-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="339a2-697">Sa</span><span class="sxs-lookup"><span data-stu-id="339a2-697">Enumerator</span></span>|<span data-ttu-id="339a2-698">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="339a2-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="339a2-700">Une ILSCEvent s'est produite.</span><span class="sxs-lookup"><span data-stu-id="339a2-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="339a2-701">Le consommateur doit appeler [ILSCLocalSyncClient:: GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour extraire les données.</span><span class="sxs-lookup"><span data-stu-id="339a2-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="339a2-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="339a2-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="339a2-703">Les extensions de fichiers prises en charge ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="339a2-703">The supported file extensions have changed.</span></span> <span data-ttu-id="339a2-704">Le consommateur doit appeler [ILSCLocalSyncClient:: GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="339a2-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="339a2-705">Énumération LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="339a2-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="339a2-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-706"></span></span>

<span data-ttu-id="339a2-707">Cette énumération spécifie les indicateurs utilisés pour une analyse heuristique des coûts réseau.</span><span class="sxs-lookup"><span data-stu-id="339a2-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="339a2-708">Sa</span><span class="sxs-lookup"><span data-stu-id="339a2-708">Enumerator</span></span>|<span data-ttu-id="339a2-709">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="339a2-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="339a2-711">True si la heuristique des coûts pour les réseaux onéreux (par exemple, 3G) est remplacée.</span><span class="sxs-lookup"><span data-stu-id="339a2-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="339a2-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="339a2-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="339a2-713">True si l'heuristique de coût pour l'utilisation de l'énergie (par exemple, une batterie) est remplacée.</span><span class="sxs-lookup"><span data-stu-id="339a2-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="339a2-714">Énumération LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="339a2-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="339a2-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="339a2-715"></span></span>

<span data-ttu-id="339a2-716">Cette énumération est utilisée pour représenter l'état de synchronisation d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="339a2-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="339a2-717">Sa</span><span class="sxs-lookup"><span data-stu-id="339a2-717">Enumerator</span></span>|<span data-ttu-id="339a2-718">Description</span><span class="sxs-lookup"><span data-stu-id="339a2-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="339a2-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="339a2-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="339a2-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="339a2-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="339a2-721">True s'il y a des données en attente d'envoi au fichier serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="339a2-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="339a2-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="339a2-723">True s'il y a des données en attente de téléchargement à partir du fichier du serveur.</span><span class="sxs-lookup"><span data-stu-id="339a2-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="339a2-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="339a2-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="339a2-725">True si le Bureau de données a sur le fichier dans son cache est la dernière copie des données sur le disque.</span><span class="sxs-lookup"><span data-stu-id="339a2-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

