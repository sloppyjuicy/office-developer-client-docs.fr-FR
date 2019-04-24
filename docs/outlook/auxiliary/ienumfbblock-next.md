---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtient le prochain nombre spécifié de blocs de données de disponibilité dans une énumération.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319592"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="7ee30-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="7ee30-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="7ee30-104">Obtient le prochain nombre spécifié de blocs de données de disponibilité dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="7ee30-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7ee30-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7ee30-105">Quick info</span></span>

<span data-ttu-id="7ee30-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="7ee30-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="7ee30-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ee30-107">Parameters</span></span>

<span data-ttu-id="7ee30-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="7ee30-108">_celt_</span></span>
  
> <span data-ttu-id="7ee30-109">dans Nombre de blocs de données de disponibilité dans *pblk* à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7ee30-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="7ee30-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="7ee30-110">_pblk_</span></span>
  
> <span data-ttu-id="7ee30-111">dans Pointeur vers un tableau de blocs de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="7ee30-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="7ee30-112">La taille de la matrice est de *celt* .</span><span class="sxs-lookup"><span data-stu-id="7ee30-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="7ee30-113">Les blocs de disponibilité demandés sont renvoyés dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="7ee30-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="7ee30-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="7ee30-114">_pcfetch_</span></span>
  
> <span data-ttu-id="7ee30-115">remarquer Nombre de blocs de disponibilité réellement retournés dans *pblk* .</span><span class="sxs-lookup"><span data-stu-id="7ee30-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7ee30-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7ee30-116">Return values</span></span>

|<span data-ttu-id="7ee30-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="7ee30-117">**HRESULT**</span></span>|<span data-ttu-id="7ee30-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7ee30-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ee30-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ee30-119">S_OK</span></span>  <br/> |<span data-ttu-id="7ee30-120">Le nombre de blocs demandé a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7ee30-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="7ee30-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7ee30-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="7ee30-122">Le nombre de blocs demandé n'a pas été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7ee30-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ee30-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ee30-123">See also</span></span>

- [<span data-ttu-id="7ee30-124">Constantes (API de disponibilité)</span><span class="sxs-lookup"><span data-stu-id="7ee30-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="7ee30-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="7ee30-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="7ee30-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="7ee30-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="7ee30-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="7ee30-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="7ee30-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="7ee30-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="7ee30-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="7ee30-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

