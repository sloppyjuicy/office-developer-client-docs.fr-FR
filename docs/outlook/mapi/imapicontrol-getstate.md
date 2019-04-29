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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419008"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="60892-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="60892-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="60892-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60892-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60892-105">Récupère une valeur qui indique si le contrôle de bouton est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="60892-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="60892-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60892-106">Parameters</span></span>

 <span data-ttu-id="60892-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60892-107">_ulFlags_</span></span>
  
> <span data-ttu-id="60892-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="60892-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="60892-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="60892-109">_lpulState_</span></span>
  
> <span data-ttu-id="60892-110">remarquer Pointeur vers une valeur qui indique l'état du contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="60892-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="60892-111">L'une des valeurs suivantes peut être renvoyée:</span><span class="sxs-lookup"><span data-stu-id="60892-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="60892-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="60892-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="60892-113">Le contrôle de bouton est désactivé et ne peut pas être cliqué.</span><span class="sxs-lookup"><span data-stu-id="60892-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="60892-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="60892-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="60892-115">Le contrôle de bouton est activé et peut être cliqué.</span><span class="sxs-lookup"><span data-stu-id="60892-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60892-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="60892-116">Return value</span></span>

<span data-ttu-id="60892-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="60892-117">S_OK</span></span> 
  
> <span data-ttu-id="60892-118">L'état du contrôle bouton a été correctement récupéré.</span><span class="sxs-lookup"><span data-stu-id="60892-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60892-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="60892-119">Remarks</span></span>

<span data-ttu-id="60892-120">Les fournisseurs de services implémentent la méthode **IMAPIControl:: GetState** pour fournir à MAPI l'état d'un contrôle de bouton.</span><span class="sxs-lookup"><span data-stu-id="60892-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="60892-121">Si le bouton est activé, il peut répondre à un clic de souris ou appuyer sur une touche.</span><span class="sxs-lookup"><span data-stu-id="60892-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="60892-122">Si elle est désactivée, le bouton apparaît estompé et ne répond pas à un clic de souris ou à une pression de touche.</span><span class="sxs-lookup"><span data-stu-id="60892-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="60892-123">Pour plus d'informations sur la façon d'implémenter **GetState** et sur les autres méthodes [IMAPIControl: IUnknown](imapicontroliunknown.md) , voir [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="60892-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60892-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60892-124">See also</span></span>



[<span data-ttu-id="60892-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="60892-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="60892-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60892-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

