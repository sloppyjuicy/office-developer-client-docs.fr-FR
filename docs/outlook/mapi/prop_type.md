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
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332759"
---
# <a name="proptype"></a><span data-ttu-id="14a40-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="14a40-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="14a40-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14a40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14a40-105">Renvoie le type de propriété d'une balise de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="14a40-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14a40-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="14a40-106">Header file:</span></span>  <br/> |<span data-ttu-id="14a40-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="14a40-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="14a40-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="14a40-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="14a40-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="14a40-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="14a40-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14a40-110">Parameters</span></span>

 <span data-ttu-id="14a40-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="14a40-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="14a40-112">Balise de propriété qui contient le type de propriété à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="14a40-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14a40-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="14a40-113">Remarks</span></span>

<span data-ttu-id="14a40-114">La macro **PROP_TYPE** peut être utilisée pour déterminer le type d'une propriété.</span><span class="sxs-lookup"><span data-stu-id="14a40-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="14a40-115">Par exemple, l'appel de PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) entraîne le renvoi de la valeur PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="14a40-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="14a40-116">Chaque balise de propriété contient le type de propriété dans le mot de poids faible (bits 0 à 15) et l'identificateur de la propriété dans le mot de poids fort (bits 16 à 31).</span><span class="sxs-lookup"><span data-stu-id="14a40-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="14a40-117">La macro **PROP_TYPE** extrait le type de propriété et le place dans les bits 0 à 15 de l'entier à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="14a40-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="14a40-118">Les autres bits de la valeur de retour sont définis sur zéros.</span><span class="sxs-lookup"><span data-stu-id="14a40-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14a40-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14a40-119">See also</span></span>



[<span data-ttu-id="14a40-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="14a40-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="14a40-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="14a40-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

