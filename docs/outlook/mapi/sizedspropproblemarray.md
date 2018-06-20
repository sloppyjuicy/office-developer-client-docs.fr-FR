---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787173"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="fd894-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="fd894-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="fd894-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd894-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd894-105">Crée une structure [SPropProblemArray](spropproblemarray.md) nommée qui contient un nombre spécifié de structures [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="fd894-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd894-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fd894-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd894-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd894-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fd894-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="fd894-108">Related structure:</span></span>  <br/> |<span data-ttu-id="fd894-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="fd894-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="fd894-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd894-110">Parameters</span></span>

<span data-ttu-id="fd894-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="fd894-111">__cprob_</span></span>
  
> <span data-ttu-id="fd894-112">Nombre de structures **SPropProblem** à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="fd894-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="fd894-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="fd894-113">__name_</span></span>
  
> <span data-ttu-id="fd894-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="fd894-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd894-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd894-115">Remarks</span></span>

<span data-ttu-id="fd894-116">Utilisez la macro **SizedSPropProblemArray** pour créer un tableau de la propriété problème avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="fd894-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="fd894-117">Pour utiliser la nouvelle structure de résultats de la macro **SizedSPropProblemArray** comme un pointeur vers une structure **SPropProblemArray** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="fd894-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="fd894-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd894-118">See also</span></span>

- [<span data-ttu-id="fd894-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="fd894-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="fd894-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="fd894-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="fd894-121">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="fd894-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

