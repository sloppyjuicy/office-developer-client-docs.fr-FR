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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410930"
---
# <a name="sizedsrowset"></a><span data-ttu-id="12b3f-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="12b3f-103">SizedSRowSet</span></span>

<span data-ttu-id="12b3f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12b3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12b3f-105">Crée une structure [SRowSet nommée](srowset.md) qui contient un nombre spécifié de lignes.</span><span class="sxs-lookup"><span data-stu-id="12b3f-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12b3f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="12b3f-106">Header file:</span></span>  <br/> |<span data-ttu-id="12b3f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12b3f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="12b3f-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="12b3f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="12b3f-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="12b3f-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="12b3f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12b3f-110">Parameters</span></span>

<span data-ttu-id="12b3f-111">_</span><span class="sxs-lookup"><span data-stu-id="12b3f-111">_ _crow_</span></span>
  
> <span data-ttu-id="12b3f-112">Nombre de lignes à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="12b3f-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="12b3f-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="12b3f-113">_ _name_</span></span>
  
> <span data-ttu-id="12b3f-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="12b3f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12b3f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="12b3f-115">Remarks</span></span>

<span data-ttu-id="12b3f-116">Pour utiliser la nouvelle structure qui résulte de la macro **SizedSRowSet** comme pointeur vers une structure **SRowSet,** effectuez la distribution suivante :</span><span class="sxs-lookup"><span data-stu-id="12b3f-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="12b3f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12b3f-117">See also</span></span>

- [<span data-ttu-id="12b3f-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="12b3f-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="12b3f-119">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="12b3f-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

