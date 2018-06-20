---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784046"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="c977e-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="c977e-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="c977e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c977e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c977e-105">Génère un rapport nonread pour un message ou en lecture.</span><span class="sxs-lookup"><span data-stu-id="c977e-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="c977e-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="c977e-106">Parameters</span></span>

 <span data-ttu-id="c977e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c977e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c977e-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont la lecture ou l’état nonread est généré.</span><span class="sxs-lookup"><span data-stu-id="c977e-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="c977e-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="c977e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c977e-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="c977e-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="c977e-111">Un rapport nonread est généré.</span><span class="sxs-lookup"><span data-stu-id="c977e-111">A nonread report is generated.</span></span> <span data-ttu-id="c977e-112">Si MAPI_NON_READ n’est pas définie, un rapport de lecture est généré.</span><span class="sxs-lookup"><span data-stu-id="c977e-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="c977e-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="c977e-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="c977e-114">[in] Pointeur vers le message sur lequel le rapport doit être généré.</span><span class="sxs-lookup"><span data-stu-id="c977e-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="c977e-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="c977e-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="c977e-116">[entrée, sortie] À l’entrée _lppEmptyMessage_ pointe vers un pointeur vers un message vide.</span><span class="sxs-lookup"><span data-stu-id="c977e-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="c977e-117">Dans la sortie, _lppEmptyMessage_ pointe vers un pointeur vers le message d’état.</span><span class="sxs-lookup"><span data-stu-id="c977e-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c977e-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c977e-118">Return value</span></span>

<span data-ttu-id="c977e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c977e-119">S_OK</span></span> 
  
> <span data-ttu-id="c977e-120">Le rapport a été généré.</span><span class="sxs-lookup"><span data-stu-id="c977e-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c977e-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="c977e-121">Remarks</span></span>

<span data-ttu-id="c977e-122">La méthode **IMAPISupport::ReadReceipt** est implémentée uniquement pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="c977e-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="c977e-123">Fournisseurs de magasins message appellent **ReadReceipt** pour indiquer à MAPI pour générer un rapport nonread pour le message vers laquelle pointé le paramètre _lpReadMessage_ ou en lecture.</span><span class="sxs-lookup"><span data-stu-id="c977e-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c977e-124">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c977e-124">Notes to callers</span></span>

<span data-ttu-id="c977e-125">Appel **ReadReceipt** lorsque la valeur de la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="c977e-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="c977e-126">Le message a été lu.</span><span class="sxs-lookup"><span data-stu-id="c977e-126">The message has been read.</span></span>
    
- <span data-ttu-id="c977e-127">Le message a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c977e-127">The message has been moved.</span></span>
    
- <span data-ttu-id="c977e-128">Le message a été copié.</span><span class="sxs-lookup"><span data-stu-id="c977e-128">The message has been copied.</span></span>
    
- <span data-ttu-id="c977e-129">Méthode de [IMessage::SetReadFlag](imessage-setreadflag.md) du message a été appelée.</span><span class="sxs-lookup"><span data-stu-id="c977e-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="c977e-130">N’appelez pas **ReadReceipt** lorsqu’un message est supprimé.</span><span class="sxs-lookup"><span data-stu-id="c977e-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="c977e-131">Un rapport nonread ou en lecture doit être envoyé qu’une seule fois pour un message.</span><span class="sxs-lookup"><span data-stu-id="c977e-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="c977e-132">Garder une trace des état de lecture d’un message et ne pas envoyer de rapports multiples pour un seul message.</span><span class="sxs-lookup"><span data-stu-id="c977e-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="c977e-133">Si le paramètre _lppEmptyMessage_ pointe vers un message de rapport valide MAPI retourne à partir de **ReadReceipt**, appelez la méthode de [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer le message et puis relâchez le pointeur en appelant son **IUnknown:s:Release **méthode.</span><span class="sxs-lookup"><span data-stu-id="c977e-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="c977e-134">Si **ReadReceipt** échoue, le message doit être libéré sans soumis.</span><span class="sxs-lookup"><span data-stu-id="c977e-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="c977e-135">Si vous stockez état de lecture du message, vous pouvez tenter de générer le lire ou nonread à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c977e-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="c977e-136">Vous pouvez masquer ou afficher des rapports de lecture et nonread générés par magasins dans vos dossiers.</span><span class="sxs-lookup"><span data-stu-id="c977e-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="c977e-137">Stockage des rapports de lecture et nonread dans des dossiers cachés vous permet d’implémenter une sécurité accrue.</span><span class="sxs-lookup"><span data-stu-id="c977e-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c977e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c977e-138">See also</span></span>



[<span data-ttu-id="c977e-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="c977e-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="c977e-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c977e-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c977e-141">Propriété canonique PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c977e-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="c977e-142">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c977e-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

