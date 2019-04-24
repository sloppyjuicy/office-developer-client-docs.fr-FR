---
title: Vue d'ensemble de l'objet et de l'interface MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345786"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="3a183-103">Vue d'ensemble de l'objet et de l'interface MAPI</span><span class="sxs-lookup"><span data-stu-id="3a183-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="3a183-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a183-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a183-105">Un objet MAPI est une classe d'objet C++ ou une structure de données C héritée d'une ou de plusieurs interfaces MAPI, ou des collections de fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="3a183-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="3a183-106">Ces collections de fonctions connexes sont connues des développeurs C++ comme des fonctions virtuelles pures.</span><span class="sxs-lookup"><span data-stu-id="3a183-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="3a183-107">Pour une fonction virtuelle pure, MAPI fournit uniquement le prototype de fonction, pas une implémentation.</span><span class="sxs-lookup"><span data-stu-id="3a183-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="3a183-108">Une application cliente, un fournisseur de services ou MAPI doit fournir cette implémentation en créant une classe d'objet qui hérite de l'interface et conforme aux descriptions de fonction de l'API de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3a183-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="3a183-109">Une interface MAPI ne peut être instanciée que par le biais d'une classe héritée.</span><span class="sxs-lookup"><span data-stu-id="3a183-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="3a183-110">Il existe de nombreux objets MAPI différents, chaque objet qui hérite d'une interface qui est finalement héritée de l'interface [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3a183-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="3a183-111">**IUnknown** est l'interface de base com (Component Object Model) de OLE.</span><span class="sxs-lookup"><span data-stu-id="3a183-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="3a183-112">Il fournit des objets MAPI avec un mécanisme standard de communication et de contrôle.</span><span class="sxs-lookup"><span data-stu-id="3a183-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="3a183-113">COM détermine comment les implémenteurs d'objets gèrent les problèmes tels que la gestion de la mémoire, la gestion des paramètres et le multithreading.</span><span class="sxs-lookup"><span data-stu-id="3a183-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="3a183-114">En se conformant à ce modèle, un implémenteur d'objet adhère à un contrat tel que spécifié par les interfaces incluses dans l'objet.</span><span class="sxs-lookup"><span data-stu-id="3a183-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="3a183-115">De nombreuses interfaces MAPI sont directement héritées de **IUnknown**, tandis que d'autres sont indirectement héritées par le biais de l'une des deux autres interfaces de base: [IMAPIProp: IUnknown](imapipropiunknown.md) pour la gestion des propriétés et [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) pour le dossier et accès au carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="3a183-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="3a183-116">Les interfaces de base ne sont jamais implémentées en tant qu'objets autonomes distincts; elles sont toujours implémentées dans le cadre d'autres objets, objets qui implémentent des interfaces dérivées.</span><span class="sxs-lookup"><span data-stu-id="3a183-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="3a183-117">MAPI définit de nombreux types d'objets, chacun étant implémenté par un ou plusieurs composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="3a183-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="3a183-118">Les objets implémentés par les clients sont utilisés par MAPI, par les fournisseurs de services et par les composants de formulaire personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3a183-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="3a183-119">Les objets implémentés par les fournisseurs de services sont généralement utilisés par MAPI et par les clients.</span><span class="sxs-lookup"><span data-stu-id="3a183-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="3a183-120">Les objets implémentés par les fournisseurs de bibliothèques de formulaires et les serveurs de formulaires sont utilisés par les autres composants de formulaire et par les clients.</span><span class="sxs-lookup"><span data-stu-id="3a183-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a183-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a183-121">See also</span></span>



[<span data-ttu-id="3a183-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a183-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="3a183-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3a183-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="3a183-124">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="3a183-124">MAPI Concepts</span></span>](mapi-concepts.md)

