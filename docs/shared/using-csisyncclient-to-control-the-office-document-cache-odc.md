---
title: Utilisation de CSISyncClient pour contrôler le Cache de documents Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Découvrez comment utiliser CSISyncClient pour contrôler le Cache de documents Office (ODC).
ms.openlocfilehash: adaa56bf040889bd8220506bcfab8fdb0b7ab6c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787978"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="e842a-103">Utilisation de CSISyncClient pour contrôler le Cache de documents Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="e842a-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="e842a-104">Découvrez comment utiliser CSISyncClient pour contrôler le Cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="e842a-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="e842a-105">CSISyncClient est un serveur COM out-of-process (CsiSyncClient.exe) qui permet à Microsoft OneDrive contrôler le comportement de la Cache de documents Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="e842a-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="e842a-106">Par exemple, OneDrive peut-être faire appel à la ODC via CSISyncClient pour télécharger des fichiers vers et depuis les systèmes d’extrémité MS-FSSHTTP est activé.</span><span class="sxs-lookup"><span data-stu-id="e842a-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="e842a-107">Cela permet de garantie service fonctionnalités avancées dans Office, telles que les transitions de co-création et transparentes d’en mode hors connexion à en ligne.</span><span class="sxs-lookup"><span data-stu-id="e842a-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="e842a-108">CsiSyncClient est disponible dans Office Desktop (x86 et x64).</span><span class="sxs-lookup"><span data-stu-id="e842a-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="e842a-109">Remarque : Alors que les nouvelles versions d’Office peuvent livrées avec CsiSyncClient, le processus sera utilisé pour la compatibilité descendante uniquement.</span><span class="sxs-lookup"><span data-stu-id="e842a-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="e842a-110">L’interface CsiSyncClient et la méthodologie de contrôler le ODC seront modifié dans les futures versions de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="e842a-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="e842a-111">L’identificateur de classe est actuellement définie pour répondre uniquement à OneDrive.</span><span class="sxs-lookup"><span data-stu-id="e842a-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="e842a-112">L’objet COM est utilisable comme serveur COM out-of-proc et s’exécute dans CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="e842a-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="e842a-113">En raison de limitations avec Access (qui le ODC utilise), il est fourni avec le type de bit Office est fourni dans ce x64 Office signifie un x64 objet COM ou x86 Office signifie un x86 objet COM.</span><span class="sxs-lookup"><span data-stu-id="e842a-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="e842a-114">Pour contourner cette limitation, spécification CLSCTX_LOCAL_SERVER comme partie de l’interface CoCreateInstance aura l’objet COM être hébergé en tant qu’un serveur COM out-of-process, autoriser la compatibilité cross-nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="e842a-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="e842a-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="e842a-115">Interfaces</span></span>

