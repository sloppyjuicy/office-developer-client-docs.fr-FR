---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316631"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="94cdd-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="94cdd-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="94cdd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94cdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94cdd-105">Rend permanentes les modifications apportées à un objet depuis la dernière opération d’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="94cdd-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="94cdd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="94cdd-106">Parameters</span></span>

 <span data-ttu-id="94cdd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94cdd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="94cdd-108">[in] Masque de bits d’indicateurs qui contrôle ce qu’il advient de l’objet lorsque la méthode **IMAPIProp::SaveChanges** est appelée.</span><span class="sxs-lookup"><span data-stu-id="94cdd-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="94cdd-109">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="94cdd-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="94cdd-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="94cdd-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="94cdd-111">Indique que le message n’a pas été remis à partir d’un Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="94cdd-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="94cdd-112">Cet indicateur doit être utilisé en combinaison avec la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) et l’indicateur ITEMPROC_FORCE pour indiquer à un magasin PST que le message est éligible pour le traitement des règles avant que le magasin de dossiers personnels (PST) informe tout client d’écoute que le message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="94cdd-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="94cdd-113">Ce traitement des règles s’applique uniquement aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un Exchange Server, auquel cas le Exchange Server aurait déjà traitée des règles sur le message.</span><span class="sxs-lookup"><span data-stu-id="94cdd-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="94cdd-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="94cdd-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="94cdd-115">Les modifications doivent être écrites dans l’objet, en remplacement des modifications précédentes apportées à l’objet, et l’objet doit être fermé.</span><span class="sxs-lookup"><span data-stu-id="94cdd-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="94cdd-116">Une autorisation de lecture/écriture doit être définie pour que l’opération réussisse.</span><span class="sxs-lookup"><span data-stu-id="94cdd-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="94cdd-117">L FORCE_SAVE est utilisé après un appel précédent à **SaveChanges** renvoyé MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="94cdd-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="94cdd-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="94cdd-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="94cdd-119">Les modifications doivent être déterminées et l’objet doit rester ouvert en lecture.</span><span class="sxs-lookup"><span data-stu-id="94cdd-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="94cdd-120">Aucune modification supplémentaire n’est apportée.</span><span class="sxs-lookup"><span data-stu-id="94cdd-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="94cdd-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="94cdd-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="94cdd-122">Les modifications doivent être déterminées et l’objet doit rester ouvert pour une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="94cdd-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="94cdd-123">Cet indicateur est généralement définie lors de la première ouverture de l’objet pour une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="94cdd-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="94cdd-124">Les modifications ultérieures apportées à l’objet sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="94cdd-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="94cdd-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="94cdd-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="94cdd-126">Permet à **SaveChanges de** retourner correctement, éventuellement avant que les modifications n’ont été entièrement engagés.</span><span class="sxs-lookup"><span data-stu-id="94cdd-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="94cdd-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="94cdd-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="94cdd-128">Active le filtrage du courrier indésirable sur un message enregistré.</span><span class="sxs-lookup"><span data-stu-id="94cdd-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="94cdd-129">La prise en charge du filtrage du courrier indésirable n’est disponible que si le type d’adresse e-mail de l’expéditeur suit le protocole SMTP et que le message est enregistré dans une banque pour un fichier de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="94cdd-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94cdd-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="94cdd-130">Return value</span></span>

<span data-ttu-id="94cdd-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="94cdd-131">S_OK</span></span> 
  
> <span data-ttu-id="94cdd-132">L’engagement des modifications a réussi.</span><span class="sxs-lookup"><span data-stu-id="94cdd-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="94cdd-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="94cdd-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="94cdd-134">**SaveChanges ne** peut pas conserver l’objet ouvert pour une autorisation en lecture seule si KEEP_OPEN_READONLY est définie, ou une autorisation de lecture/écriture si KEEP_OPEN_READWRITE est définie.</span><span class="sxs-lookup"><span data-stu-id="94cdd-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="94cdd-135">Aucune modification n’est apportée.</span><span class="sxs-lookup"><span data-stu-id="94cdd-135">No changes are committed.</span></span> 
    
<span data-ttu-id="94cdd-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="94cdd-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="94cdd-137">L’objet a changé depuis son ouverture.</span><span class="sxs-lookup"><span data-stu-id="94cdd-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="94cdd-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="94cdd-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="94cdd-139">L’objet a été supprimé depuis son ouverture.</span><span class="sxs-lookup"><span data-stu-id="94cdd-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94cdd-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="94cdd-140">Remarks</span></span>

