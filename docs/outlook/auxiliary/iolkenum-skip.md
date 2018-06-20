---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Ignore un nombre spécifié de comptes dans l’énumérateur.
ms.openlocfilehash: 2791f1204cedf5e91d13923e50dfc45b981b7e26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782732"
---
# <a name="iolkenumskip"></a><span data-ttu-id="c4301-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="c4301-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="c4301-104">Ignore un nombre spécifié de comptes dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="c4301-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c4301-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c4301-105">Quick info</span></span>

<span data-ttu-id="c4301-106">Voir [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="c4301-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="c4301-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4301-107">Parameters</span></span>

<span data-ttu-id="c4301-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="c4301-108">_cSkip_</span></span>
  
> <span data-ttu-id="c4301-109">[in] Le nombre de comptes est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c4301-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c4301-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c4301-110">Return values</span></span>

<span data-ttu-id="c4301-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="c4301-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4301-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4301-112">See also</span></span>

- [<span data-ttu-id="c4301-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="c4301-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="c4301-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="c4301-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="c4301-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="c4301-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

