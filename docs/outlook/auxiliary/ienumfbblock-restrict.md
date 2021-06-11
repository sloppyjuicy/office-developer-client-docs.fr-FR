---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Limite l’éumération à une période spécifiée.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431945"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="31ebd-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="31ebd-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="31ebd-104">Limite l’éumération à une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="31ebd-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="31ebd-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="31ebd-105">Quick info</span></span>

<span data-ttu-id="31ebd-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="31ebd-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="31ebd-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="31ebd-107">Parameters</span></span>

<span data-ttu-id="31ebd-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="31ebd-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="31ebd-109">[in] Heure de début pour limiter l’éumération.</span><span class="sxs-lookup"><span data-stu-id="31ebd-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="31ebd-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="31ebd-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="31ebd-111">[in] Heure de fin pour limiter l’éumération.</span><span class="sxs-lookup"><span data-stu-id="31ebd-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="31ebd-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="31ebd-112">Return values</span></span>

<span data-ttu-id="31ebd-113">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="31ebd-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31ebd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="31ebd-114">Remarks</span></span>

<span data-ttu-id="31ebd-115">Cette méthode réinitialise également l’éumération.</span><span class="sxs-lookup"><span data-stu-id="31ebd-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31ebd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31ebd-116">See also</span></span>

- [<span data-ttu-id="31ebd-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="31ebd-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="31ebd-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="31ebd-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="31ebd-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="31ebd-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="31ebd-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="31ebd-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="31ebd-121">Utiliser l’heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="31ebd-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

