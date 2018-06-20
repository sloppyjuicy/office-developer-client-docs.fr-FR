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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0a60b813a52779b28124ab6d69b493def35b14aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783917"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="bbc46-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="bbc46-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="bbc46-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbc46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbc46-105">Rend permanentes toutes les modifications qui ont été apportées à un objet depuis la dernière opération d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bbc46-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bbc46-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="bbc46-106">Parameters</span></span>

 <span data-ttu-id="bbc46-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbc46-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bbc46-108">[in] Masque de bits d’indicateurs qui contrôle ce qui se passe à l’objet lorsque la méthode **IMAPIProp::SaveChanges** est appelée.</span><span class="sxs-lookup"><span data-stu-id="bbc46-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="bbc46-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="bbc46-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="bbc46-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="bbc46-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="bbc46-111">Indique que le message n’a pas été remis à partir d’un serveur Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="bbc46-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="bbc46-112">Cet indicateur doit être utilisé conjointement avec la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) et traitement avant que le magasin de fichiers (PST) de dossiers personnels avertit une des règles de l’indicateur ITEMPROC_FORCE pour indiquer à une banque de dossiers personnels que le message est éligible pour client d’écoute que le message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="bbc46-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="bbc46-113">Cette règle traitement s’applique uniquement aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un serveur Exchange, auquel cas le serveur Exchange est ont déjà traités règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="bbc46-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="bbc46-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="bbc46-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="bbc46-115">Modifications doivent être écrites à l’objet écraser les modifications précédentes qui ont été apportées à l’objet, et l’objet doit être fermé.</span><span class="sxs-lookup"><span data-stu-id="bbc46-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="bbc46-116">Autorisation de lecture/écriture doit être définie pour l’opération aboutisse.</span><span class="sxs-lookup"><span data-stu-id="bbc46-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="bbc46-117">L’indicateur FORCE_SAVE est utilisé lorsqu’un appel précédent à **SaveChanges** MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="bbc46-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="bbc46-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="bbc46-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="bbc46-119">Les modifications doivent être validées et l’objet doit être maintenue ouverte pour être lue.</span><span class="sxs-lookup"><span data-stu-id="bbc46-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="bbc46-120">Aucune modification supplémentaire ne sera.</span><span class="sxs-lookup"><span data-stu-id="bbc46-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="bbc46-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="bbc46-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="bbc46-122">Les modifications doivent être validées et l’objet doit être conservée à ouvrir pour l’autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="bbc46-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="bbc46-123">Cet indicateur est généralement défini lors de la première ouverture de l’objet d’autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="bbc46-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="bbc46-124">Les modifications suivantes à l’objet sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="bbc46-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="bbc46-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="bbc46-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="bbc46-126">Permet de **SaveChanges** renvoyer avec succès, éventuellement avant que les modifications ont été entièrement validées.</span><span class="sxs-lookup"><span data-stu-id="bbc46-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="bbc46-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="bbc46-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="bbc46-128">Permet de courrier indésirable de filtrage d’un message est enregistré.</span><span class="sxs-lookup"><span data-stu-id="bbc46-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="bbc46-129">Prise en charge de filtrage du courrier indésirable est disponible uniquement si le type d’adresse de messagerie de l’expéditeur est SMTP Simple Mail Transfer Protocol (), et le message est enregistré dans un magasin d’un fichier de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="bbc46-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbc46-130">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bbc46-130">Return value</span></span>

<span data-ttu-id="bbc46-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbc46-131">S_OK</span></span> 
  
> <span data-ttu-id="bbc46-132">L’engagement des modifications a réussi.</span><span class="sxs-lookup"><span data-stu-id="bbc46-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="bbc46-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bbc46-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="bbc46-134">L’objet ne peuvent pas conserver ouverte pour un accès en lecture seule **SaveChanges** si KEEP_OPEN_READONLY est set ou autorisation en lecture/écriture si KEEP_OPEN_READWRITE est défini.</span><span class="sxs-lookup"><span data-stu-id="bbc46-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="bbc46-135">Aucune modification n’est validée.</span><span class="sxs-lookup"><span data-stu-id="bbc46-135">No changes are committed.</span></span> 
    
