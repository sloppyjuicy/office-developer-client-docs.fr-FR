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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309715"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="2aa69-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="2aa69-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="2aa69-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aa69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aa69-105">Entraîne la libération du message actuel par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="2aa69-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="2aa69-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2aa69-106">Parameters</span></span>

<span data-ttu-id="2aa69-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="2aa69-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="2aa69-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2aa69-108">Return value</span></span>

<span data-ttu-id="2aa69-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="2aa69-109">S_OK</span></span> 
  
> <span data-ttu-id="2aa69-110">Le message a été libéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="2aa69-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2aa69-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2aa69-111">Remarks</span></span>

<span data-ttu-id="2aa69-112">Transition de formulaires vers deux États HandsOff:</span><span class="sxs-lookup"><span data-stu-id="2aa69-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="2aa69-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="2aa69-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="2aa69-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="2aa69-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="2aa69-115">Lorsqu'un formulaire est dans l'un de ces États, il est en cours de stockage permanent.</span><span class="sxs-lookup"><span data-stu-id="2aa69-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2aa69-116">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="2aa69-116">Notes to implementers</span></span>

<span data-ttu-id="2aa69-117">Lorsqu'une visionneuse de formulaires appelle la méthode **IPersistMessage:: HandsOffMessage** alors que votre formulaire est dans l'état [normal](normal-state.md) ou noscribble, appelez **HandsOffMessage** sur chaque message incorporé dans le message actif et [](noscribble-state.md) le [ IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) méthode sur chaque objet OLE incorporé dans le message actif.</span><span class="sxs-lookup"><span data-stu-id="2aa69-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="2aa69-118">Ensuite, relâchez le message en cours, ainsi que tous les messages incorporés et les objets OLE.</span><span class="sxs-lookup"><span data-stu-id="2aa69-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="2aa69-119">Si votre formulaire était dans un état normal, passez à l'État HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="2aa69-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="2aa69-120">Si votre formulaire était dans l'État noScribble, passez à l'État HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="2aa69-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="2aa69-121">Après une transition réussie, appelez la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de message et renvoyez S_OK.</span><span class="sxs-lookup"><span data-stu-id="2aa69-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="2aa69-122">Lorsqu'une visionneuse de formulaires appelle **HandsOffMessage** alors que votre formulaire se trouve dans l'un des États HandsOff, renvoie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="2aa69-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="2aa69-123">Pour plus d'informations sur les différents États d'un formulaire, consultez la rubrique [États de formulaire](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="2aa69-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="2aa69-124">Pour plus d'informations sur l'utilisation de l'État HandsOff des objets de stockage, voir la méthode [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2aa69-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2aa69-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aa69-125">See also</span></span>



[<span data-ttu-id="2aa69-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2aa69-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="2aa69-127">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="2aa69-127">Form States</span></span>](form-states.md)

