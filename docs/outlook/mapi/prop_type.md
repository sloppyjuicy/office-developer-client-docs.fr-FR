---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786930"
---
# <a name="proptype"></a><span data-ttu-id="6ad22-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="6ad22-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="6ad22-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ad22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ad22-105">Renvoie le type de propriété d’une balise de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6ad22-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ad22-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6ad22-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ad22-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ad22-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6ad22-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="6ad22-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="6ad22-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6ad22-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="6ad22-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ad22-110">Parameters</span></span>

 <span data-ttu-id="6ad22-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="6ad22-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="6ad22-112">Balise de propriété qui contient le type de propriété à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="6ad22-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ad22-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ad22-113">Remarks</span></span>

<span data-ttu-id="6ad22-114">La macro **PROP_TYPE** peut être utilisée pour déterminer le type d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="6ad22-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="6ad22-115">Par exemple, l’appel PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) entraîne la valeur PT_BINARY renvoyés.</span><span class="sxs-lookup"><span data-stu-id="6ad22-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="6ad22-116">Chaque balise de propriété contient le type de propriété dans le mot de poids faible (bits 0 à 15) et l’identificateur de propriété dans le mot de poids fort (bits 16 à 31).</span><span class="sxs-lookup"><span data-stu-id="6ad22-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="6ad22-117">La macro **PROP_TYPE** extrait le type de propriété et la place dans les bits 0 à 15 du nombre entier à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="6ad22-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="6ad22-118">Les bits restants de la valeur de retour sont définies sur zéro.</span><span class="sxs-lookup"><span data-stu-id="6ad22-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ad22-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad22-119">See also</span></span>



[<span data-ttu-id="6ad22-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6ad22-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6ad22-121">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="6ad22-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