<span data-ttu-id="bbc46-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="bbc46-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="bbc46-137">L’objet a été modifié depuis son ouverture.</span><span class="sxs-lookup"><span data-stu-id="bbc46-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="bbc46-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="bbc46-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="bbc46-139">L’objet a été supprimé car il a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="bbc46-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbc46-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="bbc46-140">Remarks</span></span>

<span data-ttu-id="bbc46-141">La méthode **IMAPIProp::SaveChanges** apporte les modifications de propriété définitive pour les objets qui prennent en charge le modèle de transaction de traitement, telles que les messages, les pièces jointes, les conteneurs de carnet d’adresses et les objets utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bbc46-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="bbc46-142">Les objets qui ne prennent pas en charge les transactions, telles que les dossiers et banques de messages aux sections de profil apporter des modifications permanentes immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bbc46-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="bbc46-143">Aucun appel à **SaveChanges** n’est requis.</span><span class="sxs-lookup"><span data-stu-id="bbc46-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="bbc46-144">Car les fournisseurs de services n’ont pas à générer un identificateur d’entrée pour leurs objets jusqu'à ce que toutes les propriétés ont été enregistrées, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) d’un objet peuvent ne pas être disponible qu’après la méthode **SaveChanges** a été appelée.</span><span class="sxs-lookup"><span data-stu-id="bbc46-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="bbc46-145">Certains fournisseurs attendre jusqu'à ce que l’indicateur KEEP_OPEN_READONLY est défini sur l’appel de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="bbc46-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="bbc46-146">KEEP_OPEN_READONLY indique que les modifications soient enregistrées dans l’appel en cours est le dernier des modifications qui seront effectuées sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="bbc46-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="bbc46-147">Certaines implémentations de banque de messages ne pas afficher nouvellement créé les messages dans un dossier jusqu'à un client enregistre le message passe à l’aide de **SaveChanges** et libère les objets de message à l’aide de la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bbc46-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="bbc46-148">En outre, certaines implémentations de l’objet ne peut pas générer une propriété **PR_ENTRYID** d’un objet nouvellement créé jusqu'à après **SaveChanges** a été appelée et certaines peuvent le faire qu’après **SaveChanges** a été appelée à l’aide de KEEP_OPEN_READONLY définir dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="bbc46-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bbc46-149">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="bbc46-149">Notes to implementers</span></span>

<span data-ttu-id="bbc46-150">Si vous recevez l’indicateur KEEP_OPEN_READONLY, vous avez la possibilité de laisser des accès de l’objet en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="bbc46-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="bbc46-151">Toutefois, un fournisseur ne peut jamais laisser un objet dans un état en lecture seule lorsque l’indicateur KEEP_OPEN_READWRITE est passé.</span><span class="sxs-lookup"><span data-stu-id="bbc46-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="bbc46-152">Lorsqu’un client enregistre plusieurs pièces jointes à plusieurs messages, il appelle la méthode **SaveChanges** pour chaque pièce jointe et chaque message.</span><span class="sxs-lookup"><span data-stu-id="bbc46-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="bbc46-153">Souvent, les clients définira MAPI_DEFERRED_ERRORS pour chacun de ces appels, à l’exception de la dernière série.</span><span class="sxs-lookup"><span data-stu-id="bbc46-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="bbc46-154">Vous pouvez retourner les erreurs avec le dernier appel ou appels antérieures.</span><span class="sxs-lookup"><span data-stu-id="bbc46-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="bbc46-155">Vous pouvez même ignorer l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="bbc46-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="bbc46-156">Si KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY est défini avec MAPI_DEFERRED_ERRORS, vous pouvez ignorer la demande de report d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bbc46-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="bbc46-157">Si MAPI_DEFERRED_ERRORS n’est pas définie dans _ulFlags_, l’erreur précédemment différée peut être renvoyé pour l’appel de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="bbc46-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="bbc46-158">Si un fournisseur de transport à distance fournit une implémentation de cette méthode fonctionnelle est facultative et dépend des autres options de conception dans votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="bbc46-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="bbc46-159">Si vous implémentez cette méthode, le faire conformément à la documentation ici.</span><span class="sxs-lookup"><span data-stu-id="bbc46-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="bbc46-160">Étant donné que les objets folder et les objets d’état ne sont pas traitées, au minimum implémentation d’un fournisseur de transport à distance de **SaveChanges** doit retourner S_OK sans réellement utilisé.</span><span class="sxs-lookup"><span data-stu-id="bbc46-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbc46-161">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="bbc46-161">Notes to callers</span></span>

