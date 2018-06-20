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
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787191"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="4596e-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="4596e-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="4596e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4596e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4596e-105">Crée une structure [SSortOrderSet](ssortorderset.md) nommée qui contient un nombre spécifié d’ordres de tri.</span><span class="sxs-lookup"><span data-stu-id="4596e-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4596e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4596e-106">Header file:</span></span>  <br/> |<span data-ttu-id="4596e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4596e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4596e-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="4596e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="4596e-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="4596e-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="4596e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4596e-110">Parameters</span></span>

<span data-ttu-id="4596e-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="4596e-111">__csort_</span></span>
  
> <span data-ttu-id="4596e-112">Nombre d’ordres de tri à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="4596e-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="4596e-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="4596e-113">__name_</span></span>
  
> <span data-ttu-id="4596e-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="4596e-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4596e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="4596e-115">Remarks</span></span>

<span data-ttu-id="4596e-116">Utilisez la macro **SizedSSortOrderSet** pour créer un ordre de tri avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="4596e-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="4596e-117">Pour utiliser la nouvelle structure de résultats de la macro **SizedSSortOrderSet** comme un pointeur vers une structure **SSortOrderSet** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="4596e-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="4596e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4596e-118">See also</span></span>

- [<span data-ttu-id="4596e-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="4596e-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="4596e-120">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="4596e-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

