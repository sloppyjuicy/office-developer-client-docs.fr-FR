---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Ignore un nombre spécifié de blocs de données de disponibilité.
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317548"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="95f0c-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="95f0c-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="95f0c-104">Ignore un nombre spécifié de blocs de données de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="95f0c-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="95f0c-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="95f0c-105">Quick info</span></span>

<span data-ttu-id="95f0c-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="95f0c-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="95f0c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95f0c-107">Parameters</span></span>

<span data-ttu-id="95f0c-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="95f0c-108">_celt_</span></span>
  
>  <span data-ttu-id="95f0c-109">dans Nombre de blocs de disponibilité à ignorer.</span><span class="sxs-lookup"><span data-stu-id="95f0c-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="95f0c-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="95f0c-110">Return values</span></span>

<span data-ttu-id="95f0c-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="95f0c-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95f0c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95f0c-112">See also</span></span>

- [<span data-ttu-id="95f0c-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="95f0c-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="95f0c-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="95f0c-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="95f0c-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="95f0c-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="95f0c-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="95f0c-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

