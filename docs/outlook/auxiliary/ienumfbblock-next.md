---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtient le nombre spécifié suivant de blocs de données et de disponibilité dans une énumération.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782580"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="fc4ba-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="fc4ba-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="fc4ba-104">Obtient le nombre spécifié suivant de blocs de données et de disponibilité dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc4ba-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="fc4ba-105">Quick info</span></span>

<span data-ttu-id="fc4ba-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="fc4ba-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="fc4ba-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc4ba-107">Parameters</span></span>

<span data-ttu-id="fc4ba-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="fc4ba-108">_celt_</span></span>
  
> <span data-ttu-id="fc4ba-109">[in] Le nombre de données et de disponibilité se bloque dans *pblk* à récupérer.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="fc4ba-110">_PBLK_</span><span class="sxs-lookup"><span data-stu-id="fc4ba-110">_pblk_</span></span>
  
> <span data-ttu-id="fc4ba-111">[in] Pointeur vers un tableau de blocs et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="fc4ba-112">Le tableau est alloué à une taille de *celt* .</span><span class="sxs-lookup"><span data-stu-id="fc4ba-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="fc4ba-113">Les blocs de disponibilité requis sont retournés dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="fc4ba-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="fc4ba-114">_pcfetch_</span></span>
  
> <span data-ttu-id="fc4ba-115">[out] Le nombre de blocs de disponibilité retournés dans *pblk* .</span><span class="sxs-lookup"><span data-stu-id="fc4ba-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fc4ba-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="fc4ba-116">Return values</span></span>

|<span data-ttu-id="fc4ba-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-117">**HRESULT**</span></span>|<span data-ttu-id="fc4ba-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc4ba-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc4ba-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc4ba-119">S_OK</span></span>  <br/> |<span data-ttu-id="fc4ba-120">Le nombre de blocs demandé a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="fc4ba-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fc4ba-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="fc4ba-122">Le nombre de blocs demandé n’a pas été retourné.</span><span class="sxs-lookup"><span data-stu-id="fc4ba-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc4ba-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc4ba-123">See also</span></span>

- [<span data-ttu-id="fc4ba-124">Constantes (disponibilité API)</span><span class="sxs-lookup"><span data-stu-id="fc4ba-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="fc4ba-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="fc4ba-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="fc4ba-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="fc4ba-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="fc4ba-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="fc4ba-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="fc4ba-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="fc4ba-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="fc4ba-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="fc4ba-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

