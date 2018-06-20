---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fd7e3b1d1284cdf4451330aabcce8fd0279ad5ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784354"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="40388-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="40388-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="40388-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40388-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40388-105">Le formulaire libérer le message en cours.</span><span class="sxs-lookup"><span data-stu-id="40388-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="40388-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40388-106">Parameters</span></span>

<span data-ttu-id="40388-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="40388-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="40388-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="40388-108">Return value</span></span>

<span data-ttu-id="40388-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="40388-109">S_OK</span></span> 
  
> <span data-ttu-id="40388-110">Le message a été publié correctement.</span><span class="sxs-lookup"><span data-stu-id="40388-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40388-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="40388-111">Remarks</span></span>

<span data-ttu-id="40388-112">Transition de formulaires dans les deux États HandsOff :</span><span class="sxs-lookup"><span data-stu-id="40388-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="40388-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="40388-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="40388-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="40388-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="40388-115">Lorsqu’un formulaire est dans un de ces États, il est en stocké de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="40388-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="40388-116">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="40388-116">Notes to implementers</span></span>

<span data-ttu-id="40388-117">Lorsqu’une visionneuse de formulaire appelle la méthode **IPersistMessage::HandsOffMessage** lorsque votre formulaire est dans un état [Normal](normal-state.md) ou [NoScribble](noscribble-state.md) , de manière récursive appel **HandsOffMessage** sur chaque message incorporé dans le message en cours et la [ IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) méthode sur chaque objet OLE incorporé dans le message en cours.</span><span class="sxs-lookup"><span data-stu-id="40388-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="40388-118">Puis relâchez le message actuel et les messages incorporés et les objets OLE.</span><span class="sxs-lookup"><span data-stu-id="40388-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="40388-119">Si votre formulaire a été dans son état Normal, la transition vers l’état HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="40388-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="40388-120">Si votre formulaire était dans l’état NoScribble, effectuer la transition à l’état HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="40388-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="40388-121">Après une transition réussie, appelez la méthode [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) du message et qu’elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="40388-121">After a successful transition, call the message's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="40388-122">Lorsqu’un utilisateur du formulaire appelle **HandsOffMessage** votre formulaire est ouvert dans un des États HandsOff, retourner E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="40388-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="40388-123">Pour plus d’informations sur les différents États d’un formulaire, voir [Les États de formulaire](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="40388-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="40388-124">Pour plus d’informations sur l’utilisation de l’état HandsOff des objets de stockage, voir la méthode [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) .</span><span class="sxs-lookup"><span data-stu-id="40388-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40388-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40388-125">See also</span></span>



[<span data-ttu-id="40388-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40388-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="40388-127">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="40388-127">Form States</span></span>](form-states.md)

