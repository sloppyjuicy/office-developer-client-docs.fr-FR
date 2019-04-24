---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348747"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="4626f-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="4626f-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="4626f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4626f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4626f-105">Verrouille ou déverrouille un message.</span><span class="sxs-lookup"><span data-stu-id="4626f-105">Locks or unlocks a message.</span></span> <span data-ttu-id="4626f-106">Cette m�thode est appel�e uniquement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="4626f-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="4626f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4626f-107">Parameters</span></span>

 <span data-ttu-id="4626f-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="4626f-108">_lpMessage_</span></span>
  
> <span data-ttu-id="4626f-109">dans Pointeur vers le message à verrouiller ou déverrouiller.</span><span class="sxs-lookup"><span data-stu-id="4626f-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="4626f-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="4626f-110">_ulLockState_</span></span>
  
> <span data-ttu-id="4626f-111">dans Valeur qui indique si le message doit être verrouillé ou déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="4626f-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="4626f-112">L'une des valeurs suivantes est valide:</span><span class="sxs-lookup"><span data-stu-id="4626f-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="4626f-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="4626f-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="4626f-114">Le message doit être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="4626f-114">The message should be locked.</span></span> 
    
<span data-ttu-id="4626f-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="4626f-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="4626f-116">Le message doit être déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="4626f-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4626f-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4626f-117">Return value</span></span>

<span data-ttu-id="4626f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4626f-118">S_OK</span></span> 
  
> <span data-ttu-id="4626f-119">L'état de verrouillage du message a été correctement défini.</span><span class="sxs-lookup"><span data-stu-id="4626f-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4626f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4626f-120">Remarks</span></span>

<span data-ttu-id="4626f-121">La méthode **IMsgStore:: SetLockState** verrouille ou déverrouille un message.</span><span class="sxs-lookup"><span data-stu-id="4626f-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="4626f-122">**SetLockState** ne peut être appelée que par le spouleur MAPI pendant l'envoi du message.</span><span class="sxs-lookup"><span data-stu-id="4626f-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="4626f-123">En règle générale, lorsque le spouleur MAPI appelle **SetLockState** pour verrouiller un message, il verrouille uniquement le plus ancien message (c'est-à-dire, le message suivant en file d'attente pour le spouleur MAPI à envoyer).</span><span class="sxs-lookup"><span data-stu-id="4626f-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="4626f-124">Si le message le plus ancien de la file d'attente attend un fournisseur de transport temporairement indisponible et que le message suivant de la file d'attente utilise un autre fournisseur de transport, le spouleur MAPI peut commencer à traiter le message ultérieur.</span><span class="sxs-lookup"><span data-stu-id="4626f-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="4626f-125">Elle commence à traiter en verrouillant ce message à l'aide de **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="4626f-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4626f-126">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="4626f-126">Notes to implementers</span></span>

<span data-ttu-id="4626f-127">Une fois que le spouleur MAPI a appelé **SetLockState** avec le paramètre _ULLOCKSTATE_ défini sur MSG_LOCKED, les appels à la méthode [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) pour annuler la transmission du message doivent échouer.</span><span class="sxs-lookup"><span data-stu-id="4626f-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="4626f-128">Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message dans votre implémentation **SetLockState** afin que les modifications qui ont été apportées au message avant la réception de l'appel de **SetLockState** soient enregistrées.</span><span class="sxs-lookup"><span data-stu-id="4626f-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4626f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4626f-129">See also</span></span>



[<span data-ttu-id="4626f-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="4626f-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="4626f-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="4626f-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="4626f-132">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4626f-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

