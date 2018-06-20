---
title: L’implémentation d’une visionneuse de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784151"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="e3997-103">L’implémentation d’une visionneuse de formulaire</span><span class="sxs-lookup"><span data-stu-id="e3997-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="e3997-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3997-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3997-105">Une visionneuse de formulaire comprend trois objets : un site de message, un affichage de notification récepteur et un contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="e3997-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="e3997-106">Chacun de ces objets vous permet d’interagir avec un serveur de la forme et ses formes.</span><span class="sxs-lookup"><span data-stu-id="e3997-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="e3997-107">Un site de message est un objet qui implémente le [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface et vous aide à des serveurs de formulaire avec des tâches telles que le déplacement, l’enregistrement, la suppression des messages, création de nouveaux messages ou lancement de nouveaux serveurs de formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3997-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="e3997-108">Sites de message sont utilisés par les formulaires pour obtenir des informations sur l’état de votre client en ce qui concerne les différents fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="e3997-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="e3997-109">Par exemple, un formulaire peut utiliser votre site de message pour obtenir un pointeur vers la banque de messages en cours, un message ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="e3997-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="e3997-110">Il existe deux types de méthodes de l’interface **IMAPIMessageSite** :</span><span class="sxs-lookup"><span data-stu-id="e3997-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="e3997-111">Méthodes qui fournissent des informations aux objets du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3997-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="e3997-112">Méthodes qui manipulent des messages.</span><span class="sxs-lookup"><span data-stu-id="e3997-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="e3997-113">Les méthodes qui fournissent des informations aux objets de formulaire sont faciles à implémenter.</span><span class="sxs-lookup"><span data-stu-id="e3997-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="e3997-114">Dans tous les cas, à l’exception de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), vous devez avoir déjà disponibles les informations requises par chaque méthode.</span><span class="sxs-lookup"><span data-stu-id="e3997-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="e3997-115">Les méthodes qui manipulent des messages doivent agir comme s’ils avaient été déclenchées par le biais de votre interface utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="e3997-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="e3997-116">Par exemple, si un objet form appelle votre méthode [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) , se comportent comme si l’utilisateur a choisi de créer un nouveau message personnalisé avec votre interface utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="e3997-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="e3997-117">**Composition**, **Ouvrir**, **réponse**, **répondre à tous les destinataires**et **Transférer**se trouvent les commandes qui génèrent généralement ce comportement.</span><span class="sxs-lookup"><span data-stu-id="e3997-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="e3997-118">Un contexte de vue est un objet qui implémente le [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface et fournit des serveurs de formulaire avec un contexte pour le message en cours, ce qui permet de serveurs passer rapidement dans le message suivant ou précédent dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="e3997-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="e3997-119">Un formulaire utilise un contexte de vue pour le partage des informations.</span><span class="sxs-lookup"><span data-stu-id="e3997-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="e3997-120">Avec un objet de contexte de vue, un formulaire peut :</span><span class="sxs-lookup"><span data-stu-id="e3997-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="e3997-121">Inscrire avec votre client pour les notifications.</span><span class="sxs-lookup"><span data-stu-id="e3997-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="e3997-122">Activer le message suivant ou précédent dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="e3997-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="e3997-123">Obtenir des informations sur l’impression.</span><span class="sxs-lookup"><span data-stu-id="e3997-123">Get printing information.</span></span>
    
- <span data-ttu-id="e3997-124">Obtenir l’état de votre client.</span><span class="sxs-lookup"><span data-stu-id="e3997-124">Get your client's status.</span></span>
    
- <span data-ttu-id="e3997-125">Obtenir un flux qui peut être utilisé pour enregistrer la version texte d’un message.</span><span class="sxs-lookup"><span data-stu-id="e3997-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="e3997-126">Similaire aux méthodes dans le [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, les méthodes de **IMAPIViewContext** mettre en corrélation avec les fonctionnalités de client qui sont associées au contexte de l’affichage et les actions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e3997-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="e3997-127">Par exemple, un contexte de vue est impliqué dans le message suivant ou précédent d’activation, trier le contenu du dossier et le filtrage du contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="e3997-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="e3997-128">Il n’est pas important le mécanisme de vous fournissez aux utilisateurs pour activer ces fonctionnalités, il n’est important que la sémantique de ces fonctionnalités correctement mappées sur les méthodes de l’interface **IMAPIViewContext** .</span><span class="sxs-lookup"><span data-stu-id="e3997-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="e3997-129">Un affichage de notification récepteur est un objet qui implémente le [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et gère les notifications à partir des serveurs de formulaire qui affectent vos formulaires de visionneuse et aide et les visionneuses de formulaire de travailler ensemble.</span><span class="sxs-lookup"><span data-stu-id="e3997-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="e3997-130">Pour plus d’informations, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="e3997-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

