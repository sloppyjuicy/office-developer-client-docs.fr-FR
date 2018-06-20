---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtient le compte suivant dans l’énumérateur.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782753"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="7310d-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="7310d-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="7310d-104">Obtient le compte suivant dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="7310d-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7310d-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7310d-105">Quick info</span></span>

<span data-ttu-id="7310d-106">Voir [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="7310d-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="7310d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7310d-107">Parameters</span></span>

<span data-ttu-id="7310d-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="7310d-108">_ppunk_</span></span>
  
> <span data-ttu-id="7310d-109">[in] Pointeur vers une interface **IUnknown** que les clients peuvent interroger pour obtenir une interface [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="7310d-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7310d-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7310d-110">Return values</span></span>

|<span data-ttu-id="7310d-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="7310d-111">**HRESULT**</span></span>|<span data-ttu-id="7310d-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="7310d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7310d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7310d-113">S_OK</span></span>  <br/> |<span data-ttu-id="7310d-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="7310d-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="7310d-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7310d-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="7310d-116">L’énumérateur a atteint la fin.</span><span class="sxs-lookup"><span data-stu-id="7310d-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7310d-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7310d-117">Remarks</span></span>

<span data-ttu-id="7310d-118">L’interface spécifiée par *ppunk* hérite de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="7310d-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="7310d-119">Le client peut interroger cette interface (à l’aide de **IUnknown::QueryInterface**) pour obtenir un pointeur vers une interface **IOlkAccount** et obtenir ou définir les informations de ce compte.</span><span class="sxs-lookup"><span data-stu-id="7310d-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7310d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7310d-120">See also</span></span>

- [<span data-ttu-id="7310d-121">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="7310d-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="7310d-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="7310d-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="7310d-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="7310d-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="7310d-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="7310d-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

