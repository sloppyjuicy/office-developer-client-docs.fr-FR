---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtient le compte suivant dans l'énumérateur.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321895"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="ddf57-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="ddf57-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="ddf57-104">Obtient le compte suivant dans l'énumérateur.</span><span class="sxs-lookup"><span data-stu-id="ddf57-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ddf57-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ddf57-105">Quick info</span></span>

<span data-ttu-id="ddf57-106">Voir [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="ddf57-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="ddf57-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddf57-107">Parameters</span></span>

<span data-ttu-id="ddf57-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="ddf57-108">_ppunk_</span></span>
  
> <span data-ttu-id="ddf57-109">dans Pointeur vers une interface **IUnknown** que le client peut interroger pour obtenir une interface [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf57-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ddf57-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ddf57-110">Return values</span></span>

|<span data-ttu-id="ddf57-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="ddf57-111">**HRESULT**</span></span>|<span data-ttu-id="ddf57-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="ddf57-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddf57-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ddf57-113">S_OK</span></span>  <br/> |<span data-ttu-id="ddf57-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="ddf57-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="ddf57-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ddf57-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="ddf57-116">L'énumérateur a atteint la fin.</span><span class="sxs-lookup"><span data-stu-id="ddf57-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddf57-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="ddf57-117">Remarks</span></span>

<span data-ttu-id="ddf57-118">L'interface spécifiée par *ppunk* hérite de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="ddf57-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="ddf57-119">Le client peut interroger cette interface (en utilisant **IUnknown:: QueryInterface**) pour obtenir un pointeur vers une interface **IOlkAccount** et obtenir ou définir des informations pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="ddf57-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddf57-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddf57-120">See also</span></span>

- [<span data-ttu-id="ddf57-121">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="ddf57-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="ddf57-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="ddf57-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="ddf57-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="ddf57-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="ddf57-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="ddf57-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

