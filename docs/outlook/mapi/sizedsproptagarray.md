---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429347"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="988cc-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="988cc-103">SizedSPropTagArray</span></span>

<span data-ttu-id="988cc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="988cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="988cc-105">Crée une structure [SPropTagArray](sproptagarray.md) nommée qui inclut un nombre spécifié de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="988cc-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="988cc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="988cc-106">Header file:</span></span>  <br/> |<span data-ttu-id="988cc-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="988cc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="988cc-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="988cc-108">Related structure:</span></span>  <br/> |<span data-ttu-id="988cc-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="988cc-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="988cc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="988cc-110">Parameters</span></span>

<span data-ttu-id="988cc-111">__CTAG_</span><span class="sxs-lookup"><span data-stu-id="988cc-111">__ctag_</span></span>
  
> <span data-ttu-id="988cc-112">Nombre de balises de propriété à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="988cc-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="988cc-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="988cc-113">__name_</span></span>
  
> <span data-ttu-id="988cc-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="988cc-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="988cc-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="988cc-115">Remarks</span></span>

<span data-ttu-id="988cc-116">Utilisez la macro **SizedSPropTagArray** pour créer un tableau de balises de propriété avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="988cc-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="988cc-117">Pour utiliser la nouvelle structure qui résulte de la macro **SizedSPropTagArray** en tant que pointeur vers une structure **SPropTagArray** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="988cc-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="988cc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="988cc-118">See also</span></span>

- [<span data-ttu-id="988cc-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="988cc-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="988cc-120">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="988cc-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