<span data-ttu-id="bbc46-162">Si un client transmet KEEP_OPEN_READONLY, appelle la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) , puis appelle de nouveau **SaveChanges** , l’implémentation peut échouer.</span><span class="sxs-lookup"><span data-stu-id="bbc46-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="bbc46-163">Après avoir reçu MAPI_E_NO_ACCESS à partir d’un appel dans lequel vous définissez KEEP_OPEN_READWRITE, vous pourrez ont l’autorisation de lecture/écriture à l’objet.</span><span class="sxs-lookup"><span data-stu-id="bbc46-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="bbc46-164">Vous pouvez appeler **SaveChanges** , en passant l’indicateur KEEP_OPEN_READONLY ou aucun indicateur avec KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="bbc46-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="bbc46-165">Si un fournisseur prend en charge l’indicateur KEEP_OPEN_READWRITE dépend de l’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bbc46-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="bbc46-166">Pour indiquer que l’appel uniquement au niveau de l’objet après **SaveChanges** est **IUnknown::Release**, ne définissez aucun indicateur pour le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="bbc46-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="bbc46-167">Une erreur de **SaveChanges** indique qu’il ne pourrait pas conserver les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="bbc46-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="bbc46-168">Différents fournisseurs gèrent l’absence d’indicateurs de l’appel de **SaveChanges** différemment.</span><span class="sxs-lookup"><span data-stu-id="bbc46-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="bbc46-169">Certains fournisseurs de traitent cet état comme KEEP_OPEN_READONLY ; autres fournisseurs d’interprètent la même que KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="bbc46-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="bbc46-170">Toujours autres fournisseurs d’arrêter l’objet lorsqu’ils ne reçoivent pas les indicateurs de l’appel de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="bbc46-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="bbc46-171">Certaines propriétés, les propriétés calculées en général, ne peuvent pas être traitées jusqu'à ce que vous appeliez **SaveChanges** et, dans certains cas, la **version**.</span><span class="sxs-lookup"><span data-stu-id="bbc46-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="bbc46-172">Lorsque vous apportez des modifications en bloc, telles que l’enregistrement de pièces jointes à plusieurs messages, différer l’erreur de traitement en définissant l’indicateur MAPI_DEFERRED_ERRORS dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="bbc46-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="bbc46-173">Si vous enregistrez plusieurs pièces jointes à plusieurs messages, émettre un **SaveChanges** appeler pour chaque pièce jointe et un **SaveChanges** appeler à chaque message.</span><span class="sxs-lookup"><span data-stu-id="bbc46-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="bbc46-174">Définir l’indicateur MAPI_DEFERRED_ERRORS pour chaque appel de la pièce jointe et pour tous les messages à l’exception de la dernière série.</span><span class="sxs-lookup"><span data-stu-id="bbc46-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="bbc46-175">Si **SaveChanges** renvoie MAPI_E_OBJECT_CHANGED, vérifiez si l’objet d’origine a été modifié.</span><span class="sxs-lookup"><span data-stu-id="bbc46-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="bbc46-176">Dans ce cas, avertir l’utilisateur, qui peut demander que les modifications de remplacement les modifications précédentes ou enregistrement l’objet ailleurs.</span><span class="sxs-lookup"><span data-stu-id="bbc46-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="bbc46-177">Si l’objet d’origine a été supprimé, avertir l’utilisateur de leur donner la possibilité d’enregistrer l’objet dans un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="bbc46-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="bbc46-178">Vous ne pouvez pas appeler **SaveChanges** avec l’indicateur FORCE_SAVE sur un objet ouvert qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="bbc46-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="bbc46-179">Si **SaveChanges** renvoie une erreur, l’objet dont les modifications ont été le point d’être enregistrées reste ouvert, quel que soit les indicateurs définis dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="bbc46-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="bbc46-180">_ulFlags_ NON_EMS_XP_SAVE et SPAMFILTER_ONSAVE ne peuvent pas être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="bbc46-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="bbc46-181">Pour plus d’informations, voir [L’enregistrement des propriétés MAPI](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bbc46-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbc46-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbc46-182">See also</span></span>



[<span data-ttu-id="bbc46-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="bbc46-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="bbc46-184">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="bbc46-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="bbc46-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbc46-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="bbc46-186">L’enregistrement des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bbc46-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

