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
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408767"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="65fa9-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="65fa9-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="65fa9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65fa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65fa9-105">Génère des rapports de remise et de livraison.</span><span class="sxs-lookup"><span data-stu-id="65fa9-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="65fa9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65fa9-106">Parameters</span></span>

 <span data-ttu-id="65fa9-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="65fa9-107">_lpMessage_</span></span>
  
> <span data-ttu-id="65fa9-108">dans Pointeur vers le message pour lequel le rapport doit être généré.</span><span class="sxs-lookup"><span data-stu-id="65fa9-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="65fa9-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="65fa9-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="65fa9-110">dans Pointeur vers une structure [ADRLIST](adrlist.md) qui décrit les destinataires du message désigné par _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="65fa9-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65fa9-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65fa9-111">Return value</span></span>

<span data-ttu-id="65fa9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="65fa9-112">S_OK</span></span> 
  
> <span data-ttu-id="65fa9-113">Le rapport a été généré avec succès.</span><span class="sxs-lookup"><span data-stu-id="65fa9-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="65fa9-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="65fa9-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="65fa9-115">L'appel a réussi globalement, mais il n'y a pas d'options de destinataire pour ce type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="65fa9-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="65fa9-116">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="65fa9-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="65fa9-117">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="65fa9-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="65fa9-118">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="65fa9-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65fa9-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="65fa9-119">Remarks</span></span>

<span data-ttu-id="65fa9-120">La méthode **IMAPISupport:: StatusRecips** est implémentée pour les objets de prise en charge du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="65fa9-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="65fa9-121">Les fournisseurs de transport appellent **StatusRecips** pour demander que MAPI envoie un rapport de remise ou de non-remise à un ensemble d'un ou de plusieurs destinataires d'un message.</span><span class="sxs-lookup"><span data-stu-id="65fa9-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="65fa9-122">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="65fa9-122">Notes to callers</span></span>

<span data-ttu-id="65fa9-123">Vous pouvez appeler **StatusRecips** plusieurs fois pendant le traitement d'un message.</span><span class="sxs-lookup"><span data-stu-id="65fa9-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="65fa9-124">Toutefois, si vous appelez **StatusRecips** pour un message ouvert, vous pouvez collecter toutes les informations de remise et de non-remise pour les destinataires du message et appeler **StatusRecips** pour cette liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="65fa9-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="65fa9-125">Un seul point de collection est important, car plusieurs appels **StatusRecips** pour un destinataire peuvent entraîner l'envoi de plusieurs rapports identiques.</span><span class="sxs-lookup"><span data-stu-id="65fa9-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="65fa9-126">Stockez les propriétés liées à la remise ou non à la remise des messages dans la structure **ADRLIST** indiquée par le paramètre _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="65fa9-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="65fa9-127">Pour obtenir la liste complète des propriétés requises et facultatives pour les rapports de remise et les rapports de non-remise, voir [Required Report message](required-report-message-properties.md) Properties et [Optional Report Message Properties](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="65fa9-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="65fa9-128">AlLouez de la mémoire pour la structure **ADRLIST** dans _lpRecipList_ à l'aide des fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="65fa9-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="65fa9-129">MAPI libère la mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **StatusRecips** réussit.</span><span class="sxs-lookup"><span data-stu-id="65fa9-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="65fa9-130">Pour obtenir une vue d'ensemble des rapports de remise et de non-remise, consultez la rubrique [MAPI Report messages](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="65fa9-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65fa9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65fa9-131">See also</span></span>



[<span data-ttu-id="65fa9-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="65fa9-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="65fa9-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="65fa9-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="65fa9-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="65fa9-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="65fa9-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="65fa9-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="65fa9-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="65fa9-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="65fa9-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="65fa9-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="65fa9-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="65fa9-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="65fa9-139">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65fa9-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

