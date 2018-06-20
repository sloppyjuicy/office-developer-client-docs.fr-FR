---
title: Implémentation de l’Interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 55bf8831af8f78767b2607c21ab54c32f6e4245f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784207"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="af849-103">Implémentation de l’Interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="af849-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="af849-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af849-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af849-105">Les méthodes de l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) , implémentée dans chaque objet MAPI, prend en charge la gestion de communication et l’objet inter-objet.</span><span class="sxs-lookup"><span data-stu-id="af849-105">The methods of the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="af849-106">**IUnknown** a trois méthodes : [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)et [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="af849-106">**IUnknown** has three methods: [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="af849-107">**QueryInterface** permet à un objet déterminer si un autre objet prend en charge une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="af849-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="af849-108">Deux objets sans connaissance préalable de l’autre fonctionnalité peuvent interagir avec **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="af849-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="af849-109">Si l’objet qui implémente **QueryInterface** ne prend pas en charge l’interface en question, il retourne un pointeur vers l’implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="af849-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="af849-110">Si l’objet ne prend pas en charge l’interface demandée, elle renvoie la valeur MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="af849-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="af849-111">**QueryInterface** retourne un pointeur d’interface demandé, il doit également augmenter le décompte de références du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="af849-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="af849-112">Décompte de références d’un objet est une valeur numérique utilisée pour gérer la durée de vie de l’objet.</span><span class="sxs-lookup"><span data-stu-id="af849-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="af849-113">Lorsque le décompte de références est supérieur à 1, ne peut pas libérer la mémoire de l’objet car il est utilisé activement.</span><span class="sxs-lookup"><span data-stu-id="af849-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="af849-114">Il est uniquement lorsque le décompte de références atteint 0 que l’objet peut être libéré en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="af849-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="af849-115">Les autres deux méthodes **IUnknown** , **AddRef** et **Release**, gérer le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="af849-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="af849-116">**AddRef** incrémente le décompte de références, lors de la **version** décrémente il.</span><span class="sxs-lookup"><span data-stu-id="af849-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="af849-117">Toutes les méthodes ou des fonctions de l’API qui renvoient des pointeurs d’interface, tels que **QueryInterface**, doivent appeler **AddRef** pour incrémenter le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="af849-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="af849-118">Toutes les implémentations des méthodes qui reçoivent des pointeurs d’interface doivent appeler **Release** pour le décrémenter lorsque le pointeur n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af849-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="af849-119">**Version** vérifie un décompte de références existantes, libérant ainsi la mémoire associée à l’interface uniquement si le nombre est 0.</span><span class="sxs-lookup"><span data-stu-id="af849-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af849-120">Parce que **AddRef** et **Release** ne sont pas nécessaires pour renvoyer des valeurs précises, les appelants de ces méthodes ne doivent pas utiliser les valeurs de retour pour déterminer si un objet est toujours valide ou a été détruit.</span><span class="sxs-lookup"><span data-stu-id="af849-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af849-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af849-121">See also</span></span>



[<span data-ttu-id="af849-122">Implémentation d’objets MAPI</span><span class="sxs-lookup"><span data-stu-id="af849-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