<span data-ttu-id="e842a-116">CSISyncClient utilise les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="e842a-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="e842a-117">Interface ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="e842a-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="e842a-118">Il s’agit de l’interface principale utilisée pour synchroniser des fichiers dans Office.</span><span class="sxs-lookup"><span data-stu-id="e842a-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="e842a-119">ProgID : Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="e842a-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="e842a-120">CLSID : {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="e842a-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="e842a-121">Bibliothèque de types : {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="e842a-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="e842a-122">L’objet COM qui est exposé est utilisé comme un serveur out-of-Process.</span><span class="sxs-lookup"><span data-stu-id="e842a-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="e842a-123">Spécification CLSCTX_LOCAL_SERVER dans le cadre de CoCreateInstance permet de compatibilité entre les processus 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e842a-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="e842a-124">Une fois que vous avez créé conjointement l’objet COM, vous devez d’abord appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="e842a-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="e842a-125">Une fois que [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) est terminée, vous pouvez appeler n’importe quelle API aussi souvent que vous le souhaitez et dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="e842a-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="e842a-126">Vous pouvez également appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) sur un objet déjà initialisé, mais cela n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="e842a-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="e842a-127">Les exceptions pour le paragraphe précédent sont [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) et [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="e842a-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="e842a-128">Une fois que vous appelez [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) sur l’objet COM, vous devez détruire cet objet et créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="e842a-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="e842a-129">[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) supprimer votre subcache, supprimez toutes les informations de fichier associé dans le cache, mais laissez les documents sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e842a-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="e842a-130">Il également conserve l’état pour communiquer avec le cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="e842a-131">Cela vous permet d’appeler [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) à nouveau pour créer un nouveau cache sans devoir supprimer et recréer l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="e842a-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="e842a-132">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="e842a-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="e842a-133">ILSCLocalSyncClient::DeleteFile</span><span class="sxs-lookup"><span data-stu-id="e842a-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="e842a-134">DeleteFile est utilisée pour supprimer les informations du fichier à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="e842a-135">Toutefois, cette méthode laisse le fichier associé sur le disque et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="e842a-136">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-136">Parameters</span></span>

 <span data-ttu-id="e842a-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="e842a-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="e842a-138">Chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="e842a-139">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-140">Return values</span></span>

|<span data-ttu-id="e842a-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-141">Value</span></span>|<span data-ttu-id="e842a-142">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-144">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-146">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-148">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="e842a-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="e842a-150">Le ResourceID donné n’est pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-152">Initialize n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="e842a-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="e842a-154">Le fichier est en cours de synchronisation ou ouvrir et ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="e842a-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="e842a-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-155">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-156">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="e842a-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="e842a-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="e842a-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-158"></span></span>

<span data-ttu-id="e842a-159">GetChanges retourne un énumérateur des objets ILSCEvent et retourne également un jeton qui est donné à l’appel suivant à GetChanges, en supposant que le consommateur a traité l’ensemble d’événements précédent.</span><span class="sxs-lookup"><span data-stu-id="e842a-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="e842a-160">Événements avant le _nPreviousChangesToken_ spécifié seront supprimés et non disponible.</span><span class="sxs-lookup"><span data-stu-id="e842a-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="e842a-161">S’il n’y a aucun événement à traiter, _pnCurrentChangesToken_ doit être la même valeur que _nPreviousChangesToken_, mais _ppiEvents_ sera toujours définie.</span><span class="sxs-lookup"><span data-stu-id="e842a-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="e842a-162">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-162">Parameters</span></span>

 <span data-ttu-id="e842a-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="e842a-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="e842a-164">Identifie l’événement qui a été traitée en dernier par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="e842a-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="e842a-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="e842a-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="e842a-166">Identifie l’événement le plus récent est transmise au consommateur.</span><span class="sxs-lookup"><span data-stu-id="e842a-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="e842a-167">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-167">Must not be null.</span></span>
  
 <span data-ttu-id="e842a-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="e842a-168">_ppiEvents_</span></span>
  
<span data-ttu-id="e842a-169">Énumérateur pour les événements remis au consommateur.</span><span class="sxs-lookup"><span data-stu-id="e842a-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="e842a-170">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-171">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-171">Return values</span></span>

|<span data-ttu-id="e842a-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-172">Value</span></span>|<span data-ttu-id="e842a-173">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-175">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-177">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-179">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-180">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-181">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="e842a-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="e842a-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="e842a-183">GetClientNetworkSyncPermission est utilisée pour interroger si heuristique synchronisation du bureau pour réseau coût et consommation d’énergie sont remplacées.</span><span class="sxs-lookup"><span data-stu-id="e842a-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="e842a-184">Sur un 3G ou un autre réseau coûteuses, ou lors de l’exécution sur la batterie et branché, Office peut choisir de bloquer le trafic réseau jusqu'à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="e842a-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="e842a-185">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-185">Parameters</span></span>

 <span data-ttu-id="e842a-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="e842a-186">_nspType_</span></span>
  
<span data-ttu-id="e842a-187">Indicateur qui définit le heuristique de coût de requête.</span><span class="sxs-lookup"><span data-stu-id="e842a-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="e842a-188">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="e842a-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="e842a-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="e842a-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="e842a-190">Spécifie si l’heuristique coût demandé est actuellement remplacé ou non.</span><span class="sxs-lookup"><span data-stu-id="e842a-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="e842a-191">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-192">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-192">Return values</span></span>

|<span data-ttu-id="e842a-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-193">Value</span></span>|<span data-ttu-id="e842a-194">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-196">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-198">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-200">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-201">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-202">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="e842a-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="e842a-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="e842a-204">GetFileStatus est utilisé pour collecter des informations pour un fichier spécifique : si elle existe dans le cache, si elle est en attente de la communication avec la copie sur le serveur, et si Office 2013 possède le plus jusqu'à les données de date de la copie locale.</span><span class="sxs-lookup"><span data-stu-id="e842a-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="e842a-205">Il nécessite un indicateur de bits des valeurs [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) pour déterminer les informations de l’objet COM CsiSyncClient consiste à interroger.</span><span class="sxs-lookup"><span data-stu-id="e842a-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="e842a-206">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-206">Parameters</span></span>

 <span data-ttu-id="e842a-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="e842a-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="e842a-208">Chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="e842a-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="e842a-209">Cette valeur doit être vide, avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="e842a-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="e842a-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="e842a-211">Indicateur qui définit les informations à retourner.</span><span class="sxs-lookup"><span data-stu-id="e842a-211">A flag which defines what information to return.</span></span> <span data-ttu-id="e842a-212">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="e842a-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="e842a-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="e842a-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="e842a-214">Chaîne qui identifie l’emplacement du fichier identifié par _bstrResourceID_ sur le client.</span><span class="sxs-lookup"><span data-stu-id="e842a-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="e842a-215">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-215">Must not be null.</span></span> 
  
 <span data-ttu-id="e842a-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="e842a-216">_pbstrETag_</span></span>
  
<span data-ttu-id="e842a-217">Chaîne qui contient l’eTag pour le fichier identifié par _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="e842a-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="e842a-218">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-218">Must not be null.</span></span> 
  
 <span data-ttu-id="e842a-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="e842a-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="e842a-220">Indicateur qui contiendra le statut demandé par le biais de _sfRequestedStatus_ pour le fichier identifié par _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="e842a-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="e842a-221">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-221">Must not be null.</span></span> <span data-ttu-id="e842a-222">Voir [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="e842a-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-223">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-223">Return values</span></span>

|<span data-ttu-id="e842a-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-224">Value</span></span>|<span data-ttu-id="e842a-225">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-227">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-229">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="e842a-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="e842a-231">Les informations du fichier spécifiées par _bstrResourceID_ n’existent pas dans le cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e842a-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="e842a-233">LSCStatusFlag_LocalFileUnchanged a été demandé, ou le fichier spécifié par _bstrResourceID_ est verrouillé ou manquant.</span><span class="sxs-lookup"><span data-stu-id="e842a-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="e842a-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-235">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-236">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-237">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="e842a-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="e842a-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="e842a-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-239"></span></span>

<span data-ttu-id="e842a-240">GetSupportedFileExtensions renvoie une liste délimitée par des canaux des extensions de fichiers qui sont actuellement pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="e842a-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="e842a-241">Notez que cette liste peut modifier et le consommateur serez ainsi averti d’une modification par le biais de l’objet IPartnerActivityCallback fourni sur [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (voir EventOccured).</span><span class="sxs-lookup"><span data-stu-id="e842a-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="e842a-242">Un exemple de la chaîne renvoyée se présente comme suit : « | docx | docm | pptx | »</span><span class="sxs-lookup"><span data-stu-id="e842a-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="e842a-243">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-243">Parameters</span></span>

 <span data-ttu-id="e842a-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="e842a-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="e842a-245">Chaîne à définir avec un ensemble d’extensions de fichiers pris en charge par l’objet COM CsiSyncClient délimité par canal.</span><span class="sxs-lookup"><span data-stu-id="e842a-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="e842a-246">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-247">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-247">Return values</span></span>

|<span data-ttu-id="e842a-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-248">Value</span></span>|<span data-ttu-id="e842a-249">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-251">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-253">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-255">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-256">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-257">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="e842a-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="e842a-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="e842a-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-259"></span></span>

<span data-ttu-id="e842a-260">Initialize doit être la première méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="e842a-260">Initialize must be the first method called.</span></span> <span data-ttu-id="e842a-261">Dans le cas contraire, toutes les autres API renverra E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="e842a-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="e842a-262">L’appel de Initialize sur un objet déjà initialisé renvoie S_OK et n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="e842a-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="e842a-263">Si E_LSC_CACHEMISMATCH est renvoyée, l’appelant peut appeler [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) pour supprimer le cache associé à le SuppliedID donné.</span><span class="sxs-lookup"><span data-stu-id="e842a-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="e842a-264">Toutefois, dans ce cas autres API retournera encore E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="e842a-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="e842a-265">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-265">Parameters</span></span>

 <span data-ttu-id="e842a-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="e842a-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="e842a-267">Identifie le consommateur et qui mettent en cache à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e842a-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="e842a-268">Doit être vide avec un maximum de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="e842a-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="e842a-269">_bstrProgID_</span></span>
  
<span data-ttu-id="e842a-270">Identifie un objet COM de la consommation de communication bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="e842a-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="e842a-271">Doit être vide avec un maximum de 39 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="e842a-272">Voir [ \<ProgID\> clé](http://msdn.microsoft.com/fr-fr/library/ms690196.aspx.aspx) pour plus d’informations sur le ProgID.</span><span class="sxs-lookup"><span data-stu-id="e842a-272">See [\<ProgID\> Key](http://msdn.microsoft.com/fr-fr/library/ms690196.aspx.aspx) for more information on ProgIDs.</span></span> 
  
 <span data-ttu-id="e842a-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="e842a-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="e842a-274">Identifie la racine du répertoire dans lequel seront stockés les fichiers locaux.</span><span class="sxs-lookup"><span data-stu-id="e842a-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="e842a-275">Doit être vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="e842a-276">Le répertoire doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="e842a-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="e842a-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="e842a-277">_pEventCallback_</span></span>
  
<span data-ttu-id="e842a-278">L’interface de rappel qui avertit CsiSyncClient sur les modifications.</span><span class="sxs-lookup"><span data-stu-id="e842a-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="e842a-279">Voir IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="e842a-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="e842a-280">Cette valeur ne doit pas être nulle.</span><span class="sxs-lookup"><span data-stu-id="e842a-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="e842a-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="e842a-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="e842a-282">Renvoie si un nouveau cache a été créé.</span><span class="sxs-lookup"><span data-stu-id="e842a-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="e842a-283">Si le cache n’est associé à la SuppliedID, un sera créé.</span><span class="sxs-lookup"><span data-stu-id="e842a-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="e842a-284">Cette valeur ne doit pas être nulle.</span><span class="sxs-lookup"><span data-stu-id="e842a-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-285">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-285">Return values</span></span>

|<span data-ttu-id="e842a-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-286">Value</span></span>|<span data-ttu-id="e842a-287">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-289">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-291">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="e842a-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="e842a-293">Un SuppliedID déjà possède un cache qui lui est associé, mais dispose d’un ProgId ou FileSystemDirectoryHint différentes de celles qui sont fournies.</span><span class="sxs-lookup"><span data-stu-id="e842a-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="e842a-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="e842a-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="e842a-295">Le FileSystemDirectoryHint (ou un sous-dossier) existe déjà sur un cache différent.</span><span class="sxs-lookup"><span data-stu-id="e842a-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="e842a-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="e842a-297">Le ProgID existe déjà sur un cache différent.</span><span class="sxs-lookup"><span data-stu-id="e842a-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-298">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-299">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="e842a-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="e842a-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="e842a-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-301"></span></span>

<span data-ttu-id="e842a-302">LocalFileChange est utilisée pour indiquer à l’objet COM CsiSyncClient pour essayer de télécharger le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e842a-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="e842a-303">La méthode prépare le fichier à télécharger, y compris le contenu du fichier en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="e842a-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="e842a-304">Si un téléchargement est déjà en attente, téléchargement précédent sera ignoré et le nouveau contenu préparé pour télécharger.</span><span class="sxs-lookup"><span data-stu-id="e842a-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="e842a-305">Si le fichier est ouvert pour modification dans une application, cette méthode renvoie S_OK sans préparer le fichier de téléchargement (l’application doit déjà effectuer cette étape si des modifications sont apportées).</span><span class="sxs-lookup"><span data-stu-id="e842a-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="e842a-306">Cette méthode permet volumineux s’il a été marqué comme télécharge bloqués précédemment (voir [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="e842a-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="e842a-307">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-307">Parameters</span></span>

 <span data-ttu-id="e842a-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="e842a-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="e842a-309">Une chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="e842a-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="e842a-310">Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="e842a-311">Ce chemin d’accès doit être dans l’arborescence du répertoire spécifié par le FileSystemDirectoryHint lors de l’appel à [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) a été effectué.</span><span class="sxs-lookup"><span data-stu-id="e842a-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="e842a-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="e842a-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="e842a-313">Une chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="e842a-314">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="e842a-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="e842a-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="e842a-316">Une chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="e842a-317">Cette valeur doit être URL non vide et valide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="e842a-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-318">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-318">Return values</span></span>

|<span data-ttu-id="e842a-319">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-319">Value</span></span>|<span data-ttu-id="e842a-320">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-322">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-324">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="e842a-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="e842a-326">Le fichier spécifié par _bstrFileSystemPath_ a un autre ResourceID celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="e842a-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="e842a-327">Un événement de type LSCEventType_OnFilePathConflict est envoyée lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="e842a-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="e842a-328">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="e842a-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="e842a-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="e842a-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="e842a-330">Le fichier a été supprimée opération intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="e842a-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="e842a-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="e842a-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="e842a-332">L’extension de fichier donné n’est pas pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="e842a-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="e842a-333">Voir [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="e842a-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="e842a-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="e842a-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="e842a-335">L’objet COM n’avez pas prévu un téléchargement parce que le fichier dans le cache a des modifications les plus récentes à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="e842a-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="e842a-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e842a-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="e842a-337">Le fichier spécifié par _bstrFileSystemPath_ est manquant ou verrouillé.</span><span class="sxs-lookup"><span data-stu-id="e842a-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="e842a-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="e842a-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="e842a-339">Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="e842a-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-341">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="e842a-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="e842a-343">Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="e842a-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="e842a-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="e842a-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="e842a-345">Le fichier spécifié déjà en attente de modification dans un cache différent et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="e842a-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="e842a-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="e842a-347">Le WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="e842a-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-348">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-349">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="e842a-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="e842a-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="e842a-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-351"></span></span>

<span data-ttu-id="e842a-352">RenameFile associe une nouvelle URL et le chemin d’accès local pour un ResourceID donné.</span><span class="sxs-lookup"><span data-stu-id="e842a-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="e842a-353">Si le fichier spécifié par le ResourceID n’existe pas déjà dans le cache, une tentative seront créer et marquer pour téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e842a-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="e842a-354">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-354">Parameters</span></span>

 <span data-ttu-id="e842a-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="e842a-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="e842a-356">Une chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="e842a-357">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="e842a-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="e842a-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="e842a-359">Chaîne qui spécifie le nouveau chemin d’accès local pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="e842a-360">Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="e842a-361">Ce chemin d’accès doit être dans l’arborescence spécifiée par le FileSystemDirectoryHint lors de l’appel à initialiser.</span><span class="sxs-lookup"><span data-stu-id="e842a-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="e842a-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="e842a-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="e842a-363">Chaîne qui spécifie la nouvelle URL pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="e842a-364">Cette valeur doit être non vides URL valide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="e842a-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="e842a-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="e842a-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="e842a-366">Spécifie si les téléchargements vers le nouvel emplacement sont actuellement autorisées.</span><span class="sxs-lookup"><span data-stu-id="e842a-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-367">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-367">Return values</span></span>

|<span data-ttu-id="e842a-368">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-368">Value</span></span>|<span data-ttu-id="e842a-369">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-371">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-373">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="e842a-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="e842a-375">Le _bstrNewFileSystemPath_ ou _bstrNewWebPath_ existent déjà sur un autre fichier dans n’importe quel cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="e842a-376">Un événement de type LSCEventType_OnFilePathConflict est envoyée lorsque cette erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="e842a-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="e842a-377">Voir [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="e842a-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="e842a-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="e842a-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="e842a-379">Les informations du fichier a été supprimées du cache pendant l’exécution de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e842a-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="e842a-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="e842a-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="e842a-381">Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="e842a-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-383">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="e842a-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="e842a-385">Le fichier spécifié est en cours de synchronisation dans une application Office.</span><span class="sxs-lookup"><span data-stu-id="e842a-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="e842a-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-386">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-387">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="e842a-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="e842a-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="e842a-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-389"></span></span>

<span data-ttu-id="e842a-390">ResetCache supprime le cache associé à le SuppliedID qui a été fournie dans Initialize.</span><span class="sxs-lookup"><span data-stu-id="e842a-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="e842a-391">Cela inclut toutes les informations sur les fichier, mais laisse les fichiers sur le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="e842a-392">Cette méthode rend également l’objet dans un état partiellement non initialisé.</span><span class="sxs-lookup"><span data-stu-id="e842a-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="e842a-393">Les appels valides uniquement après ce sont [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="e842a-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="e842a-394">Cette méthode peut être appelée si Initialize échoue et renvoie E_LSC_CACHEMISMATCH et supprime le cache associé à le SuppliedID qui a été fournie avec l’appel défectueux.</span><span class="sxs-lookup"><span data-stu-id="e842a-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="e842a-395">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-395">Parameters</span></span>

<span data-ttu-id="e842a-396">Aucune</span><span class="sxs-lookup"><span data-stu-id="e842a-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-397">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-397">Return values</span></span>

|<span data-ttu-id="e842a-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-398">Value</span></span>|<span data-ttu-id="e842a-399">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-401">L’appel n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="e842a-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-403">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-404">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-405">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="e842a-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="e842a-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="e842a-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-407"></span></span>

<span data-ttu-id="e842a-408">ServerFileChange indique à l’objet COM CsiSyncClient pour marquer le fichier spécifié pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e842a-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="e842a-409">Si le fichier est ouvert dans une application Office pour modifier, cette méthode renvoie S_OK sans marquage du fichier de téléchargement (l’application doit déjà effectuer cette étape si des modifications sont apportées).</span><span class="sxs-lookup"><span data-stu-id="e842a-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="e842a-410">Cette méthode permet téléchargements si elle a été marquée comme téléchargements bloqués précédemment (voir RenameFile).</span><span class="sxs-lookup"><span data-stu-id="e842a-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="e842a-411">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-411">Parameters</span></span>

|<span data-ttu-id="e842a-412">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e842a-412">Parameter</span></span>|<span data-ttu-id="e842a-413">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="e842a-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="e842a-415">Une chaîne qui identifie le fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="e842a-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="e842a-416">Cette valeur doit être un chemin d’accès local non vide avec un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="e842a-417">Ce chemin d’accès doit être dans l’arborescence spécifiée par le FileSystemDirectoryHint lors de l’appel à initialiser.</span><span class="sxs-lookup"><span data-stu-id="e842a-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="e842a-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="e842a-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="e842a-419">Une chaîne qui identifie le ResourceID du fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="e842a-420">Cette valeur doit être vide avec un maximum de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="e842a-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="e842a-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="e842a-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="e842a-422">Une chaîne qui identifie le fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="e842a-423">Cette valeur doit être une URL valide non vide, mais pas plus de INTERNET_MAX_URL_LENGTH, tel que défini par http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="e842a-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="e842a-424">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-424">Return values</span></span>

|<span data-ttu-id="e842a-425">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-425">Value</span></span>|<span data-ttu-id="e842a-426">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-428">Échec pour définir l’état de la connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="e842a-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="e842a-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="e842a-430">Le fichier spécifié par _bstrFileSystemPath_ a un autre ResourceID celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="e842a-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="e842a-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="e842a-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="e842a-432">L’extension de fichier donné n’est pas pris en charge par l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="e842a-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="e842a-433">Voir GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="e842a-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="e842a-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="e842a-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="e842a-435">Le fichier a été supprimé dans une opération intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="e842a-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="e842a-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-437">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="e842a-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="e842a-439">Le FileSystemPath donné n’est pas sous la racine du répertoire spécifiée par le FileSystemDirectoryHint lors de l’appel d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="e842a-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-441">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="e842a-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="e842a-443">Le fichier spécifié par _bstrResourceID_ a un FileSystemPath différent de celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="e842a-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="e842a-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="e842a-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="e842a-445">Le fichier spécifié a des modifications en attente dans un cache différent déjà et ne peut pas encore être associé au cache du consommateur.</span><span class="sxs-lookup"><span data-stu-id="e842a-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="e842a-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="e842a-447">Le WebPath fourni se situe sous un cache différent.</span><span class="sxs-lookup"><span data-stu-id="e842a-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-448">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-449">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="e842a-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="e842a-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="e842a-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-451"></span></span>

<span data-ttu-id="e842a-452">Définit le cache dans un état en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e842a-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="e842a-453">Si elle est en mode hors connexion, Office tentera pas à communiquer avec le serveur pour tous les fichiers dans ce cache, quel que soit le paramètre de _fBlockUploads_ de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="e842a-454">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-454">Parameters</span></span>

 <span data-ttu-id="e842a-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="e842a-455">_fIsOnline_</span></span>
  
<span data-ttu-id="e842a-456">Valeur de type boolean détermination de l’état de la connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-457">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-457">Return values</span></span>

|<span data-ttu-id="e842a-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-458">Value</span></span>|<span data-ttu-id="e842a-459">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-461">Échec pour définir l’état de la connectivité du cache.</span><span class="sxs-lookup"><span data-stu-id="e842a-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="e842a-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-463">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-465">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-466">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-467">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="e842a-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="e842a-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="e842a-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-469"></span></span>

<span data-ttu-id="e842a-470">SetClientNetworkSyncPermission est utilisé pour substituer ou heuristique de synchronisation de restoreOffice pour réseau d’utilisation de coûts et d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="e842a-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="e842a-471">Sur un 3G ou un autre réseau coûteuses, ou lors de l’exécution sur la batterie et branché, Office peut choisir de bloquer le trafic réseau jusqu'à un moment plus opportun.</span><span class="sxs-lookup"><span data-stu-id="e842a-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="e842a-472">Le consommateur de cette API pouvez l’utiliser pour remplacer heuristique d’Office et de forcer la synchronisation ait lieu.</span><span class="sxs-lookup"><span data-stu-id="e842a-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="e842a-473">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-473">Parameters</span></span>

 <span data-ttu-id="e842a-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="e842a-474">_nspType_</span></span>
  
<span data-ttu-id="e842a-475">Indicateur qui définit le heuristique coût à remplacer.</span><span class="sxs-lookup"><span data-stu-id="e842a-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="e842a-476">Voir [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="e842a-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="e842a-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="e842a-477">_fEnableSync_</span></span>
  
<span data-ttu-id="e842a-478">Spécifie s’il faut forcer la synchronisation, remplaçant ainsi que heuristique coût, ou remplacer n’est plus.</span><span class="sxs-lookup"><span data-stu-id="e842a-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-479">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-479">Return values</span></span>

|<span data-ttu-id="e842a-480">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-480">Value</span></span>|<span data-ttu-id="e842a-481">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-483">Échec de la synchronisation heuristique de remplacer.</span><span class="sxs-lookup"><span data-stu-id="e842a-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="e842a-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-485">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-486">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-487">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="e842a-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="e842a-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="e842a-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-489"></span></span>

<span data-ttu-id="e842a-490">Décharge le cache de l’objet COM et effectuer des opérations de fermeture.</span><span class="sxs-lookup"><span data-stu-id="e842a-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="e842a-491">[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DOIT être appelée avant la destruction de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="e842a-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="e842a-492">Une fois appelée, aucune autre API ne peut être appelé, l’objet COM doit être détruit et créer une nouvelle si vous souhaitez continuer d’opérations.</span><span class="sxs-lookup"><span data-stu-id="e842a-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="e842a-493">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-493">Parameters</span></span>

<span data-ttu-id="e842a-494">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e842a-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-495">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-495">Return values</span></span>

|<span data-ttu-id="e842a-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-496">Value</span></span>|<span data-ttu-id="e842a-497">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-499">Échec d’annuler l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="e842a-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e842a-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="e842a-501">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) n’a pas été correctement appelé dans le passé.</span><span class="sxs-lookup"><span data-stu-id="e842a-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="e842a-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-502">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-503">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="e842a-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="e842a-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="e842a-505">Cette interface représente une liste d’événements ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="e842a-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="e842a-506">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="e842a-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="e842a-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="e842a-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="e842a-508">Récupère l’événement suivant à partir de la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="e842a-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="e842a-509">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-509">Parameters</span></span>

 <span data-ttu-id="e842a-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="e842a-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="e842a-511">Pointeur vers une interface ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="e842a-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-512">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-512">Return values</span></span>

|<span data-ttu-id="e842a-513">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-513">Value</span></span>|<span data-ttu-id="e842a-514">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-516">Il existe plus d’événements.</span><span class="sxs-lookup"><span data-stu-id="e842a-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="e842a-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-517">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-518">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="e842a-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="e842a-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="e842a-520">Réinitialise l’énumérateur au premier événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="e842a-521">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-521">Parameters</span></span>

<span data-ttu-id="e842a-522">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e842a-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-523">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-523">Return values</span></span>

<span data-ttu-id="e842a-524">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="e842a-525">Interface ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="e842a-525">Interface ILSCEvent</span></span>

<span data-ttu-id="e842a-526">Cette interface représente un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="e842a-527">Toutes les informations relatives à l’événement peuvent être récupérées à partir de l’interface.</span><span class="sxs-lookup"><span data-stu-id="e842a-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="e842a-528">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="e842a-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="e842a-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="e842a-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="e842a-530">Notez que cette valeur est renseignée lorsque [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) est appelé, pas lorsque l’événement a été créé, vous devrez uniquement l’état actuel du fichier, pas l’état du fichier lors de la modification de l’état de conflit.</span><span class="sxs-lookup"><span data-stu-id="e842a-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="e842a-531">Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="e842a-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="e842a-532">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-532">Parameters</span></span>

 <span data-ttu-id="e842a-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="e842a-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="e842a-534">L’état actuel de conflit du fichier associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-535">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-535">Return values</span></span>

<span data-ttu-id="e842a-536">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="e842a-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="e842a-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="e842a-538">Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="e842a-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="e842a-539">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-539">Parameters</span></span>

 <span data-ttu-id="e842a-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="e842a-540">_pnError_</span></span>
  
<span data-ttu-id="e842a-541">L’erreur associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-542">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-542">Return values</span></span>

<span data-ttu-id="e842a-543">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="e842a-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="e842a-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="e842a-545">Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="e842a-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="e842a-546">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-546">Parameters</span></span>

 <span data-ttu-id="e842a-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="e842a-547">_pbstrETag_</span></span>
  
<span data-ttu-id="e842a-548">L’ETag associé à cet événement</span><span class="sxs-lookup"><span data-stu-id="e842a-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-549">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-549">Return values</span></span>

<span data-ttu-id="e842a-550">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="e842a-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="e842a-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="e842a-552">Obtient le type de cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="e842a-553">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-553">Parameters</span></span>

 <span data-ttu-id="e842a-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="e842a-554">_pnEventType_</span></span>
  
<span data-ttu-id="e842a-555">Le type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-555">The event type of this event.</span></span> <span data-ttu-id="e842a-556">Voir [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="e842a-557">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-558">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-558">Return values</span></span>

|<span data-ttu-id="e842a-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-559">Value</span></span>|<span data-ttu-id="e842a-560">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-562">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-563">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-564">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="e842a-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="e842a-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="e842a-566">Obtient le chemin d’accès local de travail de cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="e842a-567">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-567">Parameters</span></span>

 <span data-ttu-id="e842a-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="e842a-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="e842a-569">Le chemin d’accès local du fichier à laquelle cet événement se rapporte.</span><span class="sxs-lookup"><span data-stu-id="e842a-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-570">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-570">Return values</span></span>

<span data-ttu-id="e842a-571">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="e842a-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="e842a-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="e842a-573">Obtient l’ID de ressource pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="e842a-574">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-574">Parameters</span></span>

 <span data-ttu-id="e842a-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="e842a-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="e842a-576">ResourceID du fichier associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="e842a-577">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-577">Return values</span></span>

<span data-ttu-id="e842a-578">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="e842a-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="e842a-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="e842a-580">Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="e842a-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="e842a-581">Lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque un conflit de chemin d’accès Web ou le chemin d’accès Local avec un autre fichier dans le cache des fichiers Office, cela événement est généré.</span><span class="sxs-lookup"><span data-stu-id="e842a-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="e842a-582">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-582">Parameters</span></span>

 <span data-ttu-id="e842a-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="e842a-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="e842a-584">ResourceID qui a provoqué cet événement sont générés.</span><span class="sxs-lookup"><span data-stu-id="e842a-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="e842a-585">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-586">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-586">Return values</span></span>

<span data-ttu-id="e842a-587">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="e842a-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="e842a-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="e842a-589">Cette valeur est remplie uniquement lorsque l' [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="e842a-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="e842a-590">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-590">Parameters</span></span>

 <span data-ttu-id="e842a-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="e842a-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="e842a-592">Le type d’erreur associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-592">The error type associated with this event.</span></span> <span data-ttu-id="e842a-593">Voir [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) pour les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="e842a-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="e842a-594">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-595">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-595">Return values</span></span>

|<span data-ttu-id="e842a-596">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-596">Value</span></span>|<span data-ttu-id="e842a-597">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-599">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-600">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-601">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="e842a-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="e842a-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="e842a-603">Cette valeur est renseignée uniquement lors de l' [Énumération LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) de l’événement est LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="e842a-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="e842a-604">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-604">Parameters</span></span>

 <span data-ttu-id="e842a-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="e842a-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="e842a-606">Spécifie le chemin d’accès Web associé à cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="e842a-607">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-608">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-608">Return values</span></span>

<span data-ttu-id="e842a-609">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="e842a-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="e842a-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="e842a-611">Cette interface conserve des informations supplémentaires sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="e842a-612">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="e842a-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="e842a-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="e842a-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="e842a-614">Obtient les informations de la chaîne d’erreur sur un événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="e842a-615">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-615">Parameters</span></span>

 <span data-ttu-id="e842a-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="e842a-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="e842a-617">Une chaîne contenant les informations de la chaîne d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e842a-617">A string to hold the error chain information.</span></span> <span data-ttu-id="e842a-618">Ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="e842a-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-619">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-619">Return values</span></span>

|<span data-ttu-id="e842a-620">Valeur</span><span class="sxs-lookup"><span data-stu-id="e842a-620">Value</span></span>|<span data-ttu-id="e842a-621">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="e842a-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="e842a-623">La version d’Office installée ne prend pas en charge cette interface</span><span class="sxs-lookup"><span data-stu-id="e842a-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="e842a-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e842a-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e842a-625">Un ou plusieurs des valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="e842a-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e842a-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="e842a-627">Les informations de la chaîne d’erreur ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e842a-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="e842a-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="e842a-628">S_OK</span></span>  <br/> |<span data-ttu-id="e842a-629">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e842a-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="e842a-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="e842a-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="e842a-631">Cette interface fournit une fonction de rappel à l’objet COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="e842a-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="e842a-632">**Fonctions membres publics**</span><span class="sxs-lookup"><span data-stu-id="e842a-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="e842a-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="e842a-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="e842a-634">Il s’agit d’une fonction de rappel sur l’objet donné à l’objet COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="e842a-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="e842a-635">Il est prévu que lorsqu’un événement se produit (voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour des types d’événement valide), l’objet COM CsiSyncClient appeler cette méthode, le consommateur de signalisation.</span><span class="sxs-lookup"><span data-stu-id="e842a-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="e842a-636">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e842a-636">Parameters</span></span>

 <span data-ttu-id="e842a-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="e842a-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="e842a-638">Le type d’événement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-638">The event type of this event.</span></span> <span data-ttu-id="e842a-639">Voir [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) pour les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="e842a-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="e842a-640">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e842a-640">Return values</span></span>

<span data-ttu-id="e842a-641">Renvoie toujours S_OK.</span><span class="sxs-lookup"><span data-stu-id="e842a-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="e842a-642">Énumérations</span><span class="sxs-lookup"><span data-stu-id="e842a-642">Enumerations</span></span>

<span data-ttu-id="e842a-643">CSISyncClient utilise les énumérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="e842a-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="e842a-644">Énumération LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="e842a-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="e842a-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-645"></span></span>

<span data-ttu-id="e842a-646">Cette énumération spécifie les catégories d’erreurs qui peuvent se produire lors de la synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="e842a-647">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="e842a-647">Enumerator</span></span>|<span data-ttu-id="e842a-648">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="e842a-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="e842a-650">L’erreur de synchronisation de cet événement était inattendu et peut nécessiter une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="e842a-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="e842a-651">Par défaut, l’utilisateur peut avoir à intervenir.</span><span class="sxs-lookup"><span data-stu-id="e842a-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="e842a-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="e842a-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="e842a-653">L’erreur de synchronisation de cet événement ne doit pas une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="e842a-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="e842a-654">Office il gère automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e842a-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="e842a-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="e842a-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="e842a-656">L’erreur de synchronisation de cet événement requiert un utilisateur pour le résoudre.</span><span class="sxs-lookup"><span data-stu-id="e842a-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="e842a-657">Par exemple, erreur de conflit de fusion requiert un utilisateur ouvrir le document et les fusionner.</span><span class="sxs-lookup"><span data-stu-id="e842a-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="e842a-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="e842a-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="e842a-659">L’erreur de synchronisation de cet événement requiert le consommateur intervenir, mais ne nécessitent ne pas une attention particulière par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e842a-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="e842a-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="e842a-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="e842a-661">L’erreur de synchronisation de cet événement requiert le consommateur intervenir comme un cas spécial.</span><span class="sxs-lookup"><span data-stu-id="e842a-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="e842a-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="e842a-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="e842a-663">Énumération LSCEventType</span><span class="sxs-lookup"><span data-stu-id="e842a-663">Enum LSCEventType</span></span>
<span data-ttu-id="e842a-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-664"></span></span>

<span data-ttu-id="e842a-665">Cette énumération spécifie le type d’événements qui peut se produire pour un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="e842a-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="e842a-666">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="e842a-666">Enumerator</span></span>|<span data-ttu-id="e842a-667">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="e842a-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="e842a-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="e842a-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="e842a-670">Modifications apportées à un fichier local.</span><span class="sxs-lookup"><span data-stu-id="e842a-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="e842a-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="e842a-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="e842a-672">Un utilisateur ouvre un fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="e842a-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="e842a-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="e842a-674">Terminé le téléchargement des modifications de fichiers à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="e842a-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="e842a-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="e842a-676">Terminé le téléchargement des modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="e842a-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="e842a-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="e842a-678">L’état de conflit de fusion d’un fichier a changé.</span><span class="sxs-lookup"><span data-stu-id="e842a-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="e842a-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="e842a-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="e842a-680">Un fichier a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="e842a-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="e842a-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="e842a-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="e842a-682">Un fichier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="e842a-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="e842a-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="e842a-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="e842a-684">Synchronisation a été activée pour les fichiers d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e842a-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="e842a-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="e842a-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="e842a-686">Démarrer le téléchargement des modifications de fichiers à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="e842a-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="e842a-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="e842a-688">Démarrer le téléchargement des modifications de fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e842a-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="e842a-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="e842a-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="e842a-690">Cet événement est généré lorsqu’un appel à [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoque un conflit de chemin d’accès Web ou le chemin d’accès Local avec un autre fichier dans le Cache de fichiers Office.</span><span class="sxs-lookup"><span data-stu-id="e842a-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="e842a-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="e842a-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="e842a-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="e842a-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="e842a-693">Énumération LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="e842a-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="e842a-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-694"></span></span>

<span data-ttu-id="e842a-695">Cette énumération spécifie le type des événements qui peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="e842a-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="e842a-696">Le consommateur doit appeler des fonctions ILSCLocalSyncClient spécifiques en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="e842a-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="e842a-697">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="e842a-697">Enumerator</span></span>|<span data-ttu-id="e842a-698">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="e842a-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="e842a-700">Un ILSCEvent s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e842a-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="e842a-701">Le consommateur doit appeler [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) pour extraire les données.</span><span class="sxs-lookup"><span data-stu-id="e842a-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="e842a-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="e842a-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="e842a-703">Les extensions de fichier prises en charge ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="e842a-703">The supported file extensions have changed.</span></span> <span data-ttu-id="e842a-704">Le consommateur doit appeler [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) pour récupérer la nouvelle liste des extensions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e842a-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="e842a-705">Énumération LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="e842a-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="e842a-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-706"></span></span>

<span data-ttu-id="e842a-707">Cette énumération spécifie les indicateurs utilisés pour une heuristique de coût du réseau.</span><span class="sxs-lookup"><span data-stu-id="e842a-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="e842a-708">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="e842a-708">Enumerator</span></span>|<span data-ttu-id="e842a-709">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="e842a-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="e842a-711">True si l’heuristique coût pour les réseaux coûteux (par exemple, 3 G) est remplacé.</span><span class="sxs-lookup"><span data-stu-id="e842a-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="e842a-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="e842a-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="e842a-713">True si l’heuristique coût consommation d’énergie (par exemple, une batterie) est remplacé.</span><span class="sxs-lookup"><span data-stu-id="e842a-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="e842a-714">Énumération LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="e842a-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="e842a-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="e842a-715"></span></span>

<span data-ttu-id="e842a-716">Cette énumération est utilisée pour représenter l’état de synchronisation d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="e842a-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="e842a-717">Énumérateur</span><span class="sxs-lookup"><span data-stu-id="e842a-717">Enumerator</span></span>|<span data-ttu-id="e842a-718">Description</span><span class="sxs-lookup"><span data-stu-id="e842a-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e842a-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="e842a-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="e842a-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="e842a-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="e842a-721">True si les données à envoyer au fichier du serveur en attente.</span><span class="sxs-lookup"><span data-stu-id="e842a-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="e842a-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="e842a-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="e842a-723">True si les données à télécharger à partir du fichier de serveur en attente.</span><span class="sxs-lookup"><span data-stu-id="e842a-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="e842a-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="e842a-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="e842a-725">True si les données Office sur le fichier dans son cache est la plus récente copie des données sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e842a-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

