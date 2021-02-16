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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412834"
---
# <a name="prop_type"></a><span data-ttu-id="0c773-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="0c773-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="0c773-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c773-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c773-105">Renvoie le type de propriété d’une balise de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0c773-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c773-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0c773-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c773-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c773-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0c773-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="0c773-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="0c773-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0c773-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="0c773-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c773-110">Parameters</span></span>

 <span data-ttu-id="0c773-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="0c773-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="0c773-112">Balise de propriété qui contient le type de propriété à retourner.</span><span class="sxs-lookup"><span data-stu-id="0c773-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c773-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c773-113">Remarks</span></span>

<span data-ttu-id="0c773-114">La **PROP_TYPE** macro peut être utilisée pour déterminer le type d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="0c773-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="0c773-115">Par exemple, l’appel PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) entraîne la PT_BINARY renvoyée.</span><span class="sxs-lookup"><span data-stu-id="0c773-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="0c773-116">Chaque balise de propriété contient le type de propriété dans le mot de bas ordre (bits 0 à 15) et l’identificateur de propriété dans le mot de haut niveau (bits 16 à 31).</span><span class="sxs-lookup"><span data-stu-id="0c773-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="0c773-117">La **macro PROP_TYPE** extrait le type de propriété et le place en bits 0 à 15 de l’ensemble à retourner.</span><span class="sxs-lookup"><span data-stu-id="0c773-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="0c773-118">Les autres bits de la valeur de retour sont des zéros.</span><span class="sxs-lookup"><span data-stu-id="0c773-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c773-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c773-119">See also</span></span>



[<span data-ttu-id="0c773-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0c773-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0c773-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="0c773-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

