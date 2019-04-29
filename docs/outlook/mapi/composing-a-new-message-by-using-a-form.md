---
title: Composition d'un nouveau message à l'aide d'un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412799"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="7c95e-103">Composition d'un nouveau message à l'aide d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="7c95e-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="7c95e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c95e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c95e-105">Pour utiliser un formulaire afin de composer un nouveau message, commencez par créer un objet message personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7c95e-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="7c95e-106">**Pour composer un nouveau message à l'aide d'un formulaire**</span><span class="sxs-lookup"><span data-stu-id="7c95e-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="7c95e-107">Appelez la méthode [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) du gestionnaire de formulaire pour extraire un pointeur vers un objet d'informations de formulaire, un objet qui implémente l'interface [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="7c95e-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="7c95e-108">TransMettez le pointeur à l'objet d'informations de formulaire dans un appel à [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="7c95e-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="7c95e-109">**CreateForm** charge le serveur de formulaires approprié.</span><span class="sxs-lookup"><span data-stu-id="7c95e-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="7c95e-110">En outre, transmettez un identificateur d'interface à **CreateForm** pour spécifier l'interface à utiliser pour accéder au nouveau message.</span><span class="sxs-lookup"><span data-stu-id="7c95e-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="7c95e-111">En règle générale, vous demandez [IPersistMessage: IUnknown](ipersistmessageiunknown.md) en passant IID_IPersistMessage à **CreateForm**.</span><span class="sxs-lookup"><span data-stu-id="7c95e-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="7c95e-112">Enregistrez le nouveau message en appelant sa méthode [IPersistMessage:: Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="7c95e-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="7c95e-113">Le serveur de formulaire doit définir des valeurs pour les propriétés requises du message lors de la création du message.</span><span class="sxs-lookup"><span data-stu-id="7c95e-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="7c95e-114">Chargez le message à l'aide de l'une des deux stratégies suivantes: [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) ou [IMAPISession::P Repareform](imapisession-prepareform.md) suivi par [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="7c95e-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="7c95e-115">Pour plus d'informations sur ces stratégies, consultez la rubrique [chargement d'un message dans un formulaire](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="7c95e-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="7c95e-116">Il existe des possibilités de gains de performances lors du chargement d'un nouveau message personnalisé dans un serveur de formulaire, car vous aurez déjà eu la possibilité d'obtenir des informations sur le message, telles que sa classe de message, pendant le traitement requis pour le \*\* Appels ResolveMessageClass\*\* et **CreateForm** .</span><span class="sxs-lookup"><span data-stu-id="7c95e-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="7c95e-117">Pour cette raison, vous serez en mesure de simplifier le traitement requis avant d'appeler **LoadForm** sur ce qui est décrit dans la rubrique [chargement d'un message dans un formulaire](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="7c95e-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

