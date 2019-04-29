---
title: Interfaces de formulaire MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412344"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="f7698-103">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="f7698-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="f7698-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7698-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7698-105">MAPI définit les interfaces suivantes relatives aux formulaires.</span><span class="sxs-lookup"><span data-stu-id="f7698-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="f7698-106">**Nom de l'interface**</span><span class="sxs-lookup"><span data-stu-id="f7698-106">**Interface name**</span></span>|<span data-ttu-id="f7698-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="f7698-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7698-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="f7698-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="f7698-109">Manipule les objets de formulaire et gère les commandes de l'objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f7698-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="f7698-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f7698-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="f7698-111">Détermine si l'objet Form peut gérer le message suivant et modifie l'état suivant ou précédent de l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="f7698-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="f7698-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="f7698-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="f7698-113">Prend en charge l'installation, la désinstallation et la résolution des serveurs de formulaires par rapport à un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="f7698-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="f7698-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="f7698-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="f7698-115">Prend en charge l'utilisation de serveurs de formulaire d'exécution configurables.</span><span class="sxs-lookup"><span data-stu-id="f7698-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="f7698-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="f7698-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="f7698-117">Permet aux applications clientes d'utiliser des propriétés spécifiques à une classe de message.</span><span class="sxs-lookup"><span data-stu-id="f7698-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="f7698-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="f7698-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="f7698-119">Permet aux applications clientes d'obtenir des informations sur les serveurs de formulaires, d'activer des serveurs de formulaires et d'installer des serveurs de formulaires dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f7698-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="f7698-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="f7698-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="f7698-121">Utilisé pour manipuler les messages associés à des objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f7698-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="f7698-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f7698-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="f7698-123">Avertit les applications clientes qu'un événement s'est produit dans l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="f7698-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="f7698-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="f7698-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="f7698-125">Permet de répondre aux commandes suivante, précédente et supprimer dans l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="f7698-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="f7698-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="f7698-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="f7698-127">Permet d'enregistrer, d'initialiser et de charger des objets de formulaire depuis et vers le stockage des messages.</span><span class="sxs-lookup"><span data-stu-id="f7698-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="f7698-128">Pour plus d'informations sur les méthodes des interfaces de formulaire MAPI, reportez-vous à la documentation de ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="f7698-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="f7698-129">Vous n'avez pas besoin d'implémenter toutes les interfaces de formulaire MAPI afin de créer un formulaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f7698-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="f7698-130">Un formulaire lui-même nécessite uniquement d'implémenter les interfaces **IPersistMessage**, **IMAPIForm**et **IMAPIFormAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="f7698-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="f7698-131">Par ailleurs, il est également judicieux d'implémenter **IMAPIFormFactory** et **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="f7698-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="f7698-132">**IMAPIFormFactory** est utile pour la conformité OLE et **IMAPIFormInfo** permet aux applications clientes bien écrites de mieux utiliser vos formulaires.</span><span class="sxs-lookup"><span data-stu-id="f7698-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f7698-133">De manière stricte, **IMAPIFormAdviseSink** est une interface facultative.</span><span class="sxs-lookup"><span data-stu-id="f7698-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="f7698-134">Toutefois, il est vivement recommandé de l'implémenter dans vos serveurs de formulaires.</span><span class="sxs-lookup"><span data-stu-id="f7698-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="f7698-135">Cette interface est essentielle pour une interaction efficace entre les clients de messagerie et les serveurs de formulaires, en particulier lorsque plusieurs messages de la classe de message de votre serveur de formulaires sont traités.</span><span class="sxs-lookup"><span data-stu-id="f7698-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7698-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7698-136">See also</span></span>



[<span data-ttu-id="f7698-137">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="f7698-137">MAPI Forms</span></span>](mapi-forms.md)

