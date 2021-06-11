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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406086"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="86aa7-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="86aa7-103">SPropertyRestriction</span></span>

<span data-ttu-id="86aa7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86aa7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86aa7-105">Décrit une restriction de propriété utilisée pour faire correspondre une constante à la valeur d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="86aa7-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86aa7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="86aa7-106">Header file:</span></span>  <br/> |<span data-ttu-id="86aa7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86aa7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="86aa7-108">Members</span><span class="sxs-lookup"><span data-stu-id="86aa7-108">Members</span></span>

<span data-ttu-id="86aa7-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="86aa7-109">**relop**</span></span>
  
> <span data-ttu-id="86aa7-110">Opérateur relationnel qui sera utilisé dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="86aa7-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="86aa7-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="86aa7-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="86aa7-112">RELOP_GE : la comparaison est réalisée en fonction d’une première valeur supérieure ou égale.</span><span class="sxs-lookup"><span data-stu-id="86aa7-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="86aa7-113">RELOP_GT : la comparaison est réalisée en fonction d’une première valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="86aa7-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="86aa7-114">RELOP_LE : la comparaison est réalisée en fonction d’une première valeur inférieure ou égale.</span><span class="sxs-lookup"><span data-stu-id="86aa7-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="86aa7-115">RELOP_LT : la comparaison est réalisée en fonction d’une première valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="86aa7-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="86aa7-116">RELOP_NE : la comparaison est réalisée en fonction de valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="86aa7-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="86aa7-117">RELOP_RE : la comparaison est réalisée en fonction des valeurs LIKE (expression régulière).</span><span class="sxs-lookup"><span data-stu-id="86aa7-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="86aa7-118">RELOP_EQ : la comparaison est réalisée sur la base de valeurs égales.</span><span class="sxs-lookup"><span data-stu-id="86aa7-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="86aa7-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="86aa7-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="86aa7-120">Balise de propriété identifiant la propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="86aa7-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="86aa7-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="86aa7-121">**lpProp**</span></span>
  
> <span data-ttu-id="86aa7-122">Pointeur vers une structure [SPropValue](spropvalue.md) qui contient la valeur constante qui sera utilisée dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="86aa7-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86aa7-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="86aa7-123">Remarks</span></span>

<span data-ttu-id="86aa7-124">Il existe deux balises de propriété dans une structure **SPropertyRestriction.**</span><span class="sxs-lookup"><span data-stu-id="86aa7-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="86aa7-125">L’un se trouve dans le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** pointée par **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="86aa7-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="86aa7-126">MAPI requiert à la fois le champ d’identificateur de propriété et le champ de type de propriété.</span><span class="sxs-lookup"><span data-stu-id="86aa7-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="86aa7-127">**UlPropTag** dans **SPropertyRestriction** est la propriété à mettre en correspondance, et le pointeur **lpProp** du **SPropertyRestriction** vers le type **ulPropTag**'s de **la valeur SPropValue** indique comment la valeur des membres de **l’union lpProp est** interprétée.</span><span class="sxs-lookup"><span data-stu-id="86aa7-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="86aa7-128">Les deux types de propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="86aa7-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="86aa7-129">L’ordre de comparaison _est (valeur de propriété) (opérateur relationnel) (valeur constante)._</span><span class="sxs-lookup"><span data-stu-id="86aa7-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="86aa7-130">Lorsqu’une restriction de propriété est transmise à **IMAPITable::Restrict** ou **IMAPITable::FindRow** et que la propriété cible n’existe pas, les résultats de la restriction ne sont pas indéfinis.</span><span class="sxs-lookup"><span data-stu-id="86aa7-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="86aa7-131">En créant une restriction **AND** qui joint la restriction de propriété à une restriction **EXIST,** un appelant peut obtenir des résultats précis.</span><span class="sxs-lookup"><span data-stu-id="86aa7-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="86aa7-132">Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction **EXIST** et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **AND.**</span><span class="sxs-lookup"><span data-stu-id="86aa7-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="86aa7-133">Les balises de propriétés à valeurs multiples peuvent être utilisées dans les restrictions de propriété si le fournisseur de services qui implémente la table les prend en charge.</span><span class="sxs-lookup"><span data-stu-id="86aa7-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="86aa7-134">Si elle est prise en charge, des balises de propriétés à valeurs multiples peuvent être utilisées partout où les balises de propriété à valeur unique peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="86aa7-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="86aa7-135">Les balises de propriétés à valeurs multiples peuvent être utilisées dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="86aa7-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="86aa7-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="86aa7-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="86aa7-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="86aa7-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="86aa7-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="86aa7-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="86aa7-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="86aa7-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="86aa7-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="86aa7-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="86aa7-141">Un cas notable lorsque les deux balises de propriété ne correspondent pas est si restreindre sur une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="86aa7-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="86aa7-142">Dans ce cas, les valeurs suivantes doivent être vraies.</span><span class="sxs-lookup"><span data-stu-id="86aa7-142">In this case the following must be true.</span></span> <span data-ttu-id="86aa7-143">> Si le type de propriété du **ulPropTag** de **SPropertyRestriction** contient le MV_FLAG (0x1000) d’indicateur de type propriété à valeurs multiples, le type de propriété du **ulPropTag** de **SPropValue** doit correspondre à l’ancien signe moins l’indicateur de bits MV_FLAG, c’est-à-dire son inverse.</span><span class="sxs-lookup"><span data-stu-id="86aa7-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="86aa7-144">> Par exemple, pour restreindre l’utilisation d’une propriété de chaîne personnalisée à valeurs multiples telle qu’une catégorie avec une balise de propriété pour la 0x8012101f de propriété, autrement dit, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), la valeur **SPropertyRestriction** correspondante apparaît comme suit.</span><span class="sxs-lookup"><span data-stu-id="86aa7-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="86aa7-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> notez que si le type de propriété **du ulPropTag** de **SPropValue** contient l’indicateur de bits MV_FLAG, le retour probable est MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="86aa7-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="86aa7-146">Pour plus d’informations sur la structure **SPropertyRestriction,** voir [À propos des restrictions.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="86aa7-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86aa7-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86aa7-147">See also</span></span>

- [<span data-ttu-id="86aa7-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="86aa7-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="86aa7-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="86aa7-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="86aa7-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="86aa7-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="86aa7-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="86aa7-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="86aa7-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="86aa7-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="86aa7-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="86aa7-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="86aa7-154">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="86aa7-154">MAPI Structures</span></span>](mapi-structures.md)

