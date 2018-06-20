---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtient le nombre de comptes dans l’énumérateur.
ms.openlocfilehash: dd4152a898bdaa96883bcd27ab3ec0d94e80fd90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782739"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="56557-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="56557-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="56557-104">Obtient le nombre de comptes dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="56557-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="56557-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="56557-105">Quick info</span></span>

<span data-ttu-id="56557-106">Voir [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="56557-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="56557-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56557-107">Parameters</span></span>

<span data-ttu-id="56557-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="56557-108">_pulCount_</span></span>
  
> <span data-ttu-id="56557-109">[out] Pointeur vers le nombre d’objets énumérés.</span><span class="sxs-lookup"><span data-stu-id="56557-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="56557-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="56557-110">Return values</span></span>

<span data-ttu-id="56557-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="56557-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56557-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56557-112">See also</span></span>

- [<span data-ttu-id="56557-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="56557-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="56557-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="56557-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="56557-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="56557-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

