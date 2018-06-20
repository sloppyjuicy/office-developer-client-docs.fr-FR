---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783306"
---
# <a name="fbadrow"></a><span data-ttu-id="f97ac-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="f97ac-103">FBadRow</span></span>

  
  
<span data-ttu-id="f97ac-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f97ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f97ac-105">Valide une ligne dans une table.</span><span class="sxs-lookup"><span data-stu-id="f97ac-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f97ac-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f97ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="f97ac-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f97ac-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f97ac-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="f97ac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f97ac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f97ac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f97ac-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="f97ac-110">Called by:</span></span>  <br/> |<span data-ttu-id="f97ac-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f97ac-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="f97ac-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f97ac-112">Parameters</span></span>

 <span data-ttu-id="f97ac-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="f97ac-113">_lprow_</span></span>
  
> <span data-ttu-id="f97ac-114">[in] Pointeur vers une structure [SRow](srow.md) qui identifie la ligne à valider.</span><span class="sxs-lookup"><span data-stu-id="f97ac-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f97ac-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f97ac-115">Return value</span></span>

<span data-ttu-id="f97ac-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="f97ac-116">TRUE</span></span> 
  
> <span data-ttu-id="f97ac-117">La ligne spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f97ac-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="f97ac-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="f97ac-118">FALSE</span></span> 
  
> <span data-ttu-id="f97ac-119">La ligne spécifiée est valide.</span><span class="sxs-lookup"><span data-stu-id="f97ac-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f97ac-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f97ac-120">See also</span></span>



[<span data-ttu-id="f97ac-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="f97ac-121">FBadRowSet</span></span>](fbadrowset.md)

