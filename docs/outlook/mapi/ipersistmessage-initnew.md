---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317149"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="4f0ac-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="4f0ac-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="4f0ac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f0ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f0ac-105">Initialise un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="4f0ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f0ac-106">Parameters</span></span>

 <span data-ttu-id="4f0ac-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="4f0ac-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="4f0ac-108">dans Pointeur vers le site de messagerie que le formulaire utilisera pour fonctionner avec le message dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="4f0ac-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="4f0ac-109">_pMessage_</span></span>
  
> <span data-ttu-id="4f0ac-110">dans Pointeur vers le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f0ac-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f0ac-111">Return value</span></span>

<span data-ttu-id="4f0ac-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f0ac-112">S_OK</span></span> 
  
> <span data-ttu-id="4f0ac-113">Le nouveau message a été initialisé.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f0ac-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4f0ac-114">Remarks</span></span>

<span data-ttu-id="4f0ac-115">Les visionneuses de formulaires appellent la méthode **IPersistMessage:: InitNew** lorsque l'utilisateur écrit un nouveau message qui appartient à une classe de message gérée par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="4f0ac-116">Si l'objet Form est doté d'un pointeur d'interface utilisateur valide, l'interface utilisateur de l'objet message doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="4f0ac-117">**InitNew** ne doit pas être appelé lorsque l'état de votre formulaire est différent de l'état [non initialisé](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="4f0ac-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="4f0ac-118">Si le formulaire est dans l'un des autres États lorsque **InitNew** est appelé, renvoyer E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4f0ac-119">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="4f0ac-119">Notes to implementers</span></span>

<span data-ttu-id="4f0ac-120">En règle générale, les messages dont les propriétés ne sont pas enregistrées sont marqués comme étant modifiés afin que le client puisse afficher une boîte de dialogue qui invite l'utilisateur à indiquer si ces propriétés doivent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="4f0ac-121">Si l'utilisateur indique qu'un message doit être enregistré, enregistrez les données, marquez le message comme nettoyé, puis quittez normalement.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="4f0ac-122">Toutefois, si le traitement de vos messages nouvellement initialisés inclut la définition d'une ou de plusieurs propriétés calculées et qu'il est important que ces propriétés soient enregistrées, ne Marquez pas les messages comme étant modifiés.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="4f0ac-123">Étant donné que les propriétés calculées doivent être invisibles pour les utilisateurs, aucune boîte de dialogue ne doit s'afficher.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="4f0ac-124">Si votre formulaire comporte une référence à un site de messagerie actif autre que celui qui est transmis à **InitNew**, libérez le site d'origine car il ne sera plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="4f0ac-125">Stockez les pointeurs sur le site de messagerie et le message des paramètres _pMessageSite_ et _pMessage_ et appelez les deux méthodes « [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) » pour incrémenter leur nombre de références.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="4f0ac-126">Définissez les propriétés **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) et **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour le nouveau message à une valeur appropriée pour votre classe de message.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="4f0ac-127">De nombreuses classes de message, par exemple, Set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for New messages.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="4f0ac-128">Avant de retourner, faire basculer le formulaire vers l'état [normal](normal-state.md) si aucune erreur n'est survenue.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="4f0ac-129">Envoyez une nouvelle notification par message à toutes les visionneuses inscrites en appelant leurs méthodes [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) et en retournant S_OK.</span><span class="sxs-lookup"><span data-stu-id="4f0ac-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4f0ac-130">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="4f0ac-130">Notes to callers</span></span>

<span data-ttu-id="4f0ac-131">Une fois que vous avez effectué un appel réussi à **InitNew**, vous pouvez supposer que les propriétés requises suivantes, et aucune autre, ont été définies pour le formulaire:</span><span class="sxs-lookup"><span data-stu-id="4f0ac-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="4f0ac-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f0ac-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="4f0ac-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f0ac-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="4f0ac-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f0ac-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="4f0ac-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f0ac-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="4f0ac-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f0ac-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="4f0ac-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f0ac-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="4f0ac-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f0ac-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="4f0ac-139">Pour plus d'informations sur les États de formulaires, voir [États de formulaire](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="4f0ac-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="4f0ac-140">Pour plus d'informations sur la façon dont les objets de stockage sont initialisés, consultez la méthode [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f0ac-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f0ac-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f0ac-141">See also</span></span>



[<span data-ttu-id="4f0ac-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f0ac-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

