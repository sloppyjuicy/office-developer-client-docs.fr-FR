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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 331dc05b30390bb803d186f157e0fe9edb779ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571667"
---
# <a name="ssortorder"></a><span data-ttu-id="8d2bd-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="8d2bd-103">SSortOrder</span></span>
 
<span data-ttu-id="8d2bd-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d2bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d2bd-105">Définit comment trier les lignes d’une table, une colonne à utiliser comme la clé de tri et le sens du tri.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d2bd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8d2bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d2bd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d2bd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="8d2bd-108">Members</span><span class="sxs-lookup"><span data-stu-id="8d2bd-108">Members</span></span>

<span data-ttu-id="8d2bd-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="8d2bd-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="8d2bd-110">Balise de propriété identifiant le tri clé ou, pour un tri par catégorie, la colonne catégorie.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="8d2bd-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="8d2bd-111">**ulOrder**</span></span>
  
> <span data-ttu-id="8d2bd-112">L’ordre dans lequel les données sont à trier.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="8d2bd-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d2bd-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="8d2bd-114">TABLE_SORT_ASCEND : Le tableau doit être trié par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="8d2bd-115">TABLE_SORT_COMBINE : L’opération de tri doit créer une catégorie qui associe la propriété identifiée en tant que colonne de clé de tri dans le membre **ulPropTag** avec la colonne de clé de tri spécifiée dans la structure **SSortOrder** précédente.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="8d2bd-116">TABLE_SORT_COMBINE peut être utilisé uniquement lorsque la structure **SSortOrder** est utilisée comme une entrée dans une structure [SSortOrderSet](ssortorderset.md) pour spécifier plusieurs ordres de tri pour un tri par catégorie.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="8d2bd-117">TABLE_SORT_COMBINE ne peut pas être utilisé dans la première structure **SSortOrder** dans une structure **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="8d2bd-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="8d2bd-118">TABLE_SORT_DESCEND : Le tableau doit être trié par ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="8d2bd-119">TABLE_SORT_CATEG_MAX : Le tableau doit être trié sur la valeur maximale du membre **ulPropTag** pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédente dans la structure **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="8d2bd-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="8d2bd-120">TABLE_SORT_CATEG_MIN : Le tableau doit être trié sur la valeur minimale du membre pour les lignes de données dans les catégories spécifiées par l’ordre de tri précédente dans la structure **SSortOrderSet** en **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="8d2bd-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8d2bd-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d2bd-121">Remarks</span></span>

<span data-ttu-id="8d2bd-122">Une structure **SSortOrder** est utilisée pour décrire comment effectuer une opération de tri standard ou une opération de tri par catégorie.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="8d2bd-123">Structures **SSortOrder** sont généralement combinées en une structure **SSortOrderSet** pour décrire plusieurs clés de tri et des instructions.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="8d2bd-124">Structures **SSortOrderSet** sont utilisés dans les méthodes d’interface les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d2bd-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="8d2bd-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="8d2bd-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="8d2bd-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="8d2bd-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="8d2bd-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="8d2bd-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="8d2bd-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8d2bd-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="8d2bd-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="8d2bd-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="8d2bd-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="8d2bd-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="8d2bd-131">La plage de colonnes autorisés dans une table qui peut être utilisé comme une clé de tri dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="8d2bd-132">Colonnes qui font partie de l’ensemble actuel de la colonne peuvent toujours être utilisés en tant que clés de tri.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="8d2bd-133">Toutefois, chaque fournisseur détermine si les clés de tri peuvent être définis à l’aide des colonnes disponibles sont définies pas dans la colonne en cours.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="8d2bd-134">Une colonne disponible est une colonne qui est renvoyée à partir de [IMAPITable::QueryColumns](imapitable-querycolumns.md) lors de l’indicateur TBL_ALL_COLUMNS est défini.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="8d2bd-135">Le membre **ulOrder** indique à la fois ordre direction et informations de catégorisation, par exemple, par conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), c'est-à-dire conversationnel thread, ce qui est une série de messages et des réponses.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="8d2bd-136">Lignes peuvent être triés dans un croissant ou décroissant séquence avec toutes les entrées NULL placées en dernier.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="8d2bd-137">La valeur TABLE_SORT_COMBINE indique que la colonne spécifiée dans **ulPropTag** doit être combinée avec la colonne catégorie précédente afin de former une catégorie composite.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="8d2bd-138">Autrement dit, au lieu de classement des valeurs uniques de colonnes individuelles, TABLE_SORT_COMBINE permet la catégorisation des valeurs uniques d’une combinaison de colonnes.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="8d2bd-139">Par exemple, une seule catégorie peut être définie pour regrouper les messages provenant d’un expéditeur particulier sur un sujet particulier.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="8d2bd-140">La valeur TABLE_SORT_COMBINE réduit le nombre de lignes de catégorie qui sont affichés.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="8d2bd-141">Tri des colonnes à valeurs multiples n’est pas universel pris en charge par toutes les implémentations de tableau.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="8d2bd-142">Si prise en charge, appliquer la MV_FLAG à l’aide de la macro MVI_PROP à la balise de propriété dans le membre **ulPropTag** pour identifier la clé de tri dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="8d2bd-143">Tri sur une colonne à valeurs multiples est basé sur l’utilisation des valeurs.</span><span class="sxs-lookup"><span data-stu-id="8d2bd-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8d2bd-144">Les valeurs de membre **ulOrder** TABLE_SORT_CATEG_MAX et TABLE_SORT_CATEG_MIN ne peuvent pas être définis dans le fichier d’en-tête téléchargeable est actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="8d2bd-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="8d2bd-145">Pour plus d’informations sur le tri standard et par catégorie, voir [tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="8d2bd-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d2bd-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d2bd-146">See also</span></span>

- [<span data-ttu-id="8d2bd-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="8d2bd-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="8d2bd-148">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8d2bd-148">MAPI Structures</span></span>](mapi-structures.md)

