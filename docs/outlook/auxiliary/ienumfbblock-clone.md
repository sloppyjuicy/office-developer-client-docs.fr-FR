---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crée une copie de l’énumérateur, à l’aide de la même restriction mais définissant le curseur au début de l’énumérateur.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782574"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="1fea3-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="1fea3-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="1fea3-104">Crée une copie de l’énumérateur, à l’aide de la même restriction mais définissant le curseur au début de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="1fea3-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1fea3-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1fea3-105">Quick info</span></span>

<span data-ttu-id="1fea3-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="1fea3-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="1fea3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fea3-107">Parameters</span></span>

<span data-ttu-id="1fea3-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="1fea3-108">_ppclone_</span></span>
  
> <span data-ttu-id="1fea3-109">[out] Un pointeur vers un pointeur vers la copie de l’interface [IEnumFBBlock](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="1fea3-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1fea3-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1fea3-110">Return values</span></span>

|<span data-ttu-id="1fea3-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="1fea3-111">**HRESULT**</span></span>|<span data-ttu-id="1fea3-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="1fea3-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fea3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1fea3-113">S_OK</span></span>  <br/> |<span data-ttu-id="1fea3-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="1fea3-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="1fea3-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1fea3-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="1fea3-116">La mémoire est insuffisante pour la copie.</span><span class="sxs-lookup"><span data-stu-id="1fea3-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1fea3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fea3-117">See also</span></span>

- [<span data-ttu-id="1fea3-118">Constantes (disponibilité API)</span><span class="sxs-lookup"><span data-stu-id="1fea3-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="1fea3-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="1fea3-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="1fea3-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="1fea3-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="1fea3-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="1fea3-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="1fea3-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="1fea3-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

