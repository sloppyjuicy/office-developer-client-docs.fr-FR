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
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407318"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="63290-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="63290-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="63290-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63290-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63290-105">Affiche la boîte de dialogue Adresse commune.</span><span class="sxs-lookup"><span data-stu-id="63290-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="63290-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63290-106">Parameters</span></span>

 <span data-ttu-id="63290-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="63290-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="63290-108">[in, out] Pointeur vers le handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="63290-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="63290-109">Lors de l’entrée, une poignée de fenêtre doit toujours être passée.</span><span class="sxs-lookup"><span data-stu-id="63290-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="63290-110">En sortie, si l’indicateur DIALOG_SDI est définie dans la structure [ADRPARM](adrparm.md) pointée par le paramètre  _lpAdrParms,_ la poignée de fenêtre de la boîte de dialogue sans mode est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="63290-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="63290-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="63290-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="63290-112">[in, out] Pointeur vers une structure **ADRPARM** qui contrôle la présentation et le comportement de la boîte de dialogue d’adresse.</span><span class="sxs-lookup"><span data-stu-id="63290-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="63290-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="63290-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="63290-114">[in, out] Pointeur vers un pointeur vers une liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="63290-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="63290-115">Lors de l’entrée, cette liste est soit la liste actuelle des destinataires dans un message, soit NULL, si cette liste n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="63290-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="63290-116">Lors de la sortie,  _lppAdrList_ pointe vers une liste mise à jour des destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="63290-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="63290-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63290-117">Return value</span></span>

<span data-ttu-id="63290-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="63290-118">S_OK</span></span> 
  
> <span data-ttu-id="63290-119">La boîte de dialogue d’adresse a été affichée avec succès.</span><span class="sxs-lookup"><span data-stu-id="63290-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63290-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="63290-120">Remarks</span></span>

<span data-ttu-id="63290-121">La **méthode IMAPISupport::Address** est implémentée pour les objets de prise en charge du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="63290-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="63290-122">Les fournisseurs de carnets d’adresses appellent **l’adresse** pour créer ou mettre à jour une liste de destinataires de message.</span><span class="sxs-lookup"><span data-stu-id="63290-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="63290-123">Chaque destinataire est décrit dans une structure [ADRENTRY](adrentry.md) incluse dans la structure [ADRLIST](adrlist.md) pointée par le _paramètre lppAdrList._</span><span class="sxs-lookup"><span data-stu-id="63290-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="63290-124">La structure **ADRENTRY** contient un tableau de valeurs de propriété de destinataire, l’une d’entre elles est le type du destinataire ou la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63290-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="63290-125">Cette structure **ADRLIST** peut être transmise à un client pour l’utiliser comme paramètre  _lpMods_ dans un appel à [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="63290-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="63290-126">Chaque destinataire de la structure **ADRLIST** peut être résolu, ce qui indique que l’une de ses valeurs de propriété est sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou non résolue, ce qui indique que la propriété **PR_ENTRYID est** manquante.</span><span class="sxs-lookup"><span data-stu-id="63290-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="63290-127">En plus de **PR_ENTRYID,** les destinataires résolus incluent les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="63290-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="63290-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="63290-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="63290-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63290-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="63290-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63290-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="63290-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63290-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="63290-132">Les destinataires non résolus incluent généralement uniquement **PR_DISPLAY_NAME** et **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="63290-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="63290-133">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="63290-133">Notes to callers</span></span>

<span data-ttu-id="63290-134">La structure **ADRLIST** que l’appelant transmet peut être d’une taille différente de la structure que MAPI renvoie.</span><span class="sxs-lookup"><span data-stu-id="63290-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="63290-135">Lorsque vous allouez de la mémoire pour la structure **ADRLIST,** allouez la mémoire pour chaque structure [SPropValue](spropvalue.md) séparément.</span><span class="sxs-lookup"><span data-stu-id="63290-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="63290-136">Utilisez les pointeurs vers les fonctions d’allocation de mémoire MAPI transmises à votre fonction [ABProviderInit](abproviderinit.md) pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="63290-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="63290-137">Allouez de la mémoire avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour **ADRLIST** et chaque structure de valeur de propriété dans les structures **ADRENTRY** dans **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="63290-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="63290-138">Si **Address** doit renvoyer une structure **ADRLIST** plus grande, ou si vous avez passé NULL pour  _lppAdrList_, **Address** libère la structure d’origine et en alloue une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="63290-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="63290-139">**L’adresse** alloue également des structures de valeur de propriété supplémentaires dans la structure **ADRLIST** et libère les anciennes selon le cas.</span><span class="sxs-lookup"><span data-stu-id="63290-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="63290-140">Pour plus d’informations sur la gestion de la mémoire pour les structures **ADRLIST,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="63290-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="63290-141">**L’adresse** renvoie immédiatement si DIALOG_SDI’indicateur a été définie dans la structure **ADRPARM** dans le paramètre _lpAdrParms._</span><span class="sxs-lookup"><span data-stu-id="63290-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63290-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63290-142">See also</span></span>



[<span data-ttu-id="63290-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="63290-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="63290-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="63290-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="63290-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="63290-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="63290-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="63290-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="63290-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="63290-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="63290-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="63290-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="63290-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="63290-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="63290-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="63290-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="63290-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="63290-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="63290-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="63290-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="63290-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="63290-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="63290-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="63290-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="63290-155">Propriété canonique PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="63290-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="63290-156">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="63290-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="63290-157">Propriété canonique PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="63290-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="63290-158">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="63290-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="63290-159">Propriété canonique PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="63290-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="63290-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="63290-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="63290-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="63290-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="63290-162">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63290-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="63290-163">Gestion de la mémoire pour les structures ADRLIST et SRowSet</span><span class="sxs-lookup"><span data-stu-id="63290-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

