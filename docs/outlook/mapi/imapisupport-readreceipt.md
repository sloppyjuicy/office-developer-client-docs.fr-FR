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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425322"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="07ab9-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="07ab9-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="07ab9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07ab9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07ab9-105">Génère un rapport en lecture ou non lu pour un message.</span><span class="sxs-lookup"><span data-stu-id="07ab9-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="07ab9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07ab9-106">Parameters</span></span>

 <span data-ttu-id="07ab9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="07ab9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="07ab9-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont le rapport en lecture ou non lu est généré.</span><span class="sxs-lookup"><span data-stu-id="07ab9-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="07ab9-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="07ab9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="07ab9-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="07ab9-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="07ab9-111">Un rapport non lu est généré.</span><span class="sxs-lookup"><span data-stu-id="07ab9-111">A nonread report is generated.</span></span> <span data-ttu-id="07ab9-112">Si MAPI_NON_READ n’est pas définie, un rapport de lecture est généré.</span><span class="sxs-lookup"><span data-stu-id="07ab9-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="07ab9-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="07ab9-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="07ab9-114">[in] Pointeur vers le message à propos duquel le rapport doit être généré.</span><span class="sxs-lookup"><span data-stu-id="07ab9-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="07ab9-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="07ab9-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="07ab9-116">[in, out] Lors de  _l’entrée, lppEmptyMessage_ pointe vers un pointeur vers un message vide.</span><span class="sxs-lookup"><span data-stu-id="07ab9-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="07ab9-117">En sortie,  _lppEmptyMessage_ pointe vers un pointeur vers le message de rapport.</span><span class="sxs-lookup"><span data-stu-id="07ab9-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="07ab9-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07ab9-118">Return value</span></span>

<span data-ttu-id="07ab9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="07ab9-119">S_OK</span></span> 
  
> <span data-ttu-id="07ab9-120">Le rapport a été généré avec succès.</span><span class="sxs-lookup"><span data-stu-id="07ab9-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07ab9-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="07ab9-121">Remarks</span></span>

<span data-ttu-id="07ab9-122">La **méthode IMAPISupport::ReadReceipt** est implémentée uniquement pour les objets de prise en charge du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="07ab9-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="07ab9-123">Les fournisseurs de magasins de messages appellent **ReadReceipt** pour demander à MAPI de générer un rapport lu ou non lu pour le message pointé par le paramètre _lpReadMessage._</span><span class="sxs-lookup"><span data-stu-id="07ab9-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="07ab9-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="07ab9-124">Notes to callers</span></span>

<span data-ttu-id="07ab9-125">Appelez **ReadReceipt** lorsque la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie et que l’une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="07ab9-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="07ab9-126">Le message a été lu.</span><span class="sxs-lookup"><span data-stu-id="07ab9-126">The message has been read.</span></span>
    
- <span data-ttu-id="07ab9-127">Le message a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="07ab9-127">The message has been moved.</span></span>
    
- <span data-ttu-id="07ab9-128">Le message a été copié.</span><span class="sxs-lookup"><span data-stu-id="07ab9-128">The message has been copied.</span></span>
    
- <span data-ttu-id="07ab9-129">La méthode [IMessage::SetReadFlag](imessage-setreadflag.md) du message a été appelée.</span><span class="sxs-lookup"><span data-stu-id="07ab9-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="07ab9-130">N’appelez **pas ReadReceipt** lorsqu’un message est supprimé.</span><span class="sxs-lookup"><span data-stu-id="07ab9-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="07ab9-131">Un rapport lu ou non lu ne doit être envoyé qu’une seule fois pour un message.</span><span class="sxs-lookup"><span data-stu-id="07ab9-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="07ab9-132">Suivez l’état de lecture d’un message et n’envoyez pas plusieurs rapports pour un seul message.</span><span class="sxs-lookup"><span data-stu-id="07ab9-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="07ab9-133">Si le paramètre _lppEmptyMessage_ pointe vers un message de rapport valide lorsque MAPI revient de **ReadReceipt,** appelez la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer le message, puis relâchez le pointeur en appelant sa méthode **IUnknown:s:Release.**</span><span class="sxs-lookup"><span data-stu-id="07ab9-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="07ab9-134">En **cas d’échec de ReadReceipt,** le message doit être libéré sans être envoyé.</span><span class="sxs-lookup"><span data-stu-id="07ab9-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="07ab9-135">Si vous stockez l’état de lecture du message, vous pouvez tenter de générer le rapport lu ou non lu ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="07ab9-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="07ab9-136">Vous pouvez masquer ou afficher des rapports de lecture et non lus générés par les magasins dans vos dossiers.</span><span class="sxs-lookup"><span data-stu-id="07ab9-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="07ab9-137">Le stockage de rapports lus et non lus dans des dossiers masqués vous permet d’implémenter une sécurité plus étroite.</span><span class="sxs-lookup"><span data-stu-id="07ab9-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="07ab9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07ab9-138">See also</span></span>



[<span data-ttu-id="07ab9-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="07ab9-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="07ab9-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="07ab9-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="07ab9-141">Propriété canonique PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="07ab9-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="07ab9-142">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="07ab9-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

