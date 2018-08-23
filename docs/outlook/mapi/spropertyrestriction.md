---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7d588380ccc84f51fe58bb0f092d5287b12b4270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586535"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="c24ac-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c24ac-103">SPropertyRestriction</span></span>

<span data-ttu-id="c24ac-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c24ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c24ac-105">Décrit une restriction de propriété qui est utilisée pour la correspondance d’une constante avec la valeur d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="c24ac-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c24ac-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c24ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="c24ac-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c24ac-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="c24ac-108">Members</span><span class="sxs-lookup"><span data-stu-id="c24ac-108">Members</span></span>

<span data-ttu-id="c24ac-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="c24ac-109">**relop**</span></span>
  
> <span data-ttu-id="c24ac-110">Opérateur relationnel qui sera utilisé dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="c24ac-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="c24ac-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c24ac-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="c24ac-112">RELOP_GE : La comparaison est effectuée en fonction d’une première valeur supérieure ou égale.</span><span class="sxs-lookup"><span data-stu-id="c24ac-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="c24ac-113">RELOP_GT : La comparaison est effectuée en fonction d’une première valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="c24ac-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="c24ac-114">RELOP_LE : La comparaison est effectuée en fonction d’une première valeur inférieur ou égale.</span><span class="sxs-lookup"><span data-stu-id="c24ac-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="c24ac-115">RELOP_LT : La comparaison est effectuée en fonction d’une première valeur plus faible.</span><span class="sxs-lookup"><span data-stu-id="c24ac-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="c24ac-116">RELOP_NE : La comparaison est effectuée en fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="c24ac-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="c24ac-117">RELOP_RE : La comparaison est effectuée en fonction de comme valeurs (expression régulière).</span><span class="sxs-lookup"><span data-stu-id="c24ac-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="c24ac-118">RELOP_EQ : La comparaison est effectuée en fonction de des valeurs égales.</span><span class="sxs-lookup"><span data-stu-id="c24ac-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="c24ac-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c24ac-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="c24ac-120">Balise de propriété qui identifie la propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="c24ac-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="c24ac-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="c24ac-121">**lpProp**</span></span>
  
> <span data-ttu-id="c24ac-122">Pointeur vers une structure [SPropValue](spropvalue.md) qui contient la valeur de constante qui sera utilisée lors de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="c24ac-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c24ac-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="c24ac-123">Remarks</span></span>

<span data-ttu-id="c24ac-124">Il existe deux balises de propriété dans une structure **SPropertyRestriction** .</span><span class="sxs-lookup"><span data-stu-id="c24ac-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="c24ac-125">Est le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** désigné par **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="c24ac-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="c24ac-126">MAPI nécessite le champ d’identificateur de propriété et le champ de type de propriété.</span><span class="sxs-lookup"><span data-stu-id="c24ac-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="c24ac-127">**ulPropTag** dans **SPropertyRestriction** est la propriété à mettre en correspondance, et le pointeur **lpProp** de l' **SPropertyRestriction** au type de **ulPropTag**d' de la **SPropValue** indique comment la valeur de membres de la union **lpProp** sont interprétées.</span><span class="sxs-lookup"><span data-stu-id="c24ac-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="c24ac-128">Les types de deux propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="c24ac-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="c24ac-129">L’ordre de comparaison est _(valeur de la propriété) (opérateur relationnel) (constante)_.</span><span class="sxs-lookup"><span data-stu-id="c24ac-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="c24ac-130">Lorsqu’une restriction de propriété est transmise à **IMAPITable** ou **IMAPITable::FindRow** et la propriété cible n’existe pas, les résultats de la restriction ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="c24ac-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="c24ac-131">En créant une restriction **et** qui rejoint la restriction de propriété avec une restriction **existe** , l’appelant peut être garanti des résultats précis.</span><span class="sxs-lookup"><span data-stu-id="c24ac-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="c24ac-132">Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction **existent** et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** .</span><span class="sxs-lookup"><span data-stu-id="c24ac-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="c24ac-133">Balises de propriété à valeurs multiples peuvent être utilisées dans les restrictions de propriété si le fournisseur de services l’implémentation de la table les prend en charge.</span><span class="sxs-lookup"><span data-stu-id="c24ac-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="c24ac-134">Si prise en charge, propriété à valeurs multiples balises peut être utilisées n’importe où les balises de propriété à valeur unique peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="c24ac-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="c24ac-135">Balises de propriété à valeurs multiples peuvent être utilisées dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c24ac-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="c24ac-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="c24ac-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="c24ac-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c24ac-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="c24ac-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c24ac-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="c24ac-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="c24ac-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="c24ac-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="c24ac-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="c24ac-141">Un cas notable lorsque les balises de deux propriété ne correspondront pas se restriction sur une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="c24ac-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="c24ac-142">Dans ce cas, les informations suivantes doivent être vérifiées.</span><span class="sxs-lookup"><span data-stu-id="c24ac-142">In this case the following must be true.</span></span> <span data-ttu-id="c24ac-143">> Si le type de propriété de **ulPropTag** de **SPropertyRestriction** contient le type de propriété à valeurs multiples bit indicateur MV_FLAG (0 x 1000), le type de propriété de **ulPropTag** de **SPropValue** doit correspondre à l’ancienne moins le MV_ INDICATEUR bit indicateur, autrement dit, son inverse.</span><span class="sxs-lookup"><span data-stu-id="c24ac-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="c24ac-144">> Par exemple, pour limiter à l’aide d’une propriété de type chaîne à valeurs multiples comme une catégorie avec une balise de propriété pour la propriété 0x8012101f, c'est-à-dire PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), le correspondant **SPropertyRestriction** apparaît sous la forme suit.</span><span class="sxs-lookup"><span data-stu-id="c24ac-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="c24ac-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Notez que si le type de propriété de **ulPropTag** de **SPropValue** contient l’indicateur de bit MV_FLAG, le retour est MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="c24ac-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="c24ac-146">Pour plus d’informations sur la structure **SPropertyRestriction** , voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c24ac-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c24ac-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c24ac-147">See also</span></span>

- [<span data-ttu-id="c24ac-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="c24ac-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="c24ac-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="c24ac-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="c24ac-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c24ac-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="c24ac-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c24ac-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="c24ac-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="c24ac-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="c24ac-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="c24ac-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="c24ac-154">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c24ac-154">MAPI Structures</span></span>](mapi-structures.md)

