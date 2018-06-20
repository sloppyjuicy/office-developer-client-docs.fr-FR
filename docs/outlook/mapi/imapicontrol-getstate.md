---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a6ae89bf9b2b16439cc06f0e106859dda10ea22c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783697"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="1b69a-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="1b69a-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="1b69a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b69a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b69a-105">Récupère une valeur qui indique si le contrôle bouton est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="1b69a-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="1b69a-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="1b69a-106">Parameters</span></span>

 <span data-ttu-id="1b69a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b69a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1b69a-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="1b69a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1b69a-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="1b69a-109">_lpulState_</span></span>
  
> <span data-ttu-id="1b69a-110">[out] Pointeur vers une valeur qui indique l’état du contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="1b69a-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="1b69a-111">Une des valeurs suivantes peut être renvoyée :</span><span class="sxs-lookup"><span data-stu-id="1b69a-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="1b69a-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="1b69a-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="1b69a-113">Le contrôle bouton est désactivé et ne peut pas être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1b69a-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="1b69a-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="1b69a-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="1b69a-115">Le contrôle bouton est activé et peut être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1b69a-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b69a-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1b69a-116">Return value</span></span>

<span data-ttu-id="1b69a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b69a-117">S_OK</span></span> 
  
> <span data-ttu-id="1b69a-118">L’état du contrôle bouton a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="1b69a-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b69a-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b69a-119">Remarks</span></span>

<span data-ttu-id="1b69a-120">Fournisseurs de services implémentent la méthode **IMAPIControl::GetState** pour fournir MAPI avec l’état d’un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="1b69a-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="1b69a-121">Si le bouton est activé, il peut répondre à un clic de souris ou la touche.</span><span class="sxs-lookup"><span data-stu-id="1b69a-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="1b69a-122">S’il est désactivé, le bouton apparaît en grisé et ne répond pas à un clic de souris ou la touche.</span><span class="sxs-lookup"><span data-stu-id="1b69a-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="1b69a-123">Pour plus d’informations sur la façon d’implémenter **GetState** et l’autre [IMAPIControl : IUnknown](imapicontroliunknown.md) méthodes, voir [Implémentation d’objet de contrôle](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1b69a-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b69a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b69a-124">See also</span></span>



[<span data-ttu-id="1b69a-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="1b69a-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="1b69a-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b69a-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

