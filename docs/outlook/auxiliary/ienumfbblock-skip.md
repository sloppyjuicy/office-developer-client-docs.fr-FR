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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425721"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="3e9c1-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="3e9c1-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="3e9c1-104">Ignore un nombre spécifié de blocs de données de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3e9c1-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3e9c1-105">Quick info</span></span>

<span data-ttu-id="3e9c1-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="3e9c1-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="3e9c1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e9c1-107">Parameters</span></span>

<span data-ttu-id="3e9c1-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="3e9c1-108">_celt_</span></span>
  
>  <span data-ttu-id="3e9c1-109">dans Nombre de blocs de disponibilité à ignorer.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3e9c1-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3e9c1-110">Return values</span></span>

<span data-ttu-id="3e9c1-111">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e9c1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e9c1-112">See also</span></span>

- [<span data-ttu-id="3e9c1-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="3e9c1-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="3e9c1-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="3e9c1-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="3e9c1-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="3e9c1-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="3e9c1-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="3e9c1-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

