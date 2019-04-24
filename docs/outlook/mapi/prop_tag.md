---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328566"
---
# <a name="proptag"></a><span data-ttu-id="58c22-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="58c22-103">PROP_TAG</span></span>

<span data-ttu-id="58c22-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58c22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58c22-105">Renvoie une balise de propriété créée en combinant un type et un identificateur de propriété spécifiés.</span><span class="sxs-lookup"><span data-stu-id="58c22-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58c22-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="58c22-106">Header file:</span></span>  <br/> |<span data-ttu-id="58c22-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="58c22-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="58c22-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="58c22-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="58c22-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="58c22-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="58c22-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58c22-110">Parameters</span></span>

<span data-ttu-id="58c22-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="58c22-111">_ulPropType_</span></span>
  
> <span data-ttu-id="58c22-112">Type de propriété de la nouvelle balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="58c22-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="58c22-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="58c22-113">_ulPropID_</span></span>
  
> <span data-ttu-id="58c22-114">Identificateur de propriété de la nouvelle balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="58c22-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58c22-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="58c22-115">Remarks</span></span>

<span data-ttu-id="58c22-116">La macro de **baliSe\_prop** crée une balise de propriété pour une propriété de type _ulPropType_ et l'identificateur qui est spécifié dans _ulPropID_.</span><span class="sxs-lookup"><span data-stu-id="58c22-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="58c22-117">Par exemple, une balise de propriété pour un identificateur d'entrée peut être créée à l'aide de la macro **PROP_TAG** comme suit:</span><span class="sxs-lookup"><span data-stu-id="58c22-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="58c22-118">Les 16 bits de poids faible de la balise de propriété renvoyée contiennent le type de propriété PT_BINARY et les bits de poids fort 16 contiennent l'identificateur de propriété 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="58c22-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="58c22-119">Pour plus d'informations sur les balises de propriété, voir [MAPI Property Tags](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="58c22-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58c22-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58c22-120">See also</span></span>

- [<span data-ttu-id="58c22-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="58c22-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="58c22-122">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="58c22-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

