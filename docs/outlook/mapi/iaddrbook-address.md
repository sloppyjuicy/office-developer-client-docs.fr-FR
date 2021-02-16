---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407906"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="d0b2b-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="d0b2b-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="d0b2b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0b2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0b2b-105">Affiche la boîte de dialogue carnet d’adresses Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="d0b2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0b2b-106">Parameters</span></span>

 <span data-ttu-id="d0b2b-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d0b2b-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d0b2b-108">[in, out] Pointeur vers un handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="d0b2b-109">Lors de l’entrée, une poignée de fenêtre doit toujours être passée.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="d0b2b-110">En sortie, si le membre **ulFlags** du paramètre  _lpAdrParms_ est DIALOG_SDI, le handle de fenêtre de la boîte de dialogue sans mode est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="d0b2b-111">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-111">See Remarks.</span></span> 
    
 <span data-ttu-id="d0b2b-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="d0b2b-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="d0b2b-113">[in, out] Pointeur vers une structure [ADRPARM](adrparm.md) qui contrôle la présentation et le comportement de la boîte de dialogue d’adresse.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="d0b2b-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="d0b2b-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="d0b2b-115">[in, out] Pointeur vers un pointeur vers une structure [ADRLIST](adrlist.md) qui contient des informations sur le destinataire.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="d0b2b-116">Lors de l’entrée, ce paramètre peut être NULL ou pointer vers un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="d0b2b-117">En sortie, ce paramètre pointe vers un pointeur vers des informations de destinataire valides.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d0b2b-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0b2b-118">Return value</span></span>

<span data-ttu-id="d0b2b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0b2b-119">S_OK</span></span> 
  
> <span data-ttu-id="d0b2b-120">La boîte de dialogue d’adresse commune a été affichée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0b2b-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0b2b-121">Remarks</span></span>

<span data-ttu-id="d0b2b-122">Si le membre **ulFlags** du paramètre  _lpAdrParms_ a la valeur DIALOG_SDI anticipant le retour de la poignée de fenêtre de la boîte de dialogue sans mode lors de la sortie, il est ignoré dans Outlook ; La version modale de la boîte de dialogue est toujours affichée dans les clients non Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="d0b2b-123">La structure **ADRLIST** transmise par MAPI à l’appelant via le paramètre  _lppAdrList_ contient un tableau de structures [ADRENTRY,](adrentry.md) une structure pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="d0b2b-124">Lorsqu’elle est transmise à la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) d’un message sortant dans le paramètre  _lpMods,_ la structure **ADRLIST** peut être utilisée pour mettre à jour sa liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="d0b2b-125">Chaque structure **ADRENTRY** dans la structure **ADRLIST** contient zéro ou plusieurs structures [SPropValue,](spropvalue.md) une structure pour chaque propriété définie pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="d0b2b-126">Il ne peut y avoir aucune structure **SPropValue** lorsque la boîte de dialogue présentée par la méthode **Address** est utilisée pour supprimer un destinataire.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="d0b2b-127">Lorsqu’il existe une ou plusieurs structures **SPropValue,** la structure **ADRENTRY** correspondante est utilisée pour ajouter ou mettre à jour un destinataire.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="d0b2b-128">Le destinataire peut être résolu, ce qui indique que l’une des structures **SPropValue** décrit la propriété **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)du destinataire, ou non résolue, ce qui indique que la propriété **PR_ENTRYID** est manquante.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="d0b2b-129">En plus de **PR_ENTRYID,** les destinataires résolus incluent les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0b2b-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="d0b2b-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d0b2b-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d0b2b-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d0b2b-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="d0b2b-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d0b2b-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d0b2b-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d0b2b-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="d0b2b-134">La structure **ADRLIST** que l’appelant transmet peut être d’une taille différente de la structure que MAPI renvoie.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="d0b2b-135">Si MAPI doit renvoyer une structure **ADRLIST** plus grande, il libère la structure d’origine et en alloue une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="d0b2b-136">Lorsque vous allouez de la mémoire pour la structure **ADRLIST,** allouez la mémoire pour chaque structure **SPropValue** séparément.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="d0b2b-137">Pour plus d’informations sur l’allocation et la gratuité des structures **ADRLIST,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="d0b2b-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="d0b2b-138">**L’adresse** renvoie immédiatement si l’DIALOG_SDI est définie dans le membre **ulFlags** de la structure **ADRPARM** dans le paramètre _lpAdrParms._</span><span class="sxs-lookup"><span data-stu-id="d0b2b-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="d0b2b-139">L DIALOG_SDI est ignoré pour les clients non Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="d0b2b-140">Si DIALOG_SDI est ignoré, la version modale de la boîte de dialogue s’affiche et un pointeur vers un handle ne doit pas être attendu dans  _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="d0b2b-141">**Address** prend en charge les chaînes de caractères Unicode dans la structure **ADRPARM** si AB_UNICODEUI a été spécifié dans le membre **ulFlags** d’ADRPARM dans le paramètre _lpAdrParms_ et prend en charge les chaînes de caractères Unicode dans **ADRLIST**. </span><span class="sxs-lookup"><span data-stu-id="d0b2b-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="d0b2b-142">Les chaînes Unicode sont converties au format de chaîne de caractères multioctets (MBCS) avant d’être affichées dans la boîte de dialogue du carnet d’adresses Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d0b2b-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d0b2b-143">MFCMAPI reference</span></span>

<span data-ttu-id="d0b2b-144">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d0b2b-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d0b2b-145">**File**</span></span>|<span data-ttu-id="d0b2b-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d0b2b-146">**Function**</span></span>|<span data-ttu-id="d0b2b-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d0b2b-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0b2b-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d0b2b-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d0b2b-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="d0b2b-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="d0b2b-150">MFCMAPI utilise la méthode **Address** pour permettre à l’utilisateur de sélectionner la boîte aux lettres à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="d0b2b-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0b2b-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0b2b-151">See also</span></span>



[<span data-ttu-id="d0b2b-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="d0b2b-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="d0b2b-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d0b2b-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="d0b2b-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="d0b2b-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="d0b2b-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="d0b2b-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="d0b2b-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="d0b2b-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="d0b2b-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d0b2b-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="d0b2b-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="d0b2b-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="d0b2b-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d0b2b-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d0b2b-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="d0b2b-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="d0b2b-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d0b2b-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d0b2b-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d0b2b-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="d0b2b-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="d0b2b-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="d0b2b-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d0b2b-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="d0b2b-165">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d0b2b-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d0b2b-166">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d0b2b-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

