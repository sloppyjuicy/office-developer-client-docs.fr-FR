---
title: Interfaces de formulaires MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f37d398167e8210a2fd67ff08e63572eb6c9db9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585723"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="07d78-103">Interfaces de formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="07d78-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="07d78-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07d78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07d78-105">MAPI définit les interfaces suivantes relatives aux formulaires.</span><span class="sxs-lookup"><span data-stu-id="07d78-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="07d78-106">**Nom de l’interface**</span><span class="sxs-lookup"><span data-stu-id="07d78-106">**Interface name**</span></span>|<span data-ttu-id="07d78-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="07d78-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07d78-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="07d78-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="07d78-109">Manipule les objets de formulaire et gère les commandes objet.</span><span class="sxs-lookup"><span data-stu-id="07d78-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="07d78-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="07d78-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="07d78-111">Détermine si l’objet form peut gérer le message suivant et modifie l’état suivant ou précédent de l’objet form.</span><span class="sxs-lookup"><span data-stu-id="07d78-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="07d78-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="07d78-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="07d78-113">Prend en charge d’installation, désinstallation et la résolution des serveurs de formulaire par rapport à un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="07d78-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="07d78-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="07d78-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="07d78-115">Prend en charge l’utilisation de serveurs configurable exécution du formulaire.</span><span class="sxs-lookup"><span data-stu-id="07d78-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="07d78-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="07d78-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="07d78-117">Permet aux applications de client travailler avec les propriétés qui sont spécifiques à une classe de message.</span><span class="sxs-lookup"><span data-stu-id="07d78-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="07d78-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="07d78-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="07d78-119">Permet aux applications clientes obtenir des informations sur les serveurs de formulaire active des serveurs de formulaire et installe les serveurs de formulaire dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="07d78-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="07d78-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="07d78-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="07d78-121">Utilisé pour manipuler les messages associés aux objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="07d78-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="07d78-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="07d78-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="07d78-123">Avertit les applications de client qu’un événement s’est produite dans l’objet form.</span><span class="sxs-lookup"><span data-stu-id="07d78-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="07d78-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="07d78-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="07d78-125">Utilisé pour répondre à des commandes Delete, précédent et suivant dans l’objet form.</span><span class="sxs-lookup"><span data-stu-id="07d78-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="07d78-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="07d78-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="07d78-127">Utilisé pour enregistrer, initialiser et charger des objets de formulaire vers et depuis le stockage des messages.</span><span class="sxs-lookup"><span data-stu-id="07d78-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="07d78-128">Pour plus d’informations sur les méthodes des interfaces de formulaire MAPI, voir la documentation de ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="07d78-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="07d78-129">Vous n’êtes pas obligé de toutes les interfaces de formulaire MAPI implémenter afin de créer un formulaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="07d78-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="07d78-130">Un formulaire proprement dite nécessite uniquement que vous implémentez **IPersistMessage**, **IMAPIForm**, et les interfaces **IMAPIFormAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="07d78-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="07d78-131">En outre, il est également conseillé de mettre en œuvre **IMAPIFormFactory** et **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="07d78-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="07d78-132">**IMAPIFormFactory** est utile pour la conformité OLE et **IMAPIFormInfo** permet aux applications clientes bien écrites utilisent plus efficacement vos formulaires.</span><span class="sxs-lookup"><span data-stu-id="07d78-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="07d78-133">En principe, **IMAPIFormAdviseSink** est une interface facultative.</span><span class="sxs-lookup"><span data-stu-id="07d78-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="07d78-134">Toutefois, il est fortement recommandé d’implémenter dans vos serveurs de formulaire.</span><span class="sxs-lookup"><span data-stu-id="07d78-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="07d78-135">Cette interface est essentielle pour une interaction efficace entre les clients de messagerie et les serveurs de formulaire, en particulier lorsque plusieurs messages du votre serveur formulaire classe de message sont traitées.</span><span class="sxs-lookup"><span data-stu-id="07d78-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07d78-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07d78-136">See also</span></span>



[<span data-ttu-id="07d78-137">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="07d78-137">MAPI Forms</span></span>](mapi-forms.md)

