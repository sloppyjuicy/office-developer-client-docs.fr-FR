---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 524bbfe5f40a66585fb4ed4463b057ca6a0c881a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586801"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="198e1-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="198e1-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="198e1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="198e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="198e1-105">Affiche la boîte de dialogue adresses.</span><span class="sxs-lookup"><span data-stu-id="198e1-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="198e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="198e1-106">Parameters</span></span>

 <span data-ttu-id="198e1-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="198e1-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="198e1-108">[entrée, sortie] Pointeur vers le handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="198e1-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="198e1-109">À l’entrée, un handle de fenêtre doit toujours être transmis.</span><span class="sxs-lookup"><span data-stu-id="198e1-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="198e1-110">Dans la sortie, si l’indicateur DIALOG_SDI est défini dans la structure [ADRPARM](adrparm.md) désignée par le paramètre _lpAdrParms_ , le handle de fenêtre de la boîte de dialogue non modale est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="198e1-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="198e1-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="198e1-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="198e1-112">[entrée, sortie] Un pointeur vers une structure **ADRPARM** qui contrôle la présentation et le comportement de la boîte de dialogue adresses.</span><span class="sxs-lookup"><span data-stu-id="198e1-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="198e1-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="198e1-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="198e1-114">[entrée, sortie] Pointeur vers un pointeur vers une liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="198e1-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="198e1-115">À l’entrée, cette liste est la liste actuelle des destinataires d’un message ou valeur NULL, si aucune liste de ce type n’existe.</span><span class="sxs-lookup"><span data-stu-id="198e1-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="198e1-116">Dans la sortie, _lppAdrList_ pointe vers une liste mise à jour de destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="198e1-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="198e1-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="198e1-117">Return value</span></span>

<span data-ttu-id="198e1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="198e1-118">S_OK</span></span> 
  
> <span data-ttu-id="198e1-119">La boîte de dialogue adresse a été correctement affichée.</span><span class="sxs-lookup"><span data-stu-id="198e1-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="198e1-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="198e1-120">Remarks</span></span>

<span data-ttu-id="198e1-121">La méthode **IMAPISupport::Address** est implémentée pour les objets de prise en charge du fournisseur adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="198e1-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="198e1-122">Fournisseurs de carnet d’adresses appellent **adresse** pour créer ou mettre à jour une liste de destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="198e1-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="198e1-123">Chaque destinataire est décrite dans une structure [ADRENTRY](adrentry.md) qui est incluse dans la structure [ADRLIST](adrlist.md) désignée par le paramètre _lppAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="198e1-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="198e1-124">La structure **ADRENTRY** contient un tableau de valeurs de propriété de destinataire, un d'entre eux est le type du destinataire, ou la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="198e1-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="198e1-125">Cette structure **ADRLIST** peut être passée à un client à utiliser en tant que paramètre à un appel à [IMessage::ModifyRecipients](imessage-modifyrecipients.md) _lpMods_ .</span><span class="sxs-lookup"><span data-stu-id="198e1-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="198e1-126">Chaque destinataire de la structure **ADRLIST** peut être soit résolu, ce qui indique qu’une de ses valeurs de propriété est sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ou non, qui indique que la propriété **PR_ENTRYID** est manquante.</span><span class="sxs-lookup"><span data-stu-id="198e1-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="198e1-127">Outre **PR_ENTRYID**, destinataires résolus comprennent les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="198e1-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="198e1-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="198e1-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="198e1-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="198e1-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="198e1-130">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="198e1-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="198e1-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="198e1-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="198e1-132">En règle générale, les destinataires non résolus incluent uniquement **PR_DISPLAY_NAME** et **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="198e1-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="198e1-133">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="198e1-133">Notes to callers</span></span>

<span data-ttu-id="198e1-134">La structure **ADRLIST** qui transmet l’appelant peut être une taille différente de la structure renvoie MAPI.</span><span class="sxs-lookup"><span data-stu-id="198e1-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="198e1-135">Lorsque vous affectez la mémoire pour la structure **ADRLIST** , allouer la mémoire pour chaque structure [SPropValue](spropvalue.md) séparément.</span><span class="sxs-lookup"><span data-stu-id="198e1-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="198e1-136">Utilisez les pointeurs vers les fonctions d’allocation de mémoire MAPI à votre fonction [ABProviderInit](abproviderinit.md) d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="198e1-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="198e1-137">Allouer de la mémoire avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour **ADRLIST** et chaque structure de valeur de propriété dans les structures **ADRENTRY** dans **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="198e1-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="198e1-138">Si **l’adresse** doit renvoyer une plus grande structure **ADRLIST** , ou si vous avez passé NULL pour _lppAdrList_, **adresse** libère la structure d’origine et alloue un nouveau.</span><span class="sxs-lookup"><span data-stu-id="198e1-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="198e1-139">**Adresse** également alloue les structures de valeur de propriété supplémentaires dans la structure **ADRLIST** et libère anciens comme il convient.</span><span class="sxs-lookup"><span data-stu-id="198e1-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="198e1-140">Pour plus d’informations sur la gestion de la mémoire pour les structures **ADRLIST** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="198e1-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="198e1-141">**Adresse** renvoie immédiatement si l’indicateur DIALOG_SDI a été défini dans la structure **ADRPARM** dans le paramètre _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="198e1-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="198e1-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="198e1-142">See also</span></span>



[<span data-ttu-id="198e1-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="198e1-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="198e1-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="198e1-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="198e1-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="198e1-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="198e1-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="198e1-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="198e1-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="198e1-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="198e1-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="198e1-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="198e1-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="198e1-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="198e1-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="198e1-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="198e1-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="198e1-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="198e1-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="198e1-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="198e1-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="198e1-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="198e1-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="198e1-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="198e1-155">Propriété canonique PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="198e1-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="198e1-156">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="198e1-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="198e1-157">Propriété canonique PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="198e1-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="198e1-158">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="198e1-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="198e1-159">Propriété canonique PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="198e1-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="198e1-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="198e1-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="198e1-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="198e1-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="198e1-162">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="198e1-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="198e1-163">Gestion de la mémoire pour les structures ADRLIST et SRowSet</span><span class="sxs-lookup"><span data-stu-id="198e1-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

