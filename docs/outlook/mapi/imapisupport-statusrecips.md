---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cda629cf78d3f7915b64c130867ed4f8ebbd6f8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563841"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="d408a-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="d408a-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="d408a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d408a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d408a-105">Génère des rapports de remise et de non-remise.</span><span class="sxs-lookup"><span data-stu-id="d408a-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="d408a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d408a-106">Parameters</span></span>

 <span data-ttu-id="d408a-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="d408a-107">_lpMessage_</span></span>
  
> <span data-ttu-id="d408a-108">[in] Pointeur vers le message pour lequel le rapport doit être généré.</span><span class="sxs-lookup"><span data-stu-id="d408a-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="d408a-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="d408a-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="d408a-110">[in] Un pointeur vers une structure [ADRLIST](adrlist.md) qui décrit les destinataires du message indiqué par _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="d408a-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d408a-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d408a-111">Return value</span></span>

<span data-ttu-id="d408a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d408a-112">S_OK</span></span> 
  
> <span data-ttu-id="d408a-113">Le rapport a été généré.</span><span class="sxs-lookup"><span data-stu-id="d408a-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="d408a-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="d408a-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="d408a-115">L’appel a réussi, mais aucune option de destinataire pour ce type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="d408a-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="d408a-116">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="d408a-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="d408a-117">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="d408a-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="d408a-118">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="d408a-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d408a-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="d408a-119">Remarks</span></span>

<span data-ttu-id="d408a-120">La méthode **IMAPISupport::StatusRecips** est implémentée pour les objets de prise en charge de fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="d408a-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="d408a-121">Fournisseurs de transport appeler **StatusRecips** pour demander qu’envoi MAPI un rapport de remise ou de non-remise à un ensemble d’une ou plusieurs des destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="d408a-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d408a-122">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="d408a-122">Notes to callers</span></span>

<span data-ttu-id="d408a-123">Vous pouvez appeler **StatusRecips** plusieurs fois lors du traitement d’un message.</span><span class="sxs-lookup"><span data-stu-id="d408a-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="d408a-124">Toutefois, si vous appelez **StatusRecips** pour un message ouvert, faites votre possible pour toutes les informations de remise et de non-remise pour les destinataires du message et appeler **StatusRecips** pour cette liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="d408a-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="d408a-125">Un point unique de la collection est important, car plusieurs appels **StatusRecips** pour un destinataire peuvent générer plusieurs rapports identiques envoyés.</span><span class="sxs-lookup"><span data-stu-id="d408a-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="d408a-126">Stocker les propriétés qui sont associées à la remise du message ou de non-remise dans la structure **ADRLIST** indiquée par le paramètre _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="d408a-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="d408a-127">Pour une liste complète des propriétés obligatoires et facultatifs de rapports de remise et des rapports de non-remise, voir [Propriétés de Message de rapport requises](required-report-message-properties.md) et les [Propriétés de Message de rapport facultatif](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d408a-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="d408a-128">Allouer de la mémoire pour la structure **ADRLIST** dans _lpRecipList_ en utilisant les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="d408a-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="d408a-129">MAPI libère la mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **StatusRecips** réussit.</span><span class="sxs-lookup"><span data-stu-id="d408a-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="d408a-130">Pour une vue d’ensemble des rapports de remise et de non-remise, voir [Les Messages de rapport MAPI](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d408a-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d408a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d408a-131">See also</span></span>



[<span data-ttu-id="d408a-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d408a-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="d408a-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="d408a-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="d408a-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="d408a-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="d408a-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="d408a-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="d408a-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d408a-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d408a-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="d408a-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="d408a-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d408a-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d408a-139">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d408a-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

