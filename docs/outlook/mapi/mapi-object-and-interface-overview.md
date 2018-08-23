---
title: Objet MAPI et vue d’ensemble de l’Interface
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4f69985f9cdaaba0681b823e6fe448d009ee9dfa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585709"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="83226-103">Objet MAPI et vue d’ensemble de l’Interface</span><span class="sxs-lookup"><span data-stu-id="83226-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="83226-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83226-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83226-105">Un objet MAPI est une classe d’objet C++ ou d’une structure de données C hérité d’une ou plusieurs des interfaces MAPI ou des collections de fonctions connexes.</span><span class="sxs-lookup"><span data-stu-id="83226-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="83226-106">Ces collections de fonctions connexes sont appelées pour les développeurs C++ fonctions virtuelles pures.</span><span class="sxs-lookup"><span data-stu-id="83226-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="83226-107">Pour une fonction virtuelle pure, MAPI fournit uniquement le prototype de fonction, pas une implémentation.</span><span class="sxs-lookup"><span data-stu-id="83226-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="83226-108">Il est prévu qu’une application cliente, un fournisseur de services ou MAPI fournira cette implémentation en créant un objet de classe qui hérite de l’interface et est conforme à la description de la fonction de l’API de messagerie.</span><span class="sxs-lookup"><span data-stu-id="83226-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="83226-109">Une interface MAPI peut être instanciée uniquement par le biais d’une classe héritée.</span><span class="sxs-lookup"><span data-stu-id="83226-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="83226-110">Il existe de nombreux objets MAPI différents, chaque objet qui hérite d’une interface qui est finalement héritée de l’interface [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="83226-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="83226-111">**IUnknown** est l’interface de base OLE composant COM (Object Model).</span><span class="sxs-lookup"><span data-stu-id="83226-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="83226-112">Il fournit des objets MAPI avec un mécanisme standard de communication et de contrôle.</span><span class="sxs-lookup"><span data-stu-id="83226-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="83226-113">COM détermine comment gérer les problèmes de gestion de la mémoire, gestion de paramètre, l’implémentation d’objet et le multithreading.</span><span class="sxs-lookup"><span data-stu-id="83226-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="83226-114">En répondant à ce modèle, une implémentation de l’objet est conforme à un contrat tel que spécifié par les interfaces inclus dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="83226-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="83226-115">Nombre d’interfaces MAPI est héritée directement à partir **IUnknown**, tandis que d’autres personnes sont héritées indirectement par le biais d’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) pour la gestion de la propriété et [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) pour le dossier et accès au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="83226-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="83226-116">Interfaces de base ne sont jamais implémentées comme distinct, objets autonomes ; ils sont toujours exécutées dans le cadre d’autres objets, les objets qui implémentent les interfaces dérivées.</span><span class="sxs-lookup"><span data-stu-id="83226-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="83226-117">MAPI définit de nombreux types d’objets, chacun implémenté par un ou plusieurs composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="83226-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="83226-118">Objets implémentés par les clients qui sont utilisés par MAPI, les fournisseurs de services et par les composants de formulaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="83226-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="83226-119">Objets implémentés par les fournisseurs de services sont généralement utilisés par MAPI et par les clients.</span><span class="sxs-lookup"><span data-stu-id="83226-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="83226-120">Objets implémentés par les fournisseurs de bibliothèques de formulaires et les serveurs de formulaire sont utilisés par d’autres composants de formulaire et par les clients.</span><span class="sxs-lookup"><span data-stu-id="83226-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83226-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83226-121">See also</span></span>



[<span data-ttu-id="83226-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83226-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="83226-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="83226-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="83226-124">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="83226-124">MAPI Concepts</span></span>](mapi-concepts.md)

