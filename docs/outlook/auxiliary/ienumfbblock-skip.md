---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Ignore un nombre spécifié de blocs de données et de disponibilité.
ms.openlocfilehash: 63f699d09e143a879702e8dc76beb8a969a77b82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782573"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="ea0a6-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="ea0a6-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="ea0a6-104">Ignore un nombre spécifié de blocs de données et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="ea0a6-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ea0a6-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ea0a6-105">Quick info</span></span>

<span data-ttu-id="ea0a6-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="ea0a6-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="ea0a6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea0a6-107">Parameters</span></span>

<span data-ttu-id="ea0a6-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="ea0a6-108">_celt_</span></span>
  
>  <span data-ttu-id="ea0a6-109">[in] Le nombre de blocs de disponibilité à ignorer.</span><span class="sxs-lookup"><span data-stu-id="ea0a6-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ea0a6-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ea0a6-110">Return values</span></span>

<span data-ttu-id="ea0a6-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="ea0a6-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea0a6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea0a6-112">See also</span></span>

- [<span data-ttu-id="ea0a6-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="ea0a6-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="ea0a6-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="ea0a6-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="ea0a6-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="ea0a6-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="ea0a6-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="ea0a6-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

