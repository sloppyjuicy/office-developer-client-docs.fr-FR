---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410678"
---
# <a name="mvi_prop"></a><span data-ttu-id="e33b3-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="e33b3-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="e33b3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e33b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e33b3-105">Définit le MVI_FLAG d’une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e33b3-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e33b3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e33b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="e33b3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e33b3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e33b3-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="e33b3-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="e33b3-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e33b3-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="e33b3-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="e33b3-110">Parameters</span></span>

 <span data-ttu-id="e33b3-111">_tag_</span><span class="sxs-lookup"><span data-stu-id="e33b3-111">_tag_</span></span>
  
> <span data-ttu-id="e33b3-112">Balise de propriété à modifier.</span><span class="sxs-lookup"><span data-stu-id="e33b3-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e33b3-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="e33b3-113">Remarks</span></span>

<span data-ttu-id="e33b3-114">Le MVI_FLAG combine les paramètres de MV_FLAG, en identifiant une propriété à valeurs multiples et en MV_INSTANCE, en demandant l’affichage d’une propriété à valeurs multiples dans un tableau en plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="e33b3-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="e33b3-115">Le type de propriété de la propriété concernée est modifié, mais l’identificateur reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="e33b3-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="e33b3-116">Par exemple, lorsque la macro MVI_PROP est appliquée à une propriété de type PT_FLOAT, son type est modifié en PT_MV_FLOAT.</span><span class="sxs-lookup"><span data-stu-id="e33b3-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="e33b3-117">Lorsqu’elles sont incluses dans un tableau, plusieurs lignes sont utilisées pour représenter la propriété qui possède une ligne pour chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="e33b3-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="e33b3-118">Les propriétés des autres colonnes sont répétées.</span><span class="sxs-lookup"><span data-stu-id="e33b3-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="e33b3-119">Pour plus d’informations sur ces indicateurs, voir [MapI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="e33b3-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e33b3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e33b3-120">See also</span></span>



[<span data-ttu-id="e33b3-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e33b3-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e33b3-122">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="e33b3-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

