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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326305"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="60463-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="60463-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="60463-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60463-105">Génère un rapport de lecture ou de non-lecture pour un message.</span><span class="sxs-lookup"><span data-stu-id="60463-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="60463-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60463-106">Parameters</span></span>

 <span data-ttu-id="60463-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60463-107">_ulFlags_</span></span>
  
> <span data-ttu-id="60463-108">dans Masque de des indicateurs qui contrôle la manière dont le rapport de lecture ou de non-lecture est généré.</span><span class="sxs-lookup"><span data-stu-id="60463-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="60463-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="60463-109">The following flag can be set:</span></span>
    
<span data-ttu-id="60463-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="60463-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="60463-111">Un rapport non lu est généré.</span><span class="sxs-lookup"><span data-stu-id="60463-111">A nonread report is generated.</span></span> <span data-ttu-id="60463-112">Si MAPI_NON_READ n'est pas défini, un rapport de lecture est généré.</span><span class="sxs-lookup"><span data-stu-id="60463-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="60463-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="60463-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="60463-114">dans Pointeur vers le message à propos duquel le rapport doit être généré.</span><span class="sxs-lookup"><span data-stu-id="60463-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="60463-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="60463-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="60463-116">[in, out] Lors de l'entrée, _lppEmptyMessage_ pointe vers un pointeur vers un message vide.</span><span class="sxs-lookup"><span data-stu-id="60463-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="60463-117">En sortie, _lppEmptyMessage_ pointe vers un pointeur vers le message de rapport.</span><span class="sxs-lookup"><span data-stu-id="60463-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="60463-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="60463-118">Return value</span></span>

<span data-ttu-id="60463-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="60463-119">S_OK</span></span> 
  
> <span data-ttu-id="60463-120">Le rapport a été généré avec succès.</span><span class="sxs-lookup"><span data-stu-id="60463-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60463-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="60463-121">Remarks</span></span>

<span data-ttu-id="60463-122">La méthode **IMAPISupport:: ReadReceipt** est implémentée uniquement pour les objets de prise en charge du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="60463-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="60463-123">Les fournisseurs de banques de messages appellent **ReadReceipt** pour indiquer à MAPI de générer un rapport de lecture ou de non-lecture pour le message pointé par le paramètre _lpReadMessage_ .</span><span class="sxs-lookup"><span data-stu-id="60463-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="60463-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="60463-124">Notes to callers</span></span>

<span data-ttu-id="60463-125">Appelez **ReadReceipt** lorsque la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie et que l'une des conditions suivantes est vraie:</span><span class="sxs-lookup"><span data-stu-id="60463-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="60463-126">Le message a été lu.</span><span class="sxs-lookup"><span data-stu-id="60463-126">The message has been read.</span></span>
    
- <span data-ttu-id="60463-127">Le message a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="60463-127">The message has been moved.</span></span>
    
- <span data-ttu-id="60463-128">Le message a été copié.</span><span class="sxs-lookup"><span data-stu-id="60463-128">The message has been copied.</span></span>
    
- <span data-ttu-id="60463-129">La méthode [IMessage:: SetReadFlag](imessage-setreadflag.md) du message a été appelée.</span><span class="sxs-lookup"><span data-stu-id="60463-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="60463-130">N'appelez pas **ReadReceipt** lorsqu'un message est supprimé.</span><span class="sxs-lookup"><span data-stu-id="60463-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="60463-131">Un rapport de lecture ou de non-lecture ne doit être envoyé qu'une seule fois pour un message.</span><span class="sxs-lookup"><span data-stu-id="60463-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="60463-132">Assurer le suivi de l'état de lecture d'un message et ne pas envoyer plusieurs rapports pour un seul message.</span><span class="sxs-lookup"><span data-stu-id="60463-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="60463-133">Si le paramètre _lppEmptyMessage_ pointe vers un message de rapport valide lorsque MAPI revient de **ReadReceipt**, appelez la méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) pour envoyer le message, puis libérez le pointeur en appelant sa propriété \*\*IUnknown: s: Release. \*\*méthode.</span><span class="sxs-lookup"><span data-stu-id="60463-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="60463-134">Si **ReadReceipt** échoue, le message doit être libéré sans être soumis.</span><span class="sxs-lookup"><span data-stu-id="60463-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="60463-135">Si vous stockez l'état de lecture du message, vous pouvez essayer de générer le rapport de lecture ou de non-lecture ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="60463-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="60463-136">Vous pouvez masquer ou afficher les rapports lus et non lus générés par les banques dans vos dossiers.</span><span class="sxs-lookup"><span data-stu-id="60463-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="60463-137">Le stockage des rapports lus et non lus dans des dossiers cachés vous permet d'implémenter une sécurité plus étroite.</span><span class="sxs-lookup"><span data-stu-id="60463-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60463-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60463-138">See also</span></span>



[<span data-ttu-id="60463-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="60463-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="60463-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="60463-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="60463-141">Propriété canonique PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="60463-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="60463-142">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60463-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

