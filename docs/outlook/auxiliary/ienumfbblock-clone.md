---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en fixant le curseur au début de l’éumérateur.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413401"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="0c82d-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="0c82d-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="0c82d-104">Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en fixant le curseur au début de l’éumérateur.</span><span class="sxs-lookup"><span data-stu-id="0c82d-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0c82d-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0c82d-105">Quick info</span></span>

<span data-ttu-id="0c82d-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="0c82d-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="0c82d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0c82d-107">Parameters</span></span>

<span data-ttu-id="0c82d-108">_ccplone_</span><span class="sxs-lookup"><span data-stu-id="0c82d-108">_ppclone_</span></span>
  
> <span data-ttu-id="0c82d-109">[out] Pointeur vers le pointeur vers la copie de [l’interface IEnumFBBlock.](ienumfbblock.md)</span><span class="sxs-lookup"><span data-stu-id="0c82d-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0c82d-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0c82d-110">Return values</span></span>

|<span data-ttu-id="0c82d-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="0c82d-111">**HRESULT**</span></span>|<span data-ttu-id="0c82d-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c82d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c82d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c82d-113">S_OK</span></span>  <br/> |<span data-ttu-id="0c82d-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0c82d-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="0c82d-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="0c82d-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="0c82d-116">Mémoire insuffisante pour effectuer la copie.</span><span class="sxs-lookup"><span data-stu-id="0c82d-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c82d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c82d-117">See also</span></span>

- [<span data-ttu-id="0c82d-118">Constantes (API de libre/occupé)</span><span class="sxs-lookup"><span data-stu-id="0c82d-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="0c82d-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="0c82d-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="0c82d-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="0c82d-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="0c82d-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="0c82d-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="0c82d-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="0c82d-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

