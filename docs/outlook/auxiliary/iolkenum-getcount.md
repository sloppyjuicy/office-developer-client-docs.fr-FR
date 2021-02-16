---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtient le nombre de comptes dans l’éumérateur.
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421822"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="858f4-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="858f4-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="858f4-104">Obtient le nombre de comptes dans l’éumérateur.</span><span class="sxs-lookup"><span data-stu-id="858f4-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="858f4-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="858f4-105">Quick info</span></span>

<span data-ttu-id="858f4-106">Voir [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="858f4-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="858f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="858f4-107">Parameters</span></span>

<span data-ttu-id="858f4-108">_qu’est-ce que c'_</span><span class="sxs-lookup"><span data-stu-id="858f4-108">_pulCount_</span></span>
  
> <span data-ttu-id="858f4-109">[out] Pointeur vers le nombre d’objets en cours d’éumation.</span><span class="sxs-lookup"><span data-stu-id="858f4-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="858f4-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="858f4-110">Return values</span></span>

<span data-ttu-id="858f4-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="858f4-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="858f4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="858f4-112">See also</span></span>

- [<span data-ttu-id="858f4-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="858f4-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="858f4-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="858f4-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="858f4-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="858f4-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

