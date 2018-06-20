---
title: Composer un nouveau Message à l’aide d’un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f4b9cb00512838e6b54c0cc910b8f7279120db3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783048"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="b24c8-103">Composer un nouveau Message à l’aide d’un formulaire</span><span class="sxs-lookup"><span data-stu-id="b24c8-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="b24c8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b24c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b24c8-105">Pour utiliser un formulaire pour créer un nouveau message, d’abord créer un nouvel objet de message personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b24c8-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="b24c8-106">**Pour composer un nouveau message à l’aide d’un formulaire**</span><span class="sxs-lookup"><span data-stu-id="b24c8-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="b24c8-107">Appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) méthode du gestionnaire formulaire pour récupérer un pointeur vers un objet d’informations de formulaire, un objet qui implémente le [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="b24c8-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="b24c8-108">Passez le pointeur à l’objet d’informations de formulaire dans un appel à [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="b24c8-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="b24c8-109">**CreateForm** charge le serveur de la forme appropriée.</span><span class="sxs-lookup"><span data-stu-id="b24c8-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="b24c8-110">En outre, passez un identificateur d’interface à **CreateForm** pour spécifier l’interface à utiliser pour accéder au nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b24c8-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="b24c8-111">En règle générale, vous demander [IPersistMessage : IUnknown](ipersistmessageiunknown.md) en transmettant IID_IPersistMessage à **CreateForm**.</span><span class="sxs-lookup"><span data-stu-id="b24c8-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="b24c8-112">Enregistrez le nouveau message en appelant la méthode [IPersistMessage::Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="b24c8-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="b24c8-113">Le serveur de formulaire doit définir les valeurs des propriétés requises du message lorsqu’il crée le message.</span><span class="sxs-lookup"><span data-stu-id="b24c8-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="b24c8-114">Charger le message à l’aide d’une des deux stratégies : [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) ou [IMAPISession::PrepareForm](imapisession-prepareform.md) suivi [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="b24c8-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="b24c8-115">Pour plus d’informations sur ces stratégies, consultez [chargement d’un Message dans un formulaire](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="b24c8-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="b24c8-116">Il existe des opportunités pour les gains de performances lors du chargement d’un nouveau message personnalisé à un serveur de formulaire, car vous serez ont déjà eu permet d’obtenir des informations sur le message, telles que sa classe de message — pendant le traitement requis pour la ** ResolveMessageClass** et appels **CreateForm** .</span><span class="sxs-lookup"><span data-stu-id="b24c8-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="b24c8-117">Pour cette raison, vous serez en mesure de simplifier le traitement requis avant d’appeler **LoadForm** sur qui décrit dans la rubrique [chargement d’un Message dans un formulaire](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="b24c8-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

