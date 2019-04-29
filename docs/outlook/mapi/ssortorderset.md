---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438098"
---
# <a name="ssortorderset"></a><span data-ttu-id="b23aa-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b23aa-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="b23aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b23aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b23aa-105">Définit une collection de clés de tri pour un tableau utilisé pour le tri standard ou par catégorie.</span><span class="sxs-lookup"><span data-stu-id="b23aa-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b23aa-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b23aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="b23aa-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b23aa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b23aa-108">Macros connexes:</span><span class="sxs-lookup"><span data-stu-id="b23aa-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b23aa-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="b23aa-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="b23aa-110">Members</span><span class="sxs-lookup"><span data-stu-id="b23aa-110">Members</span></span>

 <span data-ttu-id="b23aa-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="b23aa-111">**cSorts**</span></span>
  
> <span data-ttu-id="b23aa-112">Nombre de structures [SSortOrder](ssortorder.md) incluses dans le membre **ASOR** .</span><span class="sxs-lookup"><span data-stu-id="b23aa-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="b23aa-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="b23aa-113">**cCategories**</span></span>
  
> <span data-ttu-id="b23aa-114">Nombre de colonnes qui sont désignées en tant que colonnes de catégorie.</span><span class="sxs-lookup"><span data-stu-id="b23aa-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="b23aa-115">Les valeurs possibles sont comprises entre zéro, qui indique un tri standard ou non catégorisé, et le nombre indiqué par le membre **cSorts** .</span><span class="sxs-lookup"><span data-stu-id="b23aa-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="b23aa-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="b23aa-116">**cExpanded**</span></span>
  
> <span data-ttu-id="b23aa-117">Nombre de catégories qui commencent dans un état développé, où toutes les lignes qui s'appliquent à la catégorie sont visibles dans l'affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="b23aa-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="b23aa-118">Les valeurs possibles sont comprises entre 0 et le nombre indiqué par **cCategories**.</span><span class="sxs-lookup"><span data-stu-id="b23aa-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="b23aa-119">**aSor**</span><span class="sxs-lookup"><span data-stu-id="b23aa-119">**aSort**</span></span>
  
> <span data-ttu-id="b23aa-120">Tableau de structures **SSortOrder** , chacune définissant un ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="b23aa-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b23aa-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="b23aa-121">Remarks</span></span>

<span data-ttu-id="b23aa-122">Une structure **SSortOrderSet** est utilisée pour définir plusieurs ordres de tri pour le tri standard et catégorisé.</span><span class="sxs-lookup"><span data-stu-id="b23aa-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="b23aa-123">Chaque structure **SSortOrderSet** contient au moins une structure **SSortOrder** définissant la direction du tri et la colonne qui sera utilisée comme clé de tri.</span><span class="sxs-lookup"><span data-stu-id="b23aa-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="b23aa-124">Pour le tri par catégorie, cette colonne est utilisée en tant que catégorie.</span><span class="sxs-lookup"><span data-stu-id="b23aa-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="b23aa-125">Lorsque la valeur du membre **cSorts** dépasse la valeur du membre **cCategories** , il y a plus de clés de tri que de Categories, et les catégories sont créées à partir des colonnes qui apparaissent en premier dans le tableau **SSortOrder** .</span><span class="sxs-lookup"><span data-stu-id="b23aa-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="b23aa-126">Par exemple, si **cSorts** est défini sur 3 et **cCategories** est défini sur 2, les colonnes décrites par le membre **ulPropTag** des deux premières entrées du tableau **SSortOrder** sont utilisées comme colonnes de catégorie.</span><span class="sxs-lookup"><span data-stu-id="b23aa-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="b23aa-127">La première entrée sert de groupement de catégories de niveau supérieur; deuxième entrée comme regroupement secondaire.</span><span class="sxs-lookup"><span data-stu-id="b23aa-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="b23aa-128">Toutes les lignes qui correspondent aux deux colonnes de catégorie sont triées à l'aide de la clé de tri définie dans la troisième entrée.</span><span class="sxs-lookup"><span data-stu-id="b23aa-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="b23aa-129">Le membre **cExpanded** spécifie le nombre de catégories qui sont développées pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="b23aa-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="b23aa-130">Lorsqu'il existe plusieurs catégories, l'implémentation de la table commence par la première colonne à être désignée en tant que catégorie et continue dans un ordre séquentiel avec les colonnes de catégorie suivantes jusqu'à ce que le nombre de **cCategories** ait été dépassé.</span><span class="sxs-lookup"><span data-stu-id="b23aa-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="b23aa-131">S'il y a plus de colonnes de catégorie qu'il n'y a de colonnes développées, les colonnes de catégorie sont réduites.</span><span class="sxs-lookup"><span data-stu-id="b23aa-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="b23aa-132">Si **cExpanded** est égal à zéro, seule la ligne d'en-tête de niveau supérieur est accessible à l'utilisateur de table pour l'affichage.</span><span class="sxs-lookup"><span data-stu-id="b23aa-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="b23aa-133">Si **cExpanded** est égal à un de moins que le nombre de catégories, toutes les lignes d'en-tête et aucune des lignes de feuille sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="b23aa-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="b23aa-134">Si **cExpanded** est égal au nombre de catégories, le tableau est entièrement développé.</span><span class="sxs-lookup"><span data-stu-id="b23aa-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="b23aa-135">Pour plus d'informations sur le tri standard et catégorisé, consultez la rubrique [Tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="b23aa-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b23aa-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b23aa-136">See also</span></span>



[<span data-ttu-id="b23aa-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="b23aa-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="b23aa-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="b23aa-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="b23aa-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="b23aa-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="b23aa-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b23aa-140">MAPI Structures</span></span>](mapi-structures.md)