<span data-ttu-id="94cdd-141">La méthode **IMAPIProp::SaveChanges** rend les modifications de propriété permanentes pour les objets qui prend en charge le modèle de traitement des transactions, tels que les messages, les pièces jointes, les conteneurs de carnet d’adresses et les objets utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="94cdd-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="94cdd-142">Les objets qui ne peuvent pas prendre en charge les transactions, tels que les dossiers, les magasins de messages et les sections de profil, modifient immédiatement de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="94cdd-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="94cdd-143">Aucun appel à **SaveChanges n’est** requis.</span><span class="sxs-lookup"><span data-stu-id="94cdd-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="94cdd-144">Étant donné que les fournisseurs de services n’ont pas à générer d’identificateur d’entrée pour leurs objets tant que toutes les propriétés n’ont pas été enregistrées, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) d’un objet peut ne pas être disponible tant que sa méthode **SaveChanges** n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="94cdd-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="94cdd-145">Certains fournisseurs attendent que l’indicateur KEEP_OPEN_READONLY est définie sur l’appel **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="94cdd-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="94cdd-146">KEEP_OPEN_READONLY indique que les modifications à enregistrées dans l’appel actuel seront les dernières modifications apportées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="94cdd-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="94cdd-147">Certaines implémentations de magasin de messages n’affiche pas les messages nouvellement créés dans un dossier tant qu’un client n’enregistre pas les modifications apportées aux messages à l’aide de **SaveChanges** et libère les objets de message à l’aide de la méthode [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94cdd-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="94cdd-148">En outre, certaines implémentations d’objets ne peuvent pas générer une propriété PR_ENTRYID pour un objet nouvellement créé tant que **SaveChanges** n’a pas été appelé, et d’autres ne peuvent le faire qu’après que **SaveChanges** **a** été appelé à l’aide de KEEP_OPEN_READONLY définie dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="94cdd-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="94cdd-149">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="94cdd-149">Notes to implementers</span></span>

<span data-ttu-id="94cdd-150">Si vous recevez l’KEEP_OPEN_READONLY, vous avez la possibilité de laisser l’accès de l’objet en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="94cdd-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="94cdd-151">Toutefois, un fournisseur ne peut jamais laisser un objet en lecture seule lorsque l’KEEP_OPEN_READWRITE est passé.</span><span class="sxs-lookup"><span data-stu-id="94cdd-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="94cdd-152">Lorsqu’un client enregistre plusieurs pièces jointes dans plusieurs messages, il appelle la méthode **SaveChanges** pour chaque pièce jointe et chaque message.</span><span class="sxs-lookup"><span data-stu-id="94cdd-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="94cdd-153">Souvent, les clients MAPI_DEFERRED_ERRORS pour chacun de ces appels, à l’exception du dernier.</span><span class="sxs-lookup"><span data-stu-id="94cdd-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="94cdd-154">Vous pouvez renvoyer des erreurs avec le dernier appel ou les appels précédents.</span><span class="sxs-lookup"><span data-stu-id="94cdd-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="94cdd-155">Vous pouvez même ignorer l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="94cdd-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="94cdd-156">Si une KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY est définie avec MAPI_DEFERRED_ERRORS, vous pouvez ignorer la demande de report d’erreur.</span><span class="sxs-lookup"><span data-stu-id="94cdd-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="94cdd-157">Si MAPI_DEFERRED_ERRORS n’est pas définie dans _ulFlags,_ l’une des erreurs différées précédemment peut être renvoyée pour l’appel **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="94cdd-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="94cdd-158">Si un fournisseur de transport distant fournit une implémentation fonctionnelle de cette méthode est facultatif et dépend d’autres choix de conception dans votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="94cdd-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="94cdd-159">Si vous implémentez cette méthode, faites-le conformément à la documentation ici.</span><span class="sxs-lookup"><span data-stu-id="94cdd-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="94cdd-160">Étant donné que les objets de dossier et les objets d’état ne sont pas transactionn s, au minimum l’implémentation **d’SaveChanges** par un fournisseur de transport distant doit renvoyer S_OK sans réellement faire de travail.</span><span class="sxs-lookup"><span data-stu-id="94cdd-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="94cdd-161">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="94cdd-161">Notes to callers</span></span>

<span data-ttu-id="94cdd-162">Si un client passe KEEP_OPEN_READONLY, appelle la méthode [IMAPIProp::SetProps,](imapiprop-setprops.md) puis appelle à nouveau **SaveChanges,** la même implémentation peut échouer.</span><span class="sxs-lookup"><span data-stu-id="94cdd-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="94cdd-163">Après avoir reçu MAPI_E_NO_ACCESS d’un appel dans lequel vous avez KEEP_OPEN_READWRITE, vous continuerez à avoir une autorisation de lecture/écriture sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="94cdd-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="94cdd-164">Vous pouvez appeler à nouveau **SaveChanges,** en passant l’indicateur KEEP_OPEN_READONLY ou aucun indicateur avec KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="94cdd-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="94cdd-165">Le fait qu’un fournisseur prend en charge KEEP_OPEN_READWRITE’indicateur dépend de l’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94cdd-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="94cdd-166">Pour indiquer que le seul appel à appeler sur l’objet après **SaveChanges** est **IUnknown::Release**, ne définissez aucun indicateur pour le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="94cdd-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="94cdd-167">Une erreur **de SaveChanges indique** qu’il n’a pas pu rendre permanentes les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="94cdd-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="94cdd-168">Différents fournisseurs gèrent différemment l’absence d’indicateurs sur **l’appel SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="94cdd-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="94cdd-169">Certains fournisseurs traitent cet état de la même façon que KEEP_OPEN_READONLY ; d’autres fournisseurs l’interprètent de la même KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="94cdd-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="94cdd-170">D’autres fournisseurs arrêtent l’objet lorsqu’ils ne reçoivent pas d’indicateurs lors de **l’appel SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="94cdd-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="94cdd-171">Certaines propriétés, généralement calculées, ne peuvent pas être traitées tant que vous n’avez pas appelé **SaveChanges** et, dans certains cas, **Release**.</span><span class="sxs-lookup"><span data-stu-id="94cdd-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="94cdd-172">Lorsque vous a majeurez des modifications, telles que l’enregistrement de pièces jointes dans plusieurs messages, reportez le traitement des erreurs en MAPI_DEFERRED_ERRORS’indicateur dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="94cdd-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="94cdd-173">Si vous enregistrez plusieurs pièces jointes dans plusieurs messages, faites un appel **SaveChanges** à chaque pièce jointe et un appel **SaveChanges** à chaque message.</span><span class="sxs-lookup"><span data-stu-id="94cdd-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="94cdd-174">Définissez l MAPI_DEFERRED_ERRORS pour chaque appel de pièce jointe et pour tous les messages à l’exception du dernier.</span><span class="sxs-lookup"><span data-stu-id="94cdd-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="94cdd-175">Si **SaveChanges renvoie** MAPI_E_OBJECT_CHANGED, vérifiez si l’objet d’origine a été modifié.</span><span class="sxs-lookup"><span data-stu-id="94cdd-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="94cdd-176">Si c’est le cas, avertissez l’utilisateur, qui peut demander que les modifications ont été réécrites ou enregistrer l’objet ailleurs.</span><span class="sxs-lookup"><span data-stu-id="94cdd-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="94cdd-177">Si l’objet d’origine a été supprimé, avertissez l’utilisateur de lui donner la possibilité d’enregistrer l’objet à un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="94cdd-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="94cdd-178">Vous ne pouvez **pas appeler SaveChanges** avec l’FORCE_SAVE sur un objet ouvert qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="94cdd-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="94cdd-179">Si **SaveChanges renvoie** une erreur, l’objet dont les modifications doivent être enregistrées reste ouvert, quels que soient les indicateurs définies dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="94cdd-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="94cdd-180">Les NON_EMS_XP_SAVE  _ulFlags_ et SPAMFILTER_ONSAVE peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="94cdd-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="94cdd-181">Pour plus d’informations, voir [Enregistrement des propriétés MAPI.](saving-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="94cdd-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94cdd-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94cdd-182">See also</span></span>



[<span data-ttu-id="94cdd-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="94cdd-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="94cdd-184">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="94cdd-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="94cdd-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94cdd-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="94cdd-186">Enregistrement des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="94cdd-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

