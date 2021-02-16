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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428605"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="e3ec7-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e3ec7-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="e3ec7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3ec7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3ec7-105">Crée une structure [SSortOrderSet nommée](ssortorderset.md) qui contient un nombre spécifié d’ordres de tri.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3ec7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e3ec7-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3ec7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3ec7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e3ec7-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="e3ec7-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e3ec7-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="e3ec7-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="e3ec7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3ec7-110">Parameters</span></span>

<span data-ttu-id="e3ec7-111">_ _csort_</span><span class="sxs-lookup"><span data-stu-id="e3ec7-111">_ _csort_</span></span>
  
> <span data-ttu-id="e3ec7-112">Nombre d’ordres de tri à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="e3ec7-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="e3ec7-113">_ _name_</span></span>
  
> <span data-ttu-id="e3ec7-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3ec7-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3ec7-115">Remarks</span></span>

<span data-ttu-id="e3ec7-116">Utilisez la macro **SizedSSortOrderSet** pour créer un ordre de tri avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="e3ec7-117">Pour utiliser la nouvelle structure qui résulte de la macro **SizedSSortOrderSet** comme pointeur vers une structure **SSortOrderSet,** effectuez la distribution suivante :</span><span class="sxs-lookup"><span data-stu-id="e3ec7-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="e3ec7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ec7-118">See also</span></span>

- [<span data-ttu-id="e3ec7-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e3ec7-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="e3ec7-120">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="e3ec7-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

