---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtient le compte suivant dans l’éumérateur.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405988"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="56646-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="56646-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="56646-104">Obtient le compte suivant dans l’éumérateur.</span><span class="sxs-lookup"><span data-stu-id="56646-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="56646-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="56646-105">Quick info</span></span>

<span data-ttu-id="56646-106">Voir [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="56646-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="56646-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56646-107">Parameters</span></span>

<span data-ttu-id="56646-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="56646-108">_ppunk_</span></span>
  
> <span data-ttu-id="56646-109">[in] Pointeur vers une interface **IUnknown** que le client peut interroger pour obtenir une interface [IOlkAccount.](iolkaccount.md)</span><span class="sxs-lookup"><span data-stu-id="56646-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="56646-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="56646-110">Return values</span></span>

|<span data-ttu-id="56646-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="56646-111">**HRESULT**</span></span>|<span data-ttu-id="56646-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="56646-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56646-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="56646-113">S_OK</span></span>  <br/> |<span data-ttu-id="56646-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="56646-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="56646-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="56646-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="56646-116">L’éumérateur a atteint la fin.</span><span class="sxs-lookup"><span data-stu-id="56646-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56646-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="56646-117">Remarks</span></span>

<span data-ttu-id="56646-118">L’interface spécifiée  *par ppunk*  hérite de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="56646-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="56646-119">Le client peut interroger cette interface (à l’aide de **IUnknown::QueryInterface**) pour obtenir un pointeur vers une interface **IOlkAccount** et obtenir ou définir des informations pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="56646-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56646-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56646-120">See also</span></span>

- [<span data-ttu-id="56646-121">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="56646-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="56646-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="56646-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="56646-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="56646-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="56646-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="56646-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

