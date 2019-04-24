---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crée une copie de l'énumérateur à l'aide de la même restriction temporelle, mais en définissant le curseur au début de l'énumérateur.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317597"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="03f13-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="03f13-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="03f13-104">Crée une copie de l'énumérateur à l'aide de la même restriction temporelle, mais en définissant le curseur au début de l'énumérateur.</span><span class="sxs-lookup"><span data-stu-id="03f13-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="03f13-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="03f13-105">Quick info</span></span>

<span data-ttu-id="03f13-106">Voir [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="03f13-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="03f13-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03f13-107">Parameters</span></span>

<span data-ttu-id="03f13-108">_ppClone_</span><span class="sxs-lookup"><span data-stu-id="03f13-108">_ppclone_</span></span>
  
> <span data-ttu-id="03f13-109">remarquer Pointeur vers un pointeur vers la copie de l'interface [IEnumFBBlock](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="03f13-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="03f13-110">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="03f13-110">Return values</span></span>

|<span data-ttu-id="03f13-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="03f13-111">**HRESULT**</span></span>|<span data-ttu-id="03f13-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="03f13-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="03f13-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="03f13-113">S_OK</span></span>  <br/> |<span data-ttu-id="03f13-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="03f13-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="03f13-115">STANDARD</span><span class="sxs-lookup"><span data-stu-id="03f13-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="03f13-116">Mémoire insuffisante pour la copie.</span><span class="sxs-lookup"><span data-stu-id="03f13-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03f13-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03f13-117">See also</span></span>

- [<span data-ttu-id="03f13-118">Constantes (API de disponibilité)</span><span class="sxs-lookup"><span data-stu-id="03f13-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="03f13-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="03f13-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="03f13-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="03f13-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="03f13-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="03f13-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="03f13-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="03f13-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

