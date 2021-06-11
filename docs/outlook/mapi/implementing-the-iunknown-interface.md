---
title: Mise en œuvre de l’interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310044"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="a9ff3-103">Mise en œuvre de l’interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9ff3-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="a9ff3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9ff3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9ff3-105">Les méthodes de l’interface [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) implémentées dans chaque objet MAPI, s’appliquent à la communication entre objets et à la gestion des objets.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="a9ff3-106">**IUnknown** a trois méthodes : [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)et [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9ff3-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="a9ff3-107">**QueryInterface permet** à un objet de déterminer si un autre objet prend en charge une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="a9ff3-108">Avec **QueryInterface**, deux objets sans connaissance préalable des fonctionnalités de l’un et de l’autre peuvent interagir.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="a9ff3-109">Si l’objet qui implémente **QueryInterface prend** en charge l’interface en question, il renvoie un pointeur vers l’implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="a9ff3-110">Si l’objet ne prend pas en charge l’interface demandée, il renvoie la MAPI_E_INTERFACE_NOT_SUPPORTED valeur.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="a9ff3-111">Lorsque **QueryInterface renvoie** un pointeur d’interface demandé, il doit également augmenter le nombre de références du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="a9ff3-112">Le nombre de références d’un objet est une valeur numérique utilisée pour gérer la durée de vie de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="a9ff3-113">Lorsque le nombre de références est supérieur à 1, la mémoire de l’objet ne peut pas être libérée car elle est activement utilisée.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="a9ff3-114">Ce n’est que lorsque le nombre de références passe à 0 que l’objet peut être libéré en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="a9ff3-115">Les deux autres **méthodes IUnknown,** **AddRef** et **Release,** gèrent le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="a9ff3-116">**AddRef** incrémente le nombre de références, tandis **que Release** le décrémente.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="a9ff3-117">Toutes les méthodes ou fonctions API qui retournent des pointeurs d’interface, telles que **QueryInterface,** doivent appeler **AddRef** pour incrémenter le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="a9ff3-118">Toutes les implémentations de méthodes qui reçoivent des pointeurs d’interface doivent appeler **Release** pour décrémenter le nombre lorsque le pointeur n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="a9ff3-119">**Les** libérations vérifient le nombre de références existantes, en libérant la mémoire associée à l’interface uniquement si le nombre est 0.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a9ff3-120">Étant **donné qu’AddRef** et **Release** ne sont pas requis pour renvoyer des valeurs précises, les appelants de ces méthodes ne doivent pas utiliser les valeurs de retour pour déterminer si un objet est toujours valide ou a été détruit.</span><span class="sxs-lookup"><span data-stu-id="a9ff3-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9ff3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9ff3-121">See also</span></span>



[<span data-ttu-id="a9ff3-122">Mise en œuvre des objets MAPI</span><span class="sxs-lookup"><span data-stu-id="a9ff3-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

