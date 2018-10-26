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
ms.openlocfilehash: a13696b355e6fd815cd6bda42843505d9fc3d1f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579955"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="7622d-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="7622d-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="7622d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7622d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7622d-105">Affiche la boîte de dialogue de carnet d’adresse Outlook.</span><span class="sxs-lookup"><span data-stu-id="7622d-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="7622d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7622d-106">Parameters</span></span>

 <span data-ttu-id="7622d-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7622d-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="7622d-108">[entrée, sortie] Pointeur vers un handle de la fenêtre parent de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7622d-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="7622d-109">À l’entrée, un handle de fenêtre doit toujours être transmis.</span><span class="sxs-lookup"><span data-stu-id="7622d-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="7622d-110">Dans la sortie, si le membre **ulFlags** du paramètre _lpAdrParms_ est défini sur DIALOG_SDI, le handle de fenêtre de la boîte de dialogue non modale est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7622d-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="7622d-111">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="7622d-111">See Remarks.</span></span> 
    
 <span data-ttu-id="7622d-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="7622d-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="7622d-113">[entrée, sortie] Un pointeur vers une structure [ADRPARM](adrparm.md) qui contrôle la présentation et le comportement de la boîte de dialogue adresses.</span><span class="sxs-lookup"><span data-stu-id="7622d-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="7622d-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="7622d-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="7622d-115">[entrée, sortie] Pointeur vers un pointeur vers une structure [ADRLIST](adrlist.md) qui contient les informations relatives au destinataire.</span><span class="sxs-lookup"><span data-stu-id="7622d-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="7622d-116">À l’entrée, ce paramètre peut être NULL ou pointez sur un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="7622d-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="7622d-117">Dans la sortie, ce paramètre pointe vers un pointeur vers les informations relatives au destinataire valides.</span><span class="sxs-lookup"><span data-stu-id="7622d-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7622d-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7622d-118">Return value</span></span>

<span data-ttu-id="7622d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7622d-119">S_OK</span></span> 
  
> <span data-ttu-id="7622d-120">La boîte de dialogue adresse a été correctement affichée.</span><span class="sxs-lookup"><span data-stu-id="7622d-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7622d-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="7622d-121">Remarks</span></span>

<span data-ttu-id="7622d-122">Si le membre **ulFlags** du paramètre _lpAdrParms_ est défini sur DIALOG_SDI anticipation le retour de handle de fenêtre de la boîte de dialogue non modale en sortie, il est ignoré dans Outlook ; la version de la boîte de dialogue modale est toujours affichée dans les clients non Outlook.</span><span class="sxs-lookup"><span data-stu-id="7622d-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="7622d-123">La structure **ADRLIST** transmise par MAPI à l’appelant via le paramètre _lppAdrList_ contient un tableau de structures [ADRENTRY](adrentry.md) , une structure pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="7622d-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="7622d-124">Lorsqu’il est passé à la méthode de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) d’un message sortant dans le paramètre _lpMods_ , la structure **ADRLIST** peut être utilisée pour mettre à jour sa liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="7622d-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="7622d-125">Chaque structure **ADRENTRY** dans la structure **ADRLIST** contient zéro ou plusieurs structures [SPropValue](spropvalue.md) , une structure pour chaque propriété définie pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="7622d-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="7622d-126">Il peut être zéro structures **SPropValue** lorsque la boîte de dialogue présentée par la méthode **adresse** est utilisée pour supprimer un destinataire.</span><span class="sxs-lookup"><span data-stu-id="7622d-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="7622d-127">Lorsqu’il existe une ou plusieurs structures **SPropValue** , la structure **ADRENTRY** correspondante est utilisée pour ajouter ou mettre à jour d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="7622d-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="7622d-128">Le destinataire peut être résolu, ce qui indique qu’une des structures **SPropValue** décrit la propriété du destinataire **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ou non résolus, qui indique que la propriété **PR_ENTRYID** est manquante.</span><span class="sxs-lookup"><span data-stu-id="7622d-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="7622d-129">Outre **PR_ENTRYID**, destinataires résolus comprennent les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="7622d-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="7622d-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7622d-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="7622d-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7622d-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="7622d-132">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7622d-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="7622d-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7622d-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="7622d-134">La structure **ADRLIST** qui transmet l’appelant peut être une taille différente de la structure renvoie MAPI.</span><span class="sxs-lookup"><span data-stu-id="7622d-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="7622d-135">Si MAPI doit renvoyer une plus grande structure **ADRLIST** , il libère la structure d’origine et alloue un nouveau.</span><span class="sxs-lookup"><span data-stu-id="7622d-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="7622d-136">Lorsque vous affectez la mémoire pour la structure **ADRLIST** , allouer la mémoire pour chaque structure **SPropValue** séparément.</span><span class="sxs-lookup"><span data-stu-id="7622d-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="7622d-137">Pour plus d’informations sur la façon d’allouer et libérer les structures **ADRLIST** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="7622d-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="7622d-138">**Adresse** renvoie immédiatement si l’indicateur DIALOG_SDI est défini dans le membre **ulFlags** de la structure **ADRPARM** dans le paramètre _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="7622d-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="7622d-139">L’indicateur DIALOG_SDI est ignorée pour les clients non Outlook.</span><span class="sxs-lookup"><span data-stu-id="7622d-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="7622d-140">Si DIALOG_SDI est ignorée, la version de la boîte de dialogue modale s’affiche et un pointeur vers un handle ne doit pas dans _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="7622d-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="7622d-141">**Adresse** prend en charge les chaînes de caractères Unicode dans la structure **ADRPARM** si AB_UNICODEUI a été spécifié dans le membre **ulFlags** de **ADRPARM** dans le paramètre _lpAdrParms_ , et il prend en charge les chaînes de caractères Unicode dans \*\* ADRLIST\*\*.</span><span class="sxs-lookup"><span data-stu-id="7622d-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="7622d-142">Les chaînes Unicode sont convertis au format de chaîne (MBCS) codés avant qu’elles sont affichées dans la boîte de dialogue de carnet d’adresse Outlook.</span><span class="sxs-lookup"><span data-stu-id="7622d-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7622d-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7622d-143">MFCMAPI reference</span></span>

<span data-ttu-id="7622d-144">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7622d-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7622d-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="7622d-145">**File**</span></span>|<span data-ttu-id="7622d-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="7622d-146">**Function**</span></span>|<span data-ttu-id="7622d-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="7622d-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7622d-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="7622d-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7622d-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="7622d-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="7622d-150">MFCMAPI utilise la méthode **adresse** pour autoriser l’utilisateur à sélectionner les boîtes aux lettres à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="7622d-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7622d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7622d-151">See also</span></span>



[<span data-ttu-id="7622d-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="7622d-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="7622d-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="7622d-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="7622d-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="7622d-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="7622d-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="7622d-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="7622d-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="7622d-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="7622d-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7622d-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="7622d-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="7622d-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="7622d-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7622d-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="7622d-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="7622d-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="7622d-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7622d-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7622d-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7622d-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="7622d-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7622d-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="7622d-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7622d-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="7622d-165">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="7622d-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7622d-166">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="7622d-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

