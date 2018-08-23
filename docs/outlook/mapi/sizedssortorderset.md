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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572563"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="f8725-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="f8725-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="f8725-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8725-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8725-105">Crée une structure [SSortOrderSet](ssortorderset.md) nommée qui contient un nombre spécifié d’ordres de tri.</span><span class="sxs-lookup"><span data-stu-id="f8725-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8725-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f8725-106">Header file:</span></span>  <br/> |<span data-ttu-id="f8725-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8725-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f8725-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="f8725-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f8725-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="f8725-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="f8725-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8725-110">Parameters</span></span>

<span data-ttu-id="f8725-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="f8725-111">__csort_</span></span>
  
> <span data-ttu-id="f8725-112">Nombre d’ordres de tri à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="f8725-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="f8725-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="f8725-113">__name_</span></span>
  
> <span data-ttu-id="f8725-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="f8725-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8725-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8725-115">Remarks</span></span>

<span data-ttu-id="f8725-116">Utilisez la macro **SizedSSortOrderSet** pour créer un ordre de tri avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="f8725-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="f8725-117">Pour utiliser la nouvelle structure de résultats de la macro **SizedSSortOrderSet** comme un pointeur vers une structure **SSortOrderSet** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="f8725-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="f8725-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8725-118">See also</span></span>

- [<span data-ttu-id="f8725-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="f8725-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="f8725-120">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="f8725-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

