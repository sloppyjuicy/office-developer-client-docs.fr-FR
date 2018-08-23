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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e8d85ba55c5aa2f3780ad8e04cf1326cd7c35865
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575937"
---
# <a name="ssortorderset"></a><span data-ttu-id="ccb72-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ccb72-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="ccb72-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccb72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccb72-105">Définit une collection de clés de tri pour une table qui est utilisé pour le tri standard ou par catégorie.</span><span class="sxs-lookup"><span data-stu-id="ccb72-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ccb72-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ccb72-106">Header file:</span></span>  <br/> |<span data-ttu-id="ccb72-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ccb72-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ccb72-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="ccb72-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ccb72-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="ccb72-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="ccb72-110">Members</span><span class="sxs-lookup"><span data-stu-id="ccb72-110">Members</span></span>

 <span data-ttu-id="ccb72-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="ccb72-111">**cSorts**</span></span>
  
> <span data-ttu-id="ccb72-112">Nombre de structures [SSortOrder](ssortorder.md) qui sont inclus dans le membre **aSort** .</span><span class="sxs-lookup"><span data-stu-id="ccb72-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="ccb72-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="ccb72-113">**cCategories**</span></span>
  
> <span data-ttu-id="ccb72-114">Nombre de colonnes qui sont désignés en tant que colonnes de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ccb72-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="ccb72-115">Plage de valeurs possibles à partir de zéro, ce qui indique un tri standard ou non classés, au numéro indiqué par le membre **cSorts** .</span><span class="sxs-lookup"><span data-stu-id="ccb72-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="ccb72-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="ccb72-116">**cExpanded**</span></span>
  
> <span data-ttu-id="ccb72-117">Nombre de catégories qui démarre dans un état développé, où toutes les lignes qui s’appliquent à la catégorie sont visibles dans l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="ccb72-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="ccb72-118">Valeurs possibles sont comprises entre 0 et le nombre indiqué par **cCategories**.</span><span class="sxs-lookup"><span data-stu-id="ccb72-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="ccb72-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="ccb72-119">**aSort**</span></span>
  
> <span data-ttu-id="ccb72-120">Tableau de structures **SSortOrder** , chaque définition d’un ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="ccb72-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ccb72-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="ccb72-121">Remarks</span></span>

<span data-ttu-id="ccb72-122">Une structure **SSortOrderSet** est utilisée pour définir plusieurs ordres de tri pour le tri standard et par catégorie.</span><span class="sxs-lookup"><span data-stu-id="ccb72-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="ccb72-123">Chaque structure **SSortOrderSet** contient au moins une structure **SSortOrder** définit la direction de l’ordre de tri et de la colonne qui sera utilisée comme clé de tri.</span><span class="sxs-lookup"><span data-stu-id="ccb72-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="ccb72-124">Pour le tri par catégorie, cette colonne est utilisée en tant que la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ccb72-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="ccb72-125">Lorsque la valeur du membre **cSorts** dépasse la valeur du membre **cCategories** , il existe plusieurs clés de tri que les catégories et les catégories sont créées à partir des colonnes qui s’affichent en premier dans le tableau **SSortOrder** .</span><span class="sxs-lookup"><span data-stu-id="ccb72-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="ccb72-126">Par exemple, si **cSorts** est défini à 3 et **cCategories** est défini sur 2, les colonnes décrites par le membre **ulPropTag** les deux premières entrées dans le tableau **SSortOrder** sont utilisées comme colonnes de catégorie.</span><span class="sxs-lookup"><span data-stu-id="ccb72-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="ccb72-127">La première entrée sert de la catégorie de niveau supérieur de regroupement ; la deuxième entrée en tant que le groupe secondaire.</span><span class="sxs-lookup"><span data-stu-id="ccb72-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="ccb72-128">Toutes les lignes qui correspondent aux colonnes deux catégories sont triés à l’aide de la clé de tri définie dans la troisième entrée.</span><span class="sxs-lookup"><span data-stu-id="ccb72-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="ccb72-129">Le membre **cExpanded** Spécifie le nombre de catégories qui sont développés dans un premier temps.</span><span class="sxs-lookup"><span data-stu-id="ccb72-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="ccb72-130">Lorsqu’il existe plusieurs catégories, l’implémentation de la table commence par la première colonne à désigner comme une catégorie et continue dans l’ordre séquentiel avec les colonnes de catégorie suivantes jusqu'à ce que le nombre de **cCategories** a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="ccb72-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="ccb72-131">S’il n’y a plus de colonnes de catégorie que l’étendue de colonnes, les colonnes de la catégorie sont réduits.</span><span class="sxs-lookup"><span data-stu-id="ccb72-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="ccb72-132">Si **cExpanded** est égale à zéro, uniquement la ligne d’en-tête de niveau supérieur est disponible à l’utilisateur de la table pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="ccb72-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="ccb72-133">Si **cExpanded** est égale à moins que le nombre d’abscisses, toutes les lignes d’en-tête et aucune des lignes de feuille sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="ccb72-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="ccb72-134">Si **cExpanded** est égal au nombre de catégories, le tableau est développé.</span><span class="sxs-lookup"><span data-stu-id="ccb72-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="ccb72-135">Pour plus d’informations sur le tri standard et par catégorie, voir [tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="ccb72-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ccb72-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccb72-136">See also</span></span>



[<span data-ttu-id="ccb72-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="ccb72-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="ccb72-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ccb72-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="ccb72-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ccb72-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="ccb72-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="ccb72-140">MAPI Structures</span></span>](mapi-structures.md)

