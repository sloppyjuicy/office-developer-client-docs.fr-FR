---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282627"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="7a285-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="7a285-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="7a285-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a285-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a285-105">Crée une structure [SSortOrderSet](ssortorderset.md) nommée qui contient un nombre spécifié d'ordres de tri.</span><span class="sxs-lookup"><span data-stu-id="7a285-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a285-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7a285-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a285-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7a285-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7a285-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="7a285-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7a285-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="7a285-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="7a285-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a285-110">Parameters</span></span>

<span data-ttu-id="7a285-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="7a285-111">__csort_</span></span>
  
> <span data-ttu-id="7a285-112">Nombre d'ordres de tri à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="7a285-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="7a285-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="7a285-113">__name_</span></span>
  
> <span data-ttu-id="7a285-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="7a285-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a285-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="7a285-115">Remarks</span></span>

<span data-ttu-id="7a285-116">Utilisez la macro **SizedSSortOrderSet** pour créer un ensemble d'ordres de tri avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="7a285-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="7a285-117">Pour utiliser la nouvelle structure qui résulte de la macro **SizedSSortOrderSet** en tant que pointeur vers une structure **SSortOrderSet** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="7a285-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="7a285-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a285-118">See also</span></span>

- [<span data-ttu-id="7a285-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="7a285-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="7a285-120">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="7a285-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

