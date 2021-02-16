---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423663"
---
# <a name="scontentrestriction"></a><span data-ttu-id="b0bf1-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="b0bf1-103">SContentRestriction</span></span>
 
<span data-ttu-id="b0bf1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0bf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0bf1-105">Décrit une restriction de contenu, qui est utilisée pour limiter un affichage tableau aux seules lignes qui incluent une colonne dont le contenu correspond à une chaîne de recherche.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0bf1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b0bf1-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0bf1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0bf1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="b0bf1-108">Members</span><span class="sxs-lookup"><span data-stu-id="b0bf1-108">Members</span></span>

<span data-ttu-id="b0bf1-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="b0bf1-110">Paramètres d’option définissant le niveau de précision que la restriction de contenu doit appliquer lorsque vous vérifiez la correspondance.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="b0bf1-111">Les **16 bits inférieurs** du membre **ulFuzzyLevel** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8 et doivent être définies sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0bf1-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="b0bf1-112">FL_FULLSTRING : pour correspondre, la chaîne de **recherche lpProp** doit être contenue dans la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="b0bf1-113">FL_PREFIX : pour correspondre, la chaîne de **recherche lpProp** doit apparaître au début de la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="b0bf1-114">Les deux chaînes doivent être comparées uniquement jusqu’à la longueur de la chaîne de recherche indiquée par **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="b0bf1-115">FL_SUBSTRING : pour correspondre, la chaîne de **recherche lpProp** doit être contenue n’importe où dans la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="b0bf1-116">Les **16 bits supérieurs** du membre **ulFuzzyLevel** s’appliquent uniquement aux propriétés de type PT_STRING8 et peuvent être définies sur les valeurs suivantes dans n’importe quelle combinaison :</span><span class="sxs-lookup"><span data-stu-id="b0bf1-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="b0bf1-117">FL_IGNORECASE : la comparaison doit être réalisée sans prendre en compte la cause.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="b0bf1-118">FL_IGNORENONSPACE : la comparaison doit ignorer les caractères non définis par Unicode, tels que les signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="b0bf1-119">FL_LOOSE : la comparaison doit vous donner une correspondance autant que possible, en ignorant les caractères de cas et sans espacement.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="b0bf1-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="b0bf1-121">Balise de propriété identifiant la propriété de chaîne à vérifier pour l’occurrence de la chaîne de recherche.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="b0bf1-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-122">**lpProp**</span></span>
  
> <span data-ttu-id="b0bf1-123">Pointeur vers une structure de valeurs de propriété qui contient la valeur de chaîne à utiliser comme chaîne de recherche.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0bf1-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0bf1-124">Remarks</span></span>

<span data-ttu-id="b0bf1-125">Il existe deux balises de propriété dans une structure **SContentRestriction** : l’une dans le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** pointée par **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="b0bf1-126">Dans les deux balises, MAPI requiert uniquement le champ de type de propriété et ignore le champ d’identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="b0bf1-127">Toutefois, les deux types de propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="b0bf1-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="b0bf1-128">Les valeurs FL_FULLSTRING, FL_PREFIX et FL_SUBSTRING s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="b0bf1-129">Un seul d’entre eux peut être définie, et l’un d’eux doit être définie.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="b0bf1-130">Leurs significations sont corrigées et le fournisseur doit les implémenter exactement comme défini.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="b0bf1-131">Le fournisseur doit renvoyer MAPI_E_TOO_COMPLEX s’il ne parvient pas à prendre en charge ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="b0bf1-132">Les valeurs FL_IGNORECASE, FL_IGNORENONSPACE et FL_LOOSE sont indépendantes.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="b0bf1-133">N’importe où entre zéro et les trois peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="b0bf1-134">Leurs définitions sont fournies à titre indicatif uniquement et le fournisseur est libre d’implémenter sa propre signification spécifique de chaque indicateur.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="b0bf1-135">Le fournisseur ne doit pas renvoyer d’indication d’erreur s’il n’a pas d’implémentation d’un indicateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="b0bf1-136">Le résultat d’une restriction de contenu imposée à une propriété n’est pas définie lorsque la propriété n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="b0bf1-137">Lorsqu’un client requiert un comportement bien défini pour une telle restriction et qu’il n’est pas sûr que la propriété existe, par exemple, il ne s’agit pas d’une colonne obligatoire d’une table qu’il doit créer une restriction **AND** pour joindre la restriction de contenu avec une restriction existante.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="b0bf1-138">Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction existante et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **AND.**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="b0bf1-139">Pour plus d’informations sur la structure et les restrictions **SContentRestriction** en général, voir [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b0bf1-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0bf1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0bf1-140">See also</span></span>

- [<span data-ttu-id="b0bf1-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b0bf1-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="b0bf1-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b0bf1-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="b0bf1-143">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b0bf1-143">MAPI Structures</span></span>](mapi-structures.md)

