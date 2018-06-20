---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784047"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="66eef-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="66eef-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="66eef-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66eef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66eef-105">Il prépare un message pour son envoi au spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="66eef-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="66eef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66eef-106">Parameters</span></span>

 <span data-ttu-id="66eef-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="66eef-107">_lpMessage_</span></span>
  
> <span data-ttu-id="66eef-108">[in] Pointeur vers le message préparer.</span><span class="sxs-lookup"><span data-stu-id="66eef-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="66eef-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="66eef-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="66eef-110">[entrée, sortie] À l’entrée, le paramètre _lpulFlags_ est réservé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="66eef-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="66eef-111">Dans la sortie, _lpulFlags_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="66eef-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="66eef-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="66eef-112">Return value</span></span>

<span data-ttu-id="66eef-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="66eef-113">S_OK</span></span> 
  
> <span data-ttu-id="66eef-114">Le message a été correctement préparé.</span><span class="sxs-lookup"><span data-stu-id="66eef-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66eef-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="66eef-115">Remarks</span></span>

<span data-ttu-id="66eef-116">La méthode **IMAPISupport::PrepareSubmit** est implémentée pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="66eef-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="66eef-117">Fournisseurs de banque de messages appeler **PrepareSubmit** dans leur implémentation de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour préparer un message pour son envoi au spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="66eef-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="66eef-118">**PrepareSubmit** est utilisé pour gérer les messages dont l’indicateur MSGFLAG_RESEND dans leur propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="66eef-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="66eef-119">MSGFLAG_RESEND est définie pour les messages qui incluent une demande à être renvoyées en cas d’échec d’une transmission initiale.</span><span class="sxs-lookup"><span data-stu-id="66eef-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="66eef-120">**PrepareSubmit** détermine parmi les destinataires dans la liste des destinataires a reçu le message et qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="66eef-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="66eef-121">Pour accéder à la liste des destinataires, **PrepareSubmit** appelle la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message.</span><span class="sxs-lookup"><span data-stu-id="66eef-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="66eef-122">Pour récupérer les données du destinataire, **PrepareSubmit** appelle la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de destinataire de la table.</span><span class="sxs-lookup"><span data-stu-id="66eef-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="66eef-123">Pour chaque ligne dans le tableau, **PrepareSubmit** vérifie la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) et peut prendre l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="66eef-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="66eef-124">Si l’indicateur MAPI_SUBMITTED est défini, **PrepareSubmit** efface l’indicateur et définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="66eef-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="66eef-125">Si l’indicateur MAPI_SUBMITTED n’est pas définie, **PrepareSubmit** devient **PR_RECIPIENT_TYPE** MAPI_P1 et définit **PR_RESPONSIBILITY** sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="66eef-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="66eef-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="66eef-126">Notes to callers</span></span>

<span data-ttu-id="66eef-127">Avant d’appeler **PrepareSubmit**, n’oubliez pas que vous avez appelé la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) et définissez l’indicateur NOTIFY_READYTOSEND dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="66eef-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="66eef-128">L’appel **SpoolerNotify** doit être effectuée qu’une seule fois par session avant l’appel à **PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="66eef-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="66eef-129">**SpoolerNotify** synchronise le spouleur MAPI et garantit que tous les fournisseurs de transport nécessaires sont connectés et leurs types d’adresses sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="66eef-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66eef-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66eef-130">See also</span></span>



[<span data-ttu-id="66eef-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="66eef-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="66eef-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="66eef-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="66eef-133">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66eef-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

