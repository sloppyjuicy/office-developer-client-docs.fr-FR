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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573620"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="a7322-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a7322-103">SizedSPropTagArray</span></span>

<span data-ttu-id="a7322-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7322-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7322-105">Crée une structure [SPropTagArray](sproptagarray.md) nommée qui inclut un nombre spécifié de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="a7322-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7322-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a7322-106">Header file:</span></span>  <br/> |<span data-ttu-id="a7322-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7322-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a7322-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="a7322-108">Related structure:</span></span>  <br/> |<span data-ttu-id="a7322-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="a7322-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="a7322-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7322-110">Parameters</span></span>

<span data-ttu-id="a7322-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="a7322-111">__ctag_</span></span>
  
> <span data-ttu-id="a7322-112">Nombre de balises de propriétés à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="a7322-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="a7322-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="a7322-113">__name_</span></span>
  
> <span data-ttu-id="a7322-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="a7322-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7322-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7322-115">Remarks</span></span>

<span data-ttu-id="a7322-116">Utilisez la macro **SizedSPropTagArray** pour créer un tableau de balise de propriété avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="a7322-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="a7322-117">Pour utiliser la nouvelle structure de résultats de la macro **SizedSPropTagArray** comme un pointeur vers une structure **SPropTagArray** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="a7322-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="a7322-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7322-118">See also</span></span>

- [<span data-ttu-id="a7322-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a7322-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="a7322-120">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="a7322-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

