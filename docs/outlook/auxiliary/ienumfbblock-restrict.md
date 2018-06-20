---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Limite de l’énumération à une période spécifiée.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782571"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="4921d-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="4921d-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="4921d-104">Limite de l’énumération à une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4921d-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4921d-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4921d-105">Quick info</span></span>

<span data-ttu-id="4921d-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="4921d-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="4921d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4921d-107">Parameters</span></span>

<span data-ttu-id="4921d-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="4921d-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="4921d-109">[in] L’heure de début pour limiter l’énumération.</span><span class="sxs-lookup"><span data-stu-id="4921d-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="4921d-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="4921d-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="4921d-111">[in] Heure de fin pour limiter l’énumération.</span><span class="sxs-lookup"><span data-stu-id="4921d-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4921d-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4921d-112">Return values</span></span>

<span data-ttu-id="4921d-113">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="4921d-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4921d-114">Note</span><span class="sxs-lookup"><span data-stu-id="4921d-114">Remarks</span></span>

<span data-ttu-id="4921d-115">Cette méthode réinitialise également l’énumération.</span><span class="sxs-lookup"><span data-stu-id="4921d-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4921d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4921d-116">See also</span></span>

- [<span data-ttu-id="4921d-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="4921d-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="4921d-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="4921d-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="4921d-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="4921d-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="4921d-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="4921d-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="4921d-121">Utiliser l’heure relative pour accéder aux données et de disponibilité</span><span class="sxs-lookup"><span data-stu-id="4921d-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

