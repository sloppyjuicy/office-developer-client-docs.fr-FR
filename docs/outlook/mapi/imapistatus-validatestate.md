---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438147"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="ab2d3-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="ab2d3-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="ab2d3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab2d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab2d3-105">Confirme les informations d’état externe disponibles pour la ressource MAPI ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="ab2d3-106">Cette méthode est prise en charge dans tous les objets d’état.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ab2d3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab2d3-107">Parameters</span></span>

<span data-ttu-id="ab2d3-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ab2d3-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="ab2d3-109">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="ab2d3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab2d3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ab2d3-111">[in] Masque de bits d’indicateurs qui contrôle la validation.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="ab2d3-112">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="ab2d3-112">The following flags can be set:</span></span>
    
<span data-ttu-id="ab2d3-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="ab2d3-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="ab2d3-114">L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue correspondante.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="ab2d3-115">L’objet d’état dispose de deux options :</span><span class="sxs-lookup"><span data-stu-id="ab2d3-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="ab2d3-116">Continuez à travailler sur l’opération.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="ab2d3-117">Arrêtez l’opération et renvoyez MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="ab2d3-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="ab2d3-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="ab2d3-119">Une ou plusieurs propriétés de configuration de l’objet d’état ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="ab2d3-120">Les clients peuvent définir cet indicateur pour permettre aupooler MAPI de corriger dynamiquement les défaillances critiques du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="ab2d3-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="ab2d3-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="ab2d3-122">L’objet d’état doit effectuer une connexion.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-122">The status object should perform a connection.</span></span> <span data-ttu-id="ab2d3-123">Lorsque cet indicateur est utilisé avec l’REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la connexion se produit sans mise en cache.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="ab2d3-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="ab2d3-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="ab2d3-125">L’objet d’état doit effectuer une opération de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="ab2d3-126">Lorsque cet indicateur est utilisé avec l’REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la déconnexion se produit sans mise en cache.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="ab2d3-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="ab2d3-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="ab2d3-128">Les entrées de la table de cache d’en-tête doivent être traitées, tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="ab2d3-129">Les messages qui ont des MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE doivent être déplacés.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="ab2d3-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="ab2d3-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="ab2d3-131">Pour un fournisseur de transport distant, une nouvelle liste d’en-têtes de message doit être téléchargée et tous les indicateurs qui marquent l’état du message doivent être effacés.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="ab2d3-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="ab2d3-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="ab2d3-133">Empêche l’objet status d’afficher une interface utilisateur dans le cadre de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab2d3-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ab2d3-134">Return value</span></span>

<span data-ttu-id="ab2d3-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab2d3-135">S_OK</span></span> 
  
> <span data-ttu-id="ab2d3-136">La validation a réussi.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-136">The validation was successful.</span></span>
    
<span data-ttu-id="ab2d3-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ab2d3-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ab2d3-138">Une autre opération est en cours ; Il doit être autorisé à se terminer ou arrêté avant le début de cette opération.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="ab2d3-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ab2d3-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ab2d3-140">L’objet status ne prend pas en charge la méthode de validation, comme indiqué par l’absence de l’indicateur STATUS_VALIDATE_STATE dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ab2d3-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="ab2d3-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ab2d3-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ab2d3-142">L’utilisateur a annulé l’opération de validation, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="ab2d3-143">Cette valeur est renvoyée uniquement par les fournisseurs de transport distants.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ab2d3-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab2d3-144">Remarks</span></span>

<span data-ttu-id="ab2d3-145">La **méthode IMAPIStatus::ValidateState** vérifie l’état d’une ressource associée à un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="ab2d3-146">**ValidateState** est la seule méthode de l’interface [IMAPIStatus](imapistatusimapiprop.md) requise pour tous les objets d’état.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="ab2d3-147">Le comportement exact de cette méthode dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="ab2d3-148">Le tableau suivant décrit l’implémentation de chacun des différents types d’objets d’état.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="ab2d3-149">**Objet Status**</span><span class="sxs-lookup"><span data-stu-id="ab2d3-149">**Status object**</span></span>|<span data-ttu-id="ab2d3-150">Implémentation ValidateState\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab2d3-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab2d3-151">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="ab2d3-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="ab2d3-152">Valide l’état de toutes les ressources que les fournisseurs de services actifs et le sous-système lui-même possèdent.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="ab2d3-153">Pooler MAPI</span><span class="sxs-lookup"><span data-stu-id="ab2d3-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="ab2d3-154">Effectue une session de tous les fournisseurs de transport, qu’ils soient déjà connectés ou non.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="ab2d3-155">Carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="ab2d3-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="ab2d3-156">Vérifie les entrées dans sa section de profil.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="ab2d3-157">Fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="ab2d3-157">Service provider</span></span>  <br/> |<span data-ttu-id="ab2d3-158">L’implémentation dépend du type de fournisseur et des indicateurs définies dans _le paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ab2d3-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="ab2d3-159">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ab2d3-159">Notes to implementers</span></span>

