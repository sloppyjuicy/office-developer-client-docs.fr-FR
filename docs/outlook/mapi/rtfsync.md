---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436208"
---
# <a name="rtfsync"></a><span data-ttu-id="8b9fb-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="8b9fb-103">RTFSync</span></span>

<span data-ttu-id="8b9fb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b9fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b9fb-105">Garantit que le texte du message au format RTF (Rich Text Format) correspond à la version en texte brut.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="8b9fb-106">Il est nécessaire d'appeler cette fonction avant de lire la version RTF et après avoir modifié la version RTF.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b9fb-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8b9fb-107">Header file:</span></span>  <br/> |<span data-ttu-id="8b9fb-108">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="8b9fb-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8b9fb-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8b9fb-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="8b9fb-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="8b9fb-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="8b9fb-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8b9fb-111">Called by:</span></span>  <br/> |<span data-ttu-id="8b9fb-112">Applications clientes compatibles RTF et fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="8b9fb-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="8b9fb-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b9fb-113">Parameters</span></span>

<span data-ttu-id="8b9fb-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="8b9fb-114">_lpMessage_</span></span>
  
> <span data-ttu-id="8b9fb-115">dans Pointeur vers le message à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="8b9fb-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b9fb-116">_ulFlags_</span></span>
  
> <span data-ttu-id="8b9fb-117">dans Masque de des indicateurs utilisé pour indiquer que la version au format RTF ou texte brut du message a changé.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="8b9fb-118">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="8b9fb-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="8b9fb-119">RTF_SYNC_BODY_CHANGED: la version en texte brut du message a changé.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="8b9fb-120">RTF_SYNC_RTF_CHANGED: la version RTF du message a changé.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="8b9fb-121">Tous les autres bits dans le paramètre _ulFlags_ sont réservés à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="8b9fb-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="8b9fb-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="8b9fb-123">remarquer Pointeur vers une variable qui indique s'il existe un message mis à jour.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="8b9fb-124">TRUE s'il existe un message mis à jour, FALSe dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b9fb-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b9fb-125">Return value</span></span>

<span data-ttu-id="8b9fb-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b9fb-126">S_OK</span></span> 
  
> <span data-ttu-id="8b9fb-127">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b9fb-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b9fb-128">Remarks</span></span>

<span data-ttu-id="8b9fb-129">Si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquANTE ou a la valeur false, avant de lire la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la fonction **RTFSync** doit être appelée avec le RTF_SYNC_BODY_ Indicateur modifié.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="8b9fb-130">Si l'indicateur STORE_RTF_OK n'est pas défini dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), cette fonction doit être appelée avec l'indicateur RTF_SYNC_RTF_CHANGED défini après la modification de **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="8b9fb-131">Si **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ont été modifiés, la fonction **RTFSync** doit être appelée avec les deux indicateurs définis.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="8b9fb-132">Si la valeur du paramètre _lpfMessageUpdated_ est définie sur true, la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) doit être appelée pour le message.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="8b9fb-133">Si **SaveChanges** n'est pas appelé, les modifications ne seront pas enregistrées dans le message.</span><span class="sxs-lookup"><span data-stu-id="8b9fb-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="8b9fb-134">Les fournisseurs de banques de messages peuvent utiliser **RTFSync** pour synchroniser les propriétés **PR_BODY** et **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="8b9fb-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="8b9fb-135">Pour plus d'informations, consultez la rubrique [prise en charge de texte RTF pour les fournisseurs de banque de messages](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="8b9fb-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b9fb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b9fb-136">See also</span></span>

- [<span data-ttu-id="8b9fb-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="8b9fb-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

