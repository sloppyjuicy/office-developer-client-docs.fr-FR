---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282641"
---
# <a name="sizedsrowset"></a><span data-ttu-id="956af-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="956af-103">SizedSRowSet</span></span>

<span data-ttu-id="956af-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="956af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="956af-105">Crée une structure [SRowSet](srowset.md) nommée qui contient un nombre spécifié de lignes.</span><span class="sxs-lookup"><span data-stu-id="956af-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="956af-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="956af-106">Header file:</span></span>  <br/> |<span data-ttu-id="956af-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="956af-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="956af-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="956af-108">Related structure:</span></span>  <br/> |<span data-ttu-id="956af-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="956af-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="956af-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="956af-110">Parameters</span></span>

<span data-ttu-id="956af-111">__Crow_</span><span class="sxs-lookup"><span data-stu-id="956af-111">__crow_</span></span>
  
> <span data-ttu-id="956af-112">Nombre de lignes à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="956af-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="956af-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="956af-113">__name_</span></span>
  
> <span data-ttu-id="956af-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="956af-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="956af-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="956af-115">Remarks</span></span>

<span data-ttu-id="956af-116">Pour utiliser la nouvelle structure qui résulte de la macro **SizedSRowSet** en tant que pointeur vers une structure **SRowSet** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="956af-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="956af-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="956af-117">See also</span></span>

- [<span data-ttu-id="956af-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="956af-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="956af-119">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="956af-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