<span data-ttu-id="ab2d3-160">Les applications clientes distantes **appellent la méthode ValidateState** pour démarrer le traitement à distance pour diverses actions.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="ab2d3-161">Cette méthode permet principalement de définir des bits d’état pour communiquer avec lepooler MAPI, au lieu de faire n’importe quel travail.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="ab2d3-162">En règle générale, le fournisseur de transport définit des indicateurs dans sa ligne d’état qui indiquent aupooler MAPI quelles actions doivent être lancées pour terminer la demande du client.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="ab2d3-163">Dans ce modèle d’interaction client-transport-spooler, les actions demandées par le client sont asynchrones, dans ce cas **ValidateState** renvoie avant que les actions demandées soient terminées.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="ab2d3-164">Toutefois, les actions qui n’impliquent pas nécessairement le système de messagerie sous-jacent ou qui impliquent une interface spécifique au transport peuvent être synchrones.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="ab2d3-165">L’application cliente passe un masque de bits des indicateurs suivants pour spécifier les actions que le fournisseur de transport distant doit prendre.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="ab2d3-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="ab2d3-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="ab2d3-167">Si possible, le fournisseur de transport distant doit annuler toutes les opérations qui impliquent le téléchargement d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="ab2d3-168">Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d’état de l’objet d’logo :</span><span class="sxs-lookup"><span data-stu-id="ab2d3-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="ab2d3-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to stop the incoming flush process for this transport provider.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="ab2d3-170">Définissez le STATUS_OFFLINE bit dans la **PR_STATUS_CODE** propriété.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="ab2d3-171">Définissez **la PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="ab2d3-172">Définissez **la PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="ab2d3-173">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-173">Return S_OK.</span></span> <span data-ttu-id="ab2d3-174">Toutefois, si l’opération en cours ne peut pas être annulée, **ValidateState** doit MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="ab2d3-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="ab2d3-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="ab2d3-176">Un fournisseur de transport distant ne doit jamais établir de connexion à une ressource partagée (par exemple, un modem ou un port COM) en dehors du contexte de l’interaction de transport depooler MAPI impliquée dans la méthode [IXPLogon::FlushQueues.](ixplogon-flushqueues.md)</span><span class="sxs-lookup"><span data-stu-id="ab2d3-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="ab2d3-177">Si **ValidateState** est appelé avec cet indicateur, votre fournisseur de transport doit :</span><span class="sxs-lookup"><span data-stu-id="ab2d3-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="ab2d3-178">Définissez un indicateur d’état interne pour indiquer que la connexion distante doit être établie lorsque la méthode **IXPLogon::FlushQueues** est appelée.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="ab2d3-179">Définissez les valeurs correctes dans la table d’état pour que lepooler MAPI lance le processus de purge de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="ab2d3-180">Lorsque le purgement des files d’attente est terminé, relâchez la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="ab2d3-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="ab2d3-182">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-182">Return S_OK.</span></span>
    
