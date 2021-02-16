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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425735"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="3d23b-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="3d23b-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="3d23b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d23b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d23b-105">Prépare un message à envoyer aupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d23b-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3d23b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d23b-106">Parameters</span></span>

 <span data-ttu-id="3d23b-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3d23b-107">_lpMessage_</span></span>
  
> <span data-ttu-id="3d23b-108">[in] Pointeur vers le message à préparer.</span><span class="sxs-lookup"><span data-stu-id="3d23b-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="3d23b-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d23b-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="3d23b-110">[in, out] En entrée, le  _paramètre lpulFlags_ est réservé et doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3d23b-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="3d23b-111">En sortie,  _lpulFlags doit_ avoir la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="3d23b-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3d23b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3d23b-112">Return value</span></span>

<span data-ttu-id="3d23b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d23b-113">S_OK</span></span> 
  
> <span data-ttu-id="3d23b-114">Le message a été correctement préparé.</span><span class="sxs-lookup"><span data-stu-id="3d23b-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d23b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d23b-115">Remarks</span></span>

<span data-ttu-id="3d23b-116">La **méthode IMAPISupport::P repareSubmit** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="3d23b-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="3d23b-117">Les fournisseurs de magasins de messages appellent **PrepareSubmit** dans leur implémentation de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour préparer un message à envoyer aupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d23b-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="3d23b-118">**PrepareSubmit** est utilisé pour gérer les messages dont l’indicateur MSGFLAG_RESEND est PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3d23b-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="3d23b-119">MSGFLAG_RESEND est définie pour les messages qui incluent une demande à envoyer en cas d’échec d’une transmission initiale.</span><span class="sxs-lookup"><span data-stu-id="3d23b-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="3d23b-120">**PrepareSubmit** détermine lequel des destinataires de la liste des destinataires a reçu le message avec succès et qui ne l’a pas été.</span><span class="sxs-lookup"><span data-stu-id="3d23b-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="3d23b-121">Pour accéder à la liste des **destinataires, PrepareSubmit** appelle la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message.</span><span class="sxs-lookup"><span data-stu-id="3d23b-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="3d23b-122">Pour récupérer les données du destinataire, **PrepareSubmit** appelle la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de la table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="3d23b-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="3d23b-123">Pour chaque ligne du tableau, **PrepareSubmit** vérifie la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) et prend l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d23b-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="3d23b-124">Si l MAPI_SUBMITTED est définie, **PrepareSubmit** l’effacera et définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="3d23b-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="3d23b-125">Si l’MAPI_SUBMITTED n’est pas définie, **PrepareSubmit** PR_RECIPIENT_TYPE **à** MAPI_P1 et définit PR_RESPONSIBILITY **sur** TRUE.</span><span class="sxs-lookup"><span data-stu-id="3d23b-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="3d23b-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="3d23b-126">Notes to callers</span></span>

<span data-ttu-id="3d23b-127">Avant d’appeler **PrepareSubmit,** assurez-vous d’avoir appelé la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) et définissez l’indicateur NOTIFY_READYTOSEND dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="3d23b-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="3d23b-128">**L’appel SpoolerNotify** doit être effectué une fois par session avant l’appel **à PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="3d23b-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="3d23b-129">**SpoolerNotify** synchronise lepooler MAPI et garantit que tous les fournisseurs de transport nécessaires sont connectés et que leurs types d’adresses sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="3d23b-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d23b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d23b-130">See also</span></span>



[<span data-ttu-id="3d23b-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3d23b-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="3d23b-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="3d23b-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="3d23b-133">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d23b-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

