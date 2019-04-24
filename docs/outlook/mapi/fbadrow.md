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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340956"
---
# <a name="fbadrow"></a><span data-ttu-id="74975-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="74975-103">FBadRow</span></span>

  
  
<span data-ttu-id="74975-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74975-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74975-105">Valide une ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="74975-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74975-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="74975-106">Header file:</span></span>  <br/> |<span data-ttu-id="74975-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="74975-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="74975-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="74975-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="74975-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="74975-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="74975-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="74975-110">Called by:</span></span>  <br/> |<span data-ttu-id="74975-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="74975-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="74975-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74975-112">Parameters</span></span>

 <span data-ttu-id="74975-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="74975-113">_lprow_</span></span>
  
> <span data-ttu-id="74975-114">dans Pointeur vers une structure [SRow](srow.md) identifiant la ligne à valider.</span><span class="sxs-lookup"><span data-stu-id="74975-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="74975-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="74975-115">Return value</span></span>

<span data-ttu-id="74975-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="74975-116">TRUE</span></span> 
  
> <span data-ttu-id="74975-117">La ligne spécifiée n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="74975-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="74975-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="74975-118">FALSE</span></span> 
  
> <span data-ttu-id="74975-119">La ligne spécifiée est valide.</span><span class="sxs-lookup"><span data-stu-id="74975-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74975-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74975-120">See also</span></span>



[<span data-ttu-id="74975-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="74975-121">FBadRowSet</span></span>](fbadrowset.md)

