---
title: Mise en œuvre d’une visionneuse de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435816"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="1b217-103">Mise en œuvre d’une visionneuse de formulaires</span><span class="sxs-lookup"><span data-stu-id="1b217-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="1b217-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b217-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b217-105">Une visionneuse de formulaires comprend trois objets : un site de message, un sink de conseil d’affichage et un contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1b217-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="1b217-106">Chacun de ces objets vous permet d’interagir avec un serveur de formulaires et ses formulaires.</span><span class="sxs-lookup"><span data-stu-id="1b217-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="1b217-107">Un site de message est un objet qui implémente l’interface [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) et aide les serveurs de formulaires à effectuer des tâches telles que le déplacement, l’enregistrement ou la suppression de messages, la création de nouveaux messages ou le lancement de serveurs de formulaires.</span><span class="sxs-lookup"><span data-stu-id="1b217-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="1b217-108">Les sites de messages sont utilisés par des formulaires pour obtenir des informations sur l’état de votre client par rapport à différents fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="1b217-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="1b217-109">Par exemple, un formulaire peut utiliser votre site de message pour obtenir un pointeur vers votre magasin de messages actuel, un message ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="1b217-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="1b217-110">Il existe deux types de méthodes dans l’interface **IMAPIMessageSite** :</span><span class="sxs-lookup"><span data-stu-id="1b217-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="1b217-111">Méthodes qui fournissent des informations aux objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="1b217-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="1b217-112">Méthodes qui manipulent des messages.</span><span class="sxs-lookup"><span data-stu-id="1b217-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="1b217-113">Les méthodes qui fournissent des informations aux objets de formulaire sont simples à implémenter.</span><span class="sxs-lookup"><span data-stu-id="1b217-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="1b217-114">Dans tous les cas, à l’exception de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), vous devez déjà avoir les informations requises par chaque méthode.</span><span class="sxs-lookup"><span data-stu-id="1b217-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="1b217-115">Les méthodes qui manipulent les messages doivent agir comme si elles avaient été déclenchées via votre interface utilisateur normale.</span><span class="sxs-lookup"><span data-stu-id="1b217-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="1b217-116">Par exemple, si un objet de formulaire appelle votre méthode [IMAPIMessageSite::NewMessage,](imapimessagesite-newmessage.md) se comporte comme si l’utilisateur avait choisi de composer un nouveau message personnalisé avec votre interface utilisateur normale.</span><span class="sxs-lookup"><span data-stu-id="1b217-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="1b217-117">Les commandes qui génèrent généralement ce comportement sont **Composer,** **Ouvrir,** **Répondre,** Répondre à tous les **destinataires** et **Forward**.</span><span class="sxs-lookup"><span data-stu-id="1b217-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="1b217-118">Un contexte d’affichage est un objet qui implémente l’interface [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) et fournit aux serveurs de formulaires un contexte pour le message actuel, ce qui permet aux serveurs de passer facilement au message suivant ou précédent dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="1b217-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="1b217-119">Un formulaire utilise un contexte d’affichage pour le partage d’informations.</span><span class="sxs-lookup"><span data-stu-id="1b217-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="1b217-120">Avec un objet de contexte d’affichage, un formulaire peut :</span><span class="sxs-lookup"><span data-stu-id="1b217-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="1b217-121">Inscrivez-vous auprès de votre client pour recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="1b217-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="1b217-122">Activez le message suivant ou précédent dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="1b217-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="1b217-123">Obtenir des informations d’impression.</span><span class="sxs-lookup"><span data-stu-id="1b217-123">Get printing information.</span></span>
    
- <span data-ttu-id="1b217-124">Obtenir l’état de votre client.</span><span class="sxs-lookup"><span data-stu-id="1b217-124">Get your client's status.</span></span>
    
- <span data-ttu-id="1b217-125">Obtenez un flux qui peut être utilisé pour enregistrer la version texte d’un message.</span><span class="sxs-lookup"><span data-stu-id="1b217-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="1b217-126">Similaires aux méthodes de l’interface [IMAPIMessageSite : IUnknown,](imapimessagesiteiunknown.md) les méthodes dans **IMAPIViewContext** correspondent aux actions de l’utilisateur et aux fonctionnalités clientes liées au contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1b217-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="1b217-127">Par exemple, un contexte d’affichage est impliqué dans l’activation du message suivant ou précédent, le tri du contenu du dossier et le filtrage du contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="1b217-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="1b217-128">Il n’est pas important de savoir quel mécanisme vous fournissez aux utilisateurs pour activer ces fonctionnalités, mais il est important que la sémantique de ces fonctionnalités soit bien m me aux méthodes de l’interface **IMAPIViewContext.**</span><span class="sxs-lookup"><span data-stu-id="1b217-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="1b217-129">Un réception de conseil d’affichage est un objet qui implémente l’interface [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et gère les notifications provenant de serveurs de formulaires qui affectent votre visionneuse et aident les utilisateurs de formulaires et de formulaires à collaborer.</span><span class="sxs-lookup"><span data-stu-id="1b217-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="1b217-130">Pour plus d’informations, voir [Envoyer et recevoir des notifications de formulaire.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="1b217-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

