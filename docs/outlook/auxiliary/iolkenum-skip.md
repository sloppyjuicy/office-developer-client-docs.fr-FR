---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Ignore un nombre spécifié de comptes dans l'énumérateur.
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404777"
---
# <a name="iolkenumskip"></a><span data-ttu-id="910db-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="910db-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="910db-104">Ignore un nombre spécifié de comptes dans l'énumérateur.</span><span class="sxs-lookup"><span data-stu-id="910db-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="910db-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="910db-105">Quick info</span></span>

<span data-ttu-id="910db-106">Voir [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="910db-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="910db-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="910db-107">Parameters</span></span>

<span data-ttu-id="910db-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="910db-108">_cSkip_</span></span>
  
> <span data-ttu-id="910db-109">dans Nombre de comptes à ignorer.</span><span class="sxs-lookup"><span data-stu-id="910db-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="910db-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="910db-110">Return values</span></span>

<span data-ttu-id="910db-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="910db-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="910db-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="910db-112">See also</span></span>

- [<span data-ttu-id="910db-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="910db-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="910db-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="910db-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="910db-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="910db-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

