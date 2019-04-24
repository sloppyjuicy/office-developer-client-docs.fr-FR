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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326291"
---
# <a name="mviprop"></a><span data-ttu-id="b2646-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="b2646-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="b2646-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2646-105">Définit le MVI_FLAG pour une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b2646-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2646-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b2646-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2646-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b2646-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b2646-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="b2646-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="b2646-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b2646-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="b2646-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2646-110">Parameters</span></span>

 <span data-ttu-id="b2646-111">_Numéro_</span><span class="sxs-lookup"><span data-stu-id="b2646-111">_tag_</span></span>
  
> <span data-ttu-id="b2646-112">Balise de propriété à modifier.</span><span class="sxs-lookup"><span data-stu-id="b2646-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2646-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2646-113">Remarks</span></span>

<span data-ttu-id="b2646-114">Le MVI_FLAG combine le paramètre MV_FLAG, en identifiant une propriété comme étant à valeurs multiples et MV_INSTANCE, en demandant qu'une propriété à valeurs multiples s'affiche dans un tableau sur plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="b2646-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="b2646-115">Le type de propriété de la propriété affectée est modifié, mais l'identificateur reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="b2646-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="b2646-116">Par exemple, lorsque la macro MVI_PROP est appliquée à une propriété de type PT_FLOAT, son type est modifié en PT_MV_FLOAT.</span><span class="sxs-lookup"><span data-stu-id="b2646-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="b2646-117">Lorsqu'elle est incluse dans un tableau, plusieurs lignes sont utilisées pour représenter la propriété qui contient une ligne pour chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="b2646-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="b2646-118">Les propriétés des autres colonnes sont répétées.</span><span class="sxs-lookup"><span data-stu-id="b2646-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="b2646-119">Pour plus d'informations sur ces indicateurs, voir [MAPI Property type Overview](mapi-property-type-overview.md) et [Working with multivalued Columns](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="b2646-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2646-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2646-120">See also</span></span>



[<span data-ttu-id="b2646-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b2646-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b2646-122">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="b2646-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

