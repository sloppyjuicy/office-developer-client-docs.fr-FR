---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423950"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="87063-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="87063-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="87063-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87063-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87063-105">Traite un message envoy�.</span><span class="sxs-lookup"><span data-stu-id="87063-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="87063-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87063-106">Parameters</span></span>

 <span data-ttu-id="87063-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87063-107">_ulFlags_</span></span>
  
> <span data-ttu-id="87063-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="87063-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="87063-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="87063-109">_lpMessage_</span></span>
  
> <span data-ttu-id="87063-110">[in] Pointeur vers le message ouvert pour lequel un message doit �tre g�n�r� dans le dossier d�sign� pour contenir les �l�ments envoy�s.</span><span class="sxs-lookup"><span data-stu-id="87063-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87063-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="87063-111">Return value</span></span>

<span data-ttu-id="87063-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="87063-112">S_OK</span></span> 
  
> <span data-ttu-id="87063-113">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="87063-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87063-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="87063-114">Remarks</span></span>

<span data-ttu-id="87063-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="87063-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="87063-118">**DoSentMail** effectue les t�ches suivantes :</span><span class="sxs-lookup"><span data-stu-id="87063-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="87063-119">Vérifie le message pour la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) afin de déterminer si le message doit être supprimé après l'envoi.</span><span class="sxs-lookup"><span data-stu-id="87063-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="87063-120">D�termine l'emplacement du dossier �l�ments envoy�s.</span><span class="sxs-lookup"><span data-stu-id="87063-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="87063-121">Lance le raccordement de message pour n'importe quel hooks d�finies sur le dossier �l�ments envoy�s de traitement.</span><span class="sxs-lookup"><span data-stu-id="87063-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="87063-122">D�place le message vers le dossier �l�ments envoy�s, �l�ments supprim�s, dossier, ou vers un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="87063-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="87063-123">Publie le message.</span><span class="sxs-lookup"><span data-stu-id="87063-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87063-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87063-124">See also</span></span>



[<span data-ttu-id="87063-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="87063-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="87063-126">Propri�t� canonique PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="87063-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="87063-127">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87063-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

