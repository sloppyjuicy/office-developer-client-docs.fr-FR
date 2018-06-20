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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e237e73f59fa691821dcb55b59f5d17518451797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784346"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="9ace3-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="9ace3-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="9ace3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ace3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ace3-105">Initialise un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="9ace3-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="9ace3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ace3-106">Parameters</span></span>

 <span data-ttu-id="9ace3-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="9ace3-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="9ace3-108">[in] Pointeur vers le site de message qui sera utilisée pour travailler avec le message dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="9ace3-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="9ace3-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="9ace3-109">_pMessage_</span></span>
  
> <span data-ttu-id="9ace3-110">[in] Pointeur vers le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="9ace3-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9ace3-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9ace3-111">Return value</span></span>

<span data-ttu-id="9ace3-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ace3-112">S_OK</span></span> 
  
> <span data-ttu-id="9ace3-113">Le nouveau message a été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="9ace3-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ace3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ace3-114">Remarks</span></span>

<span data-ttu-id="9ace3-115">Visionneuses de formulaire appeler la méthode **IPersistMessage::InitNew** lorsque l’utilisateur écrit un nouveau message qui appartient à une classe de message qui gère le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9ace3-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="9ace3-116">Si l’objet form possède un pointeur d’interface utilisateur valide, l’interface utilisateur pour l’objet du message doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="9ace3-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="9ace3-117">**InitNew** ne doit pas être appelée lorsque le formulaire est dans un état à l’exception de l’état [Uninitialized](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="9ace3-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="9ace3-118">Si le formulaire est dans un des autres États lorsque **InitNew** est appelée, retourner E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="9ace3-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9ace3-119">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="9ace3-119">Notes to implementers</span></span>

<span data-ttu-id="9ace3-120">En règle générale, les messages qui contiennent des propriétés non enregistrées sont marquées comme modifiées afin que le client peut afficher une boîte de dialogue qui demande à l’utilisateur si ces propriétés doivent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="9ace3-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="9ace3-121">Si l’utilisateur indique qu’un message doit être enregistré, enregistrer les données, marquer le message en tant que nouvelle et quitter normalement.</span><span class="sxs-lookup"><span data-stu-id="9ace3-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="9ace3-122">Toutefois, si le traitement de vos messages initialisés récemment inclut la définition d’une ou plusieurs des propriétés calculées et il est important pour les propriétés à être enregistrée, ne marquez pas les messages modifié.</span><span class="sxs-lookup"><span data-stu-id="9ace3-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="9ace3-123">Calculée propriétés doivent être invisibles pour les utilisateurs, aucune boîte de dialogue ne doit affiché.</span><span class="sxs-lookup"><span data-stu-id="9ace3-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="9ace3-124">Si votre formulaire comporte une référence à un site de message actif différent de celui qui est passée dans **InitNew**, version du site d’origine, car il sera ne plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="9ace3-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="9ace3-125">Stocker des pointeurs vers le site de message et le message à partir des paramètres _pMessageSite_ et _pMessage_ et appelez des deux objets [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) pour incrémenter son décompte de références.</span><span class="sxs-lookup"><span data-stu-id="9ace3-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="9ace3-126">Définir les propriétés de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour le nouveau message et le **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) par un nom approprié pour votre classe de message.</span><span class="sxs-lookup"><span data-stu-id="9ace3-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="9ace3-127">De nombreuses classes de message, par exemple, définissent **PR_MESSAGE_FLAGS** à MSGFLAG_UNSENT pour les nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="9ace3-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="9ace3-128">Avant de retourner, transition du formulaire à l’état [Normal](normal-state.md) si aucune erreur ne se sont produites.</span><span class="sxs-lookup"><span data-stu-id="9ace3-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="9ace3-129">Envoyer une notification de nouveau message à tous les utilisateurs inscrits en appelant les méthodes [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) et qu’elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="9ace3-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ace3-130">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="9ace3-130">Notes to callers</span></span>

<span data-ttu-id="9ace3-131">Après avoir apporté **InitNew**un appel réussi, vous pouvez supposer que les propriétés requises suivantes et aucune autre, ont été définies pour le formulaire :</span><span class="sxs-lookup"><span data-stu-id="9ace3-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="9ace3-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ace3-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="9ace3-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ace3-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="9ace3-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ace3-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="9ace3-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ace3-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="9ace3-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ace3-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="9ace3-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ace3-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="9ace3-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ace3-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="9ace3-139">Pour plus d’informations sur les États de formulaires, voir [États du formulaire](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="9ace3-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="9ace3-140">Pour plus d’informations sur l’initialisation des objets de stockage, voir la méthode [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9ace3-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ace3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ace3-141">See also</span></span>



[<span data-ttu-id="9ace3-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ace3-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

