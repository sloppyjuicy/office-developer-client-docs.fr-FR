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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590161"
---
# <a name="fbadrow"></a><span data-ttu-id="41255-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="41255-103">FBadRow</span></span>

  
  
<span data-ttu-id="41255-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41255-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41255-105">Valide une ligne dans une table.</span><span class="sxs-lookup"><span data-stu-id="41255-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41255-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="41255-106">Header file:</span></span>  <br/> |<span data-ttu-id="41255-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="41255-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="41255-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="41255-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="41255-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="41255-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="41255-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="41255-110">Called by:</span></span>  <br/> |<span data-ttu-id="41255-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="41255-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="41255-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41255-112">Parameters</span></span>

 <span data-ttu-id="41255-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="41255-113">_lprow_</span></span>
  
> <span data-ttu-id="41255-114">[in] Pointeur vers une structure [SRow](srow.md) qui identifie la ligne à valider.</span><span class="sxs-lookup"><span data-stu-id="41255-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41255-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="41255-115">Return value</span></span>

<span data-ttu-id="41255-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="41255-116">TRUE</span></span> 
  
> <span data-ttu-id="41255-117">La ligne spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="41255-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="41255-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="41255-118">FALSE</span></span> 
  
> <span data-ttu-id="41255-119">La ligne spécifiée est valide.</span><span class="sxs-lookup"><span data-stu-id="41255-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41255-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41255-120">See also</span></span>



[<span data-ttu-id="41255-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="41255-121">FBadRowSet</span></span>](fbadrowset.md)

