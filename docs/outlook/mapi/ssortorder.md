---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439722"
---
# <a name="ssortorder"></a><span data-ttu-id="e0817-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="e0817-103">SSortOrder</span></span>
 
<span data-ttu-id="e0817-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0817-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0817-105">Définit le mode de tri des lignes d’un tableau, la colonne à utiliser comme clé de tri et le sens du tri.</span><span class="sxs-lookup"><span data-stu-id="e0817-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0817-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e0817-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0817-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0817-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="e0817-108">Members</span><span class="sxs-lookup"><span data-stu-id="e0817-108">Members</span></span>

<span data-ttu-id="e0817-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="e0817-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="e0817-110">Balise de propriété identifiant la clé de tri ou, pour un tri catégorisé, la colonne de catégorie.</span><span class="sxs-lookup"><span data-stu-id="e0817-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="e0817-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="e0817-111">**ulOrder**</span></span>
  
> <span data-ttu-id="e0817-112">Ordre dans lequel les données doivent être triées.</span><span class="sxs-lookup"><span data-stu-id="e0817-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="e0817-113">Les valeurs possibles sont les ci-après :</span><span class="sxs-lookup"><span data-stu-id="e0817-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="e0817-114">TABLE_SORT_ASCEND : le tableau doit être trié par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="e0817-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="e0817-115">TABLE_SORT_COMBINE : l’opération de tri doit créer une catégorie qui combine la propriété identifiée en tant que colonne de clé de tri dans le membre **ulPropTag** avec la colonne de clé de tri spécifiée dans la structure **SSortOrder** précédente.</span><span class="sxs-lookup"><span data-stu-id="e0817-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="e0817-116">TABLE_SORT_COMBINE ne peut être utilisé que lorsque la structure **SSortOrder** est utilisée comme entrée dans une structure [SSortOrderSet](ssortorderset.md) pour spécifier plusieurs ordres de tri pour un tri classé.</span><span class="sxs-lookup"><span data-stu-id="e0817-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="e0817-117">TABLE_SORT_COMBINE ne peut pas être utilisé dans la première structure **SSortOrder** d’une structure **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="e0817-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="e0817-118">TABLE_SORT_DESCEND : le tableau doit être trié dans l’ordre décroit.</span><span class="sxs-lookup"><span data-stu-id="e0817-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="e0817-119">TABLE_SORT_CATEG_MAX : le tableau doit être trié sur la valeur maximale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédent dans la structure **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="e0817-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="e0817-120">TABLE_SORT_CATEG_MIN : le tableau doit être trié sur la valeur minimale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédent dans la structure **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="e0817-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e0817-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0817-121">Remarks</span></span>

<span data-ttu-id="e0817-122">Une structure **SSortOrder** est utilisée pour décrire comment effectuer une opération de tri standard ou une opération de tri classée.</span><span class="sxs-lookup"><span data-stu-id="e0817-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="e0817-123">Les structures **SSortOrder** sont généralement combinées dans une structure **SSortOrderSet** pour décrire plusieurs directions et clés de tri.</span><span class="sxs-lookup"><span data-stu-id="e0817-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="e0817-124">Les structures **SSortOrderSet** sont utilisées dans les fonctions et méthodes d’interface suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0817-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="e0817-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="e0817-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="e0817-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="e0817-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="e0817-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e0817-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="e0817-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e0817-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="e0817-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e0817-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="e0817-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e0817-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="e0817-131">La plage de colonnes autorisées dans un tableau qui peut être utilisée comme clé de tri dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e0817-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="e0817-132">Les colonnes qui font partie de l’ensemble de colonnes actuel peuvent toujours être utilisées comme clés de tri.</span><span class="sxs-lookup"><span data-stu-id="e0817-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="e0817-133">Toutefois, chaque fournisseur détermine si les clés de tri peuvent être définies à l’aide des colonnes disponibles qui ne sont pas dans le jeu de colonnes actuel.</span><span class="sxs-lookup"><span data-stu-id="e0817-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="e0817-134">Une colonne disponible est une colonne qui est renvoyée par [IMAPITable::QueryColumns](imapitable-querycolumns.md) lorsque l’TBL_ALL_COLUMNS est définie.</span><span class="sxs-lookup"><span data-stu-id="e0817-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="e0817-135">Le **membre ulOrder** indique à la fois l’ordre directionnel et les informations de catégorisation, par exemple, par conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), autrement dit, thread de conversation, qui est une série de messages et de réponses.</span><span class="sxs-lookup"><span data-stu-id="e0817-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="e0817-136">Les lignes peuvent être triées dans une séquence descendante ou ascendante avec toutes les entrées NULL positionnées en dernier.</span><span class="sxs-lookup"><span data-stu-id="e0817-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="e0817-137">La TABLE_SORT_COMBINE indique que la colonne spécifiée dans **ulPropTag** doit être combinée avec la colonne de catégorie précédente pour former une catégorie composite.</span><span class="sxs-lookup"><span data-stu-id="e0817-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="e0817-138">Autrement dit, au lieu de catégoriser des valeurs uniques de colonnes individuelles, TABLE_SORT_COMBINE permet la catégorisation des valeurs uniques d’une combinaison de colonnes.</span><span class="sxs-lookup"><span data-stu-id="e0817-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="e0817-139">Par exemple, une catégorie unique peut être définie pour grouper les messages reçus d’un expéditeur particulier sur un sujet particulier.</span><span class="sxs-lookup"><span data-stu-id="e0817-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="e0817-140">Définir la valeur sur TABLE_SORT_COMBINE réduit le nombre de lignes de catégorie affichées.</span><span class="sxs-lookup"><span data-stu-id="e0817-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="e0817-141">Le tri sur des colonnes à valeurs multiples n’est pas universellement pris en charge par toutes les implémentations de tableau.</span><span class="sxs-lookup"><span data-stu-id="e0817-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="e0817-142">Si elle est prise en charge, appliquez la MV_FLAG à l’aide de la macro MVI_PROP à la balise de propriété dans le membre **ulPropTag** pour identifier la clé de tri en tant que colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="e0817-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="e0817-143">Le tri sur une colonne à valeurs multiples est basé sur l’utilisation des valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="e0817-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e0817-144">Les valeurs de membre **ulOrder** TABLE_SORT_CATEG_MAX et TABLE_SORT_CATEG_MIN peuvent ne pas être définies dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="e0817-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="e0817-145">Pour plus d’informations sur le tri standard et catégorisé, voir [Tri et catégorisation.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="e0817-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0817-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0817-146">See also</span></span>

- [<span data-ttu-id="e0817-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e0817-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="e0817-148">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e0817-148">MAPI Structures</span></span>](mapi-structures.md)

