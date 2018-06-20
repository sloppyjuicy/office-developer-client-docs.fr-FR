---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ce4d57ab4837f40ffbc898fde68e44cc802676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783750"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="5beb0-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="5beb0-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="5beb0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5beb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5beb0-105">Indique si le formulaire peut gérer la classe de message du message suivant à afficher.</span><span class="sxs-lookup"><span data-stu-id="5beb0-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="5beb0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5beb0-106">Parameters</span></span>

 <span data-ttu-id="5beb0-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="5beb0-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="5beb0-108">[in] Pointeur vers la classe de message du message suivant.</span><span class="sxs-lookup"><span data-stu-id="5beb0-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="5beb0-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="5beb0-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="5beb0-110">[in] Un masque de bits d’indicateurs défini par le client ou défini par le fournisseur, copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message suivant à afficher, qui fournit des informations d’état concernant la table des matières que le message est inclus dans.</span><span class="sxs-lookup"><span data-stu-id="5beb0-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="5beb0-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="5beb0-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="5beb0-112">[in] Un pointeur vers un masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message suivant à afficher qui indique l’état actuel du message.</span><span class="sxs-lookup"><span data-stu-id="5beb0-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="5beb0-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="5beb0-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="5beb0-114">[out] Pointeur vers un pointeur vers l’implémentation de [IPersistMessage](ipersistmessageiunknown.md) pour l’objet de formulaire utilisé pour le nouveau formulaire, si un nouveau formulaire est requis.</span><span class="sxs-lookup"><span data-stu-id="5beb0-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="5beb0-115">Un pointeur null peut être obtenue si l’objet de formulaire en cours peut être utilisé pour afficher et enregistrer le message suivant.</span><span class="sxs-lookup"><span data-stu-id="5beb0-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5beb0-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="5beb0-116">Return value</span></span>

<span data-ttu-id="5beb0-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="5beb0-117">S_OK</span></span> 
  
> <span data-ttu-id="5beb0-118">La notification a réussi et que le formulaire peut gérer le message suivant.</span><span class="sxs-lookup"><span data-stu-id="5beb0-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="5beb0-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="5beb0-119">S_FALSE</span></span> 
  
> <span data-ttu-id="5beb0-120">Le formulaire ne gère pas la classe de message du message suivant.</span><span class="sxs-lookup"><span data-stu-id="5beb0-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5beb0-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="5beb0-121">Remarks</span></span>

<span data-ttu-id="5beb0-122">Visionneuses de formulaire appeler la méthode **IMAPIFormAdviseSink::OnActivateNext** pour déterminer le formulaire s’il peut afficher le message suivant dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="5beb0-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="5beb0-123">Le message suivant peut être un message de n’importe quelle classe, mais il est généralement de la même classe ou une classe connexe.</span><span class="sxs-lookup"><span data-stu-id="5beb0-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="5beb0-124">Ainsi, le processus de lecture de plusieurs messages de la même classe plus efficace en activant les applications clientes de réutiliser des objets de formulaire chaque fois que possible.</span><span class="sxs-lookup"><span data-stu-id="5beb0-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="5beb0-125">La plupart des objets de formulaire utilise la classe de message indiquée par le paramètre _lpszMessageClass_ pour déterminer si elles peuvent gérer le message suivant.</span><span class="sxs-lookup"><span data-stu-id="5beb0-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="5beb0-126">Généralement un formulaire peut gérer les messages qui appartiennent aux classes dont la classe du formulaire par défaut est une sous-classe, en plus des messages qui appartiennent à la classe par défaut.</span><span class="sxs-lookup"><span data-stu-id="5beb0-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="5beb0-127">Toutefois, un formulaire peut utiliser autres facteurs pour déterminer sans question si un message peut être géré, telles que l’état envoyé ou en attente du message suivant.</span><span class="sxs-lookup"><span data-stu-id="5beb0-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5beb0-128">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="5beb0-128">Notes to implementers</span></span>

<span data-ttu-id="5beb0-129">Renvoie S_OK et NULL dans le paramètre _ppPersistMessage_ si le formulaire peut gérer la classe de message.</span><span class="sxs-lookup"><span data-stu-id="5beb0-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="5beb0-130">Si le formulaire peut créer un formulaire qui peut gérer le message que le formulaire ne peut pas gérer, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5beb0-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="5beb0-131">Appelez la fabrique de classe de votre formulaire pour créer une instance d’un nouvel objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="5beb0-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="5beb0-132">Stocker cette instance dans le contenu du paramètre pointeur _ppPersistMessage_ .</span><span class="sxs-lookup"><span data-stu-id="5beb0-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="5beb0-133">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="5beb0-133">Return S_OK.</span></span>
    
<span data-ttu-id="5beb0-134">La visionneuse de formulaire chargera le message à l’aide de la méthode [IPersistMessage::Load](ipersistmessage-load.md) qui appartient à l’objet désigné par _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="5beb0-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="5beb0-135">Si le formulaire, ni un formulaire que vous pouvez créer peut gérer le message suivant, renvoie S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="5beb0-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="5beb0-136">Toutefois, en règle générale, les formulaires ne doivent pas renvoyer que cette valeur, car il engendre diminue les performances dans la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="5beb0-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5beb0-137">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5beb0-137">MFCMAPI reference</span></span>

<span data-ttu-id="5beb0-138">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5beb0-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5beb0-139">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5beb0-139">**File**</span></span>|<span data-ttu-id="5beb0-140">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5beb0-140">**Function**</span></span>|<span data-ttu-id="5beb0-141">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5beb0-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5beb0-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5beb0-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5beb0-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="5beb0-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="5beb0-144">MFCMAPI utilise la méthode **IMAPIFormAdviseSink::OnActivateNext** pour implémenter la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .</span><span class="sxs-lookup"><span data-stu-id="5beb0-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5beb0-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5beb0-145">See also</span></span>



[<span data-ttu-id="5beb0-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="5beb0-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="5beb0-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5beb0-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="5beb0-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="5beb0-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="5beb0-149">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="5beb0-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="5beb0-150">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="5beb0-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="5beb0-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5beb0-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="5beb0-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5beb0-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

