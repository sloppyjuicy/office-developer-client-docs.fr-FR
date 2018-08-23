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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6a3d0d79d190b318d36fd9be8a3ec39d6aa7ad29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593976"
---
# <a name="mviprop"></a><span data-ttu-id="d1c4a-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="d1c4a-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="d1c4a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1c4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1c4a-105">Définit le MVI_FLAG pour une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d1c4a-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1c4a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d1c4a-106">Header file:</span></span>  <br/> |<span data-ttu-id="d1c4a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1c4a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d1c4a-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="d1c4a-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="d1c4a-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d1c4a-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="d1c4a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1c4a-110">Parameters</span></span>

 <span data-ttu-id="d1c4a-111">_balise_</span><span class="sxs-lookup"><span data-stu-id="d1c4a-111">_tag_</span></span>
  
> <span data-ttu-id="d1c4a-112">La balise de propriété à modifier.</span><span class="sxs-lookup"><span data-stu-id="d1c4a-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1c4a-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1c4a-113">Remarks</span></span>

<span data-ttu-id="d1c4a-114">Le MVI_FLAG associe la valeur de MV_FLAG, qui identifie une propriété à valeurs multiples et MV_INSTANCE, demande qu’une propriété à valeurs multiples être affichée dans un tableau dans plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="d1c4a-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="d1c4a-115">Le type de propriété de la propriété concerné est modifié, mais l’identificateur reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="d1c4a-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="d1c4a-116">Par exemple, lorsque la macro MVI_PROP est appliquée à une propriété de type PT_FLOAT, son type est modifié en PT_MV_FLOAT.</span><span class="sxs-lookup"><span data-stu-id="d1c4a-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="d1c4a-117">Lorsque inclus dans une table, plusieurs lignes sont utilisés pour représenter la propriété qui comporte une ligne pour chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="d1c4a-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="d1c4a-118">Les propriétés pour les autres colonnes sont répétées.</span><span class="sxs-lookup"><span data-stu-id="d1c4a-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="d1c4a-119">Pour plus d’informations sur ces indicateurs, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md) et [l’utilisation des colonnes à valeurs multiples](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="d1c4a-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1c4a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1c4a-120">See also</span></span>



[<span data-ttu-id="d1c4a-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d1c4a-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d1c4a-122">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="d1c4a-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

