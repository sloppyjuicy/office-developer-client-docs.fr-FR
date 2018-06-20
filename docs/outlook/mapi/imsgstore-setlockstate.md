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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a4e924489f2ec656f473f28407d528e9c2ddda5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784251"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="efb78-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="efb78-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="efb78-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="efb78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="efb78-105">Verrouiller ou déverrouiller un message.</span><span class="sxs-lookup"><span data-stu-id="efb78-105">Locks or unlocks a message.</span></span> <span data-ttu-id="efb78-106">Cette m�thode est appel�e uniquement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="efb78-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="efb78-107">Param�tres</span><span class="sxs-lookup"><span data-stu-id="efb78-107">Parameters</span></span>

 <span data-ttu-id="efb78-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="efb78-108">_lpMessage_</span></span>
  
> <span data-ttu-id="efb78-109">[in] Pointeur vers le message pour verrouiller ou déverrouiller.</span><span class="sxs-lookup"><span data-stu-id="efb78-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="efb78-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="efb78-110">_ulLockState_</span></span>
  
> <span data-ttu-id="efb78-111">[in] Une valeur qui indique si le message doit être verrouillé ou déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="efb78-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="efb78-112">Valide une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="efb78-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="efb78-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="efb78-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="efb78-114">Le message doit être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="efb78-114">The message should be locked.</span></span> 
    
<span data-ttu-id="efb78-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="efb78-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="efb78-116">Le message doit être déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="efb78-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efb78-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="efb78-117">Return value</span></span>

<span data-ttu-id="efb78-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="efb78-118">S_OK</span></span> 
  
> <span data-ttu-id="efb78-119">L’état de verrouillage du message a été correctement définie.</span><span class="sxs-lookup"><span data-stu-id="efb78-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efb78-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="efb78-120">Remarks</span></span>

<span data-ttu-id="efb78-121">La méthode **IMsgStore::SetLockState** verrouille ou déverrouille un message.</span><span class="sxs-lookup"><span data-stu-id="efb78-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="efb78-122">**SetLockState** peut être appelée uniquement par le spouleur MAPI pendant qu’il envoie le message.</span><span class="sxs-lookup"><span data-stu-id="efb78-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="efb78-123">En règle générale, lorsque le spouleur MAPI appelle **SetLockState** pour verrouiller un message, il est verrouillé uniquement le message le plus ancien (autrement dit, le message suivant en file d’attente pour le spouleur MAPI envoyer).</span><span class="sxs-lookup"><span data-stu-id="efb78-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="efb78-124">Si le message le plus ancien dans la file d’attente est en attente d’un fournisseur de transport temporairement indisponible et le message suivant dans la file d’attente utilise un fournisseur de transport différents, le spouleur MAPI permettre commencer à traiter le message ultérieure.</span><span class="sxs-lookup"><span data-stu-id="efb78-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="efb78-125">Il commence le traitement par le verrouillage de ce message à l’aide de **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="efb78-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="efb78-126">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="efb78-126">Notes to implementers</span></span>

<span data-ttu-id="efb78-127">Une fois que le spouleur MAPI a appelé **SetLockState** avec le paramètre _ulLockState_ défini sur MSG_LOCKED, les appels à la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour annuler la transmission du message doivent échouer.</span><span class="sxs-lookup"><span data-stu-id="efb78-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="efb78-128">Appelez la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message dans votre implémentation **SetLockState** afin que les modifications qui ont été apportées au message avant l’appel **SetLockState** a été reçue.</span><span class="sxs-lookup"><span data-stu-id="efb78-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efb78-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efb78-129">See also</span></span>



[<span data-ttu-id="efb78-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="efb78-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="efb78-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="efb78-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="efb78-132">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="efb78-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

