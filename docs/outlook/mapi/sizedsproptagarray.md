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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787176"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="95382-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="95382-103">SizedSPropTagArray</span></span>

<span data-ttu-id="95382-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95382-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95382-105">Crée une structure [SPropTagArray](sproptagarray.md) nommée qui inclut un nombre spécifié de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="95382-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95382-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="95382-106">Header file:</span></span>  <br/> |<span data-ttu-id="95382-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95382-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="95382-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="95382-108">Related structure:</span></span>  <br/> |<span data-ttu-id="95382-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="95382-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="95382-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95382-110">Parameters</span></span>

<span data-ttu-id="95382-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="95382-111">__ctag_</span></span>
  
> <span data-ttu-id="95382-112">Nombre de balises de propriétés à inclure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="95382-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="95382-113">__nom_</span><span class="sxs-lookup"><span data-stu-id="95382-113">__name_</span></span>
  
> <span data-ttu-id="95382-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="95382-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95382-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="95382-115">Remarks</span></span>

<span data-ttu-id="95382-116">Utilisez la macro **SizedSPropTagArray** pour créer un tableau de balise de propriété avec des limites explicites.</span><span class="sxs-lookup"><span data-stu-id="95382-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="95382-117">Pour utiliser la nouvelle structure de résultats de la macro **SizedSPropTagArray** comme un pointeur vers une structure **SPropTagArray** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="95382-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="95382-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95382-118">See also</span></span>

- [<span data-ttu-id="95382-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="95382-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="95382-120">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="95382-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

