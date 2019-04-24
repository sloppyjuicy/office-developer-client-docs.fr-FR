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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348845"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="897d8-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="897d8-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="897d8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="897d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="897d8-105">Affiche la boîte de dialogue Carnet d'adresses Outlook.</span><span class="sxs-lookup"><span data-stu-id="897d8-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="897d8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="897d8-106">Parameters</span></span>

 <span data-ttu-id="897d8-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="897d8-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="897d8-108">[in, out] Pointeur vers un handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="897d8-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="897d8-109">Lors de l'entrée, un descripteur de fenêtre doit toujours être passé.</span><span class="sxs-lookup"><span data-stu-id="897d8-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="897d8-110">Lors de la sortie, si le membre **ulFlags** du paramètre _lpAdrParms_ est défini sur DIALOG_SDI, le handle de fenêtre de la boîte de dialogue non modale est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="897d8-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="897d8-111">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="897d8-111">See Remarks.</span></span> 
    
 <span data-ttu-id="897d8-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="897d8-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="897d8-113">[in, out] Pointeur vers une structure [ADRPARM](adrparm.md) qui contrôle la présentation et le comportement de la boîte de dialogue d'adresse.</span><span class="sxs-lookup"><span data-stu-id="897d8-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="897d8-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="897d8-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="897d8-115">[in, out] Pointeur vers un pointeur vers une structure [ADRLIST](adrlist.md) qui contient des informations sur le destinataire.</span><span class="sxs-lookup"><span data-stu-id="897d8-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="897d8-116">Lors de l'entrée, ce paramètre peut être NULL ou pointer vers un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="897d8-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="897d8-117">Lors de la sortie, ce paramètre pointe vers un pointeur vers des informations de destinataire valides.</span><span class="sxs-lookup"><span data-stu-id="897d8-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="897d8-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="897d8-118">Return value</span></span>

<span data-ttu-id="897d8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="897d8-119">S_OK</span></span> 
  
> <span data-ttu-id="897d8-120">La boîte de dialogue adresse commune s'est affichée.</span><span class="sxs-lookup"><span data-stu-id="897d8-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="897d8-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="897d8-121">Remarks</span></span>

<span data-ttu-id="897d8-122">Si le membre **ulFlags** du paramètre _lpAdrParms_ est défini sur DIALOG_SDI anticipant le retour du handle de fenêtre de la boîte de dialogue non modale sur la sortie, il est ignoré dans Outlook; la version modale de la boîte de dialogue est toujours affichée dans les clients autres que Outlook.</span><span class="sxs-lookup"><span data-stu-id="897d8-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="897d8-123">La structure **ADRLIST** transmise par MAPI à l'appelant via le paramètre _lppAdrList_ contient un tableau de structures [ADRENTRY](adrentry.md) , une structure pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="897d8-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="897d8-124">Lorsqu'elle est transmise à la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) d'un message sortant dans le paramètre _lpMods_ , la structure **ADRLIST** peut être utilisée pour mettre à jour sa liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="897d8-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="897d8-125">Chaque structure **ADRENTRY** de la structure **ADRLIST** contient zéro ou plusieurs structures [SPropValue](spropvalue.md) , une structure pour chaque jeu de propriétés pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="897d8-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="897d8-126">Il peut y avoir zéro structure **SPropValue** lorsque la boîte de dialogue présentée par la méthode **Address** est utilisée pour supprimer un destinataire.</span><span class="sxs-lookup"><span data-stu-id="897d8-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="897d8-127">Lorsqu'il existe une ou plusieurs structures **SPropValue** , la structure **ADRENTRY** correspondante est utilisée pour ajouter ou mettre à jour un destinataire.</span><span class="sxs-lookup"><span data-stu-id="897d8-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="897d8-128">Le destinataire peut être résolu, ce qui indique que l'une des structures **SPropValue** décrit la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du destinataire ou non résolu, ce qui indique que la propriété **PR_ENTRYID** est sans.</span><span class="sxs-lookup"><span data-stu-id="897d8-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="897d8-129">En plus de la propriété **PR_ENTRYID**, les destinataires résolus incluent les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="897d8-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="897d8-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="897d8-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="897d8-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="897d8-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="897d8-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="897d8-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="897d8-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="897d8-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="897d8-134">La structure **ADRLIST** que l'appelant passe peut avoir une taille différente de celle renvoyée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="897d8-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="897d8-135">Si MAPI doit renvoyer une structure **ADRLIST** plus grande, il libère la structure d'origine et alloue une nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="897d8-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="897d8-136">Lorsque vous allouez de la mémoire pour la structure **ADRLIST** , allouez séparément la mémoire pour chaque structure **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="897d8-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="897d8-137">Pour plus d'informations sur la façon d'allouer et de libérer des structures **ADRLIST** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md) .</span><span class="sxs-lookup"><span data-stu-id="897d8-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="897d8-138">L' **adresse** est renvoyée immédiatement si l'indicateur DIALOG_SDI est défini dans le membre **ulFlags** de la structure **ADRPARM** dans le paramètre _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="897d8-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="897d8-139">L'indicateur DIALOG_SDI est ignoré pour les clients non-Outlook.</span><span class="sxs-lookup"><span data-stu-id="897d8-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="897d8-140">Si DIALOG_SDI est ignoré, la version modale de la boîte de dialogue s'affiche et un pointeur vers un descripteur ne doit pas être attendu dans _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="897d8-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="897d8-141">**Address** prend en charge les chaînes de caractères Unicode dans la structure **ADRPARM** si AB_UNICODEUI a été spécifié dans le membre **ulFlags** de **ADRPARM** dans le paramètre _lpAdrParms_ et qu'il prend en charge les chaînes de caractères Unicode dans \*\* ADRLIST\*\*.</span><span class="sxs-lookup"><span data-stu-id="897d8-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="897d8-142">Les chaînes Unicode sont converties au format MBCS (Multibyte Character String) avant d'être affichées dans la boîte de dialogue Carnet d'adresses Outlook.</span><span class="sxs-lookup"><span data-stu-id="897d8-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="897d8-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="897d8-143">MFCMAPI reference</span></span>

<span data-ttu-id="897d8-144">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="897d8-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="897d8-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="897d8-145">**File**</span></span>|<span data-ttu-id="897d8-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="897d8-146">**Function**</span></span>|<span data-ttu-id="897d8-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="897d8-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="897d8-148">MAPIStoreFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="897d8-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="897d8-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="897d8-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="897d8-150">MFCMAPI utilise la méthode **Address** pour permettre à l'utilisateur de sélectionner la boîte aux lettres à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="897d8-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="897d8-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="897d8-151">See also</span></span>



[<span data-ttu-id="897d8-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="897d8-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="897d8-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="897d8-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="897d8-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="897d8-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="897d8-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="897d8-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="897d8-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="897d8-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="897d8-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="897d8-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="897d8-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="897d8-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="897d8-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="897d8-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="897d8-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="897d8-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="897d8-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="897d8-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="897d8-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="897d8-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="897d8-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="897d8-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="897d8-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="897d8-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="897d8-165">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="897d8-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="897d8-166">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="897d8-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