<span data-ttu-id="ab2d3-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="ab2d3-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="ab2d3-184">Le fournisseur de transport distant doit libérer sa connexion aux ressources système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="ab2d3-185">Après cela, il doit définir le bit STATUS_OFFLINE dans la propriété **PR_STATUS_CODE** et renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="ab2d3-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="ab2d3-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="ab2d3-187">Le fournisseur de transport distant doit traiter les messages distants et télécharger tous les messages différés.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="ab2d3-188">Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d’état de l’objet d’logo :</span><span class="sxs-lookup"><span data-stu-id="ab2d3-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="ab2d3-189">Définissez **la PR_STATUS_STRING** sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="ab2d3-190">Définissez les STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE bits dans la **PR_STATUS_CODE** de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="ab2d3-191">Définissez **la PR_REMOTE_VALIDATE_OK** de transport dans la ligne d’état du fournisseur de transport sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="ab2d3-192">Si une autre opération est en cours (par exemple, le téléchargement des en-têtes) lorsque **ValidateState** est appelé, **ValidateState** doit MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="ab2d3-193">Exécutez le code pour traiter l’indicateur REFRESH_XP_HEADER_CACHE, afin de satisfaire les exigences du client Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="ab2d3-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="ab2d3-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="ab2d3-195">Le fournisseur de transport distant doit récupérer les nouveaux en-têtes de message à partir du système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="ab2d3-196">Pour ce faire, le fournisseur de transport doit :</span><span class="sxs-lookup"><span data-stu-id="ab2d3-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="ab2d3-197">Définissez **la PR_STATUS_STRING** sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="ab2d3-198">Définissez les STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE bits dans la **PR_STATUS_CODE** propriété.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="ab2d3-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="ab2d3-200">Définissez le bit STATUS_ONLINE dans la **propriété PR_STATUS_CODE.**</span><span class="sxs-lookup"><span data-stu-id="ab2d3-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="ab2d3-201">Définissez **la PR_REMOTE_VALIDATE_OK** de transport dans la ligne d’état du fournisseur de transport sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="ab2d3-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="ab2d3-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="ab2d3-203">Si votre fournisseur de transport dispose d’éléments d’interface utilisateur pour le traitement des en-têtes de message (par exemple, une boîte de dialogue confirmant le téléchargement des messages), cette boîte de dialogue doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="ab2d3-204">Dans le cas **contraire, ValidateState** peut renvoyer MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="ab2d3-205">Si des indicateurs autres que ceux-ci sont passés, **ValidateState** doit MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="ab2d3-206">L’appel du client au fournisseur de transport est souvent à la méthode **IMAPIStatus::ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="ab2d3-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="ab2d3-207">Pendant le traitement de **ValidateState,** le fournisseur de transport ne doit effectuer aucune action qui alloue des ressources système allouées, telles qu’un modem ou un port COM.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="ab2d3-208">Cela est dû au fait que lepooler MAPI devra parfois vider les files d’attente sur plusieurs fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="ab2d3-209">Toutefois, le client peut appeler la méthode **ValidateState** de n’importe quel fournisseur de transport à tout moment.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="ab2d3-210">Si votre fournisseur de transport tente d’allouer une ressource importante pendant le traitement de **ValidateState**, une erreur peut se produite en raison d’un conflit avec un autre fournisseur de transport que lepooler MAPI a demandé de vider ses files d’attente.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="ab2d3-211">Si vous autorisez toutes les allocations de ressources sous la direction dupooler MAPI, vous pouvez éviter de tels conflits.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="ab2d3-212">Votre fournisseur de transport doit prendre en **charge la propriété PR_REMOTE_VALIDATE_OK** afin que les applications clientes détectent quand votre fournisseur de transport est occupé ou en attente que lepooler MAPI lance une action.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ab2d3-213">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ab2d3-213">Notes to callers</span></span>

<span data-ttu-id="ab2d3-214">Étant donné que cette méthode peut entraîner d’autres appels potentiellement longs, **ValidateState** peut renvoyer MAPI_E_BUSY pour vous informer que cette méthode attend la fin d’une autre opération.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="ab2d3-215">Vous devez attendre la fin de l’opération en attente avant d’essayer une autre tâche.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="ab2d3-216">Vous contrôlez le mieux vos appels aux objets d’état du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="ab2d3-217">Vous pouvez transmettre un ou plusieurs indicateurs **à ValidateState** qui affectent les opérations du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="ab2d3-218">Par exemple, l’ABORT_XP_HEADER_OPERATION indique que l’utilisateur a annulé la validation.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="ab2d3-219">Les fournisseurs de transport peuvent décider d’abandonner, de MAPI_E_USER_CANCELED ou de continuer.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="ab2d3-220">Vous pouvez définir l’indicateur CONFIG_CHANGED sur un appel à l’objet d’état d’un fournisseur de services ou aupooler MAPI pour indiquer qu’une option de configuration a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="ab2d3-221">Vous pouvez utiliser CONFIG_CHANGED pour reconfigurer dynamiquement un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="ab2d3-222">Lorsque vous définissez CONFIG_CHANGED sur un appel à l’objet d’état d’un fournisseur de services, le fournisseur répond par un appel à [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) pour alerter lepooler MAPI de la modification.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="ab2d3-223">Lorsque vous définissez CONFIG_CHANGED sur un appel à l’objet d’état dupooler MAPI, lepooler appelle [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour chaque fournisseur de transport actif.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="ab2d3-224">**AddressTypes informe** lepooler MAPI des types d’adresses pris en charge par un transport.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="ab2d3-225">Certains fournisseurs de services affichent également un indicateur de progression si la validation est prévue pour prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="ab2d3-226">L’affichage d’un indicateur de progression est utile, mais pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="ab2d3-227">Lorsque l’SUPPRESS_UI est définie, aucune des feuilles de propriétés de configuration ou des boîtes de dialogue de progression ne peut être affichée.</span><span class="sxs-lookup"><span data-stu-id="ab2d3-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab2d3-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab2d3-228">See also</span></span>

- [<span data-ttu-id="ab2d3-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="ab2d3-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="ab2d3-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="ab2d3-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="ab2d3-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="ab2d3-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="ab2d3-232">Propriété canonique PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="ab2d3-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="ab2d3-233">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="ab2d3-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="ab2d3-234">Propriété canonique PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="ab2d3-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="ab2d3-235">Propriété canonique PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="ab2d3-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="ab2d3-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ab2d3-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

