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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787086"
---
# <a name="scontentrestriction"></a><span data-ttu-id="931bb-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="931bb-103">SContentRestriction</span></span>
 
<span data-ttu-id="931bb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="931bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="931bb-105">Décrit une restriction de contenu, qui est utilisée pour limiter un affichage de tableau uniquement aux lignes qui comportent une colonne correspond à une chaîne de recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="931bb-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="931bb-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="931bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="931bb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="931bb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="931bb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="931bb-108">Members</span></span>

<span data-ttu-id="931bb-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="931bb-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="931bb-110">Options définissant le niveau de précision que permettent que la restriction de contenu doit appliquer lors de la vérification pour une correspondance.</span><span class="sxs-lookup"><span data-stu-id="931bb-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="931bb-111">Les **16 bits inférieurs** du membre **ulFuzzyLevel** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8 et doit être défini sur une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="931bb-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="931bb-112">FL_FULLSTRING : Pour faire correspondre, la chaîne de recherche **lpProp** doit être contenue dans la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="931bb-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="931bb-113">FL_PREFIX : Pour faire correspondre, la chaîne de recherche **lpProp** doit apparaître au début de la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="931bb-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="931bb-114">Les deux chaînes doivent être comparées uniquement jusqu'à la longueur de la chaîne de recherche indiquée par **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="931bb-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="931bb-115">FL_SUBSTRING : Pour faire correspondre, la chaîne de recherche **lpProp** doit figurer n’importe où dans la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="931bb-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="931bb-116">Les **derniers 16 bits** du membre **ulFuzzyLevel** s’appliquent uniquement aux propriétés de type PT_STRING8 et peut avoir les valeurs suivantes dans n’importe quelle combinaison :</span><span class="sxs-lookup"><span data-stu-id="931bb-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="931bb-117">FL_IGNORECASE : La comparaison doit être effectuée sans tenir compte des cas.</span><span class="sxs-lookup"><span data-stu-id="931bb-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="931bb-118">FL_IGNORENONSPACE : La comparaison doit ignorer les caractères de sans espace définie par l’Unicode tels que diacritiques.</span><span class="sxs-lookup"><span data-stu-id="931bb-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="931bb-119">FL_LOOSE : La comparaison doit vous fournir une correspondance la mesure du possible, en ignorant la casse et les caractères sans espace.</span><span class="sxs-lookup"><span data-stu-id="931bb-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="931bb-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="931bb-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="931bb-121">Balise de propriété qui identifie la propriété de type chaîne à vérifier pour une occurrence de la chaîne de recherche.</span><span class="sxs-lookup"><span data-stu-id="931bb-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="931bb-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="931bb-122">**lpProp**</span></span>
  
> <span data-ttu-id="931bb-123">Pointeur vers une structure de valeur de propriété qui contient la valeur de chaîne à utiliser comme la chaîne de recherche.</span><span class="sxs-lookup"><span data-stu-id="931bb-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="931bb-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="931bb-124">Remarks</span></span>

<span data-ttu-id="931bb-125">Il existe deux balises de propriété dans une structure **SContentRestriction** : 1 dans le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** désignés par **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="931bb-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="931bb-126">Dans les deux balises, MAPI nécessite uniquement le champ de type de propriété et ignore le champ d’identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="931bb-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="931bb-127">Toutefois, les types de deux propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="931bb-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="931bb-128">Les valeurs FL_FULLSTRING, FL_PREFIX et FL_SUBSTRING s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="931bb-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="931bb-129">Un seul d'entre eux peut être défini et qu’un d'entre eux doit être défini.</span><span class="sxs-lookup"><span data-stu-id="931bb-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="931bb-130">Leurs significations sont fixes, et le fournisseur doit implémenter les exactement tel que défini.</span><span class="sxs-lookup"><span data-stu-id="931bb-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="931bb-131">Le fournisseur doit retourner MAPI_E_TOO_COMPLEX si elle ne peut pas prendre en charge ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="931bb-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="931bb-132">Les valeurs FL_IGNORECASE, FL_IGNORENONSPACE et FL_LOOSE sont indépendants.</span><span class="sxs-lookup"><span data-stu-id="931bb-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="931bb-133">N’importe où à partir de zéro à trois d'entre eux peut être définie.</span><span class="sxs-lookup"><span data-stu-id="931bb-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="931bb-134">Leurs définitions sont fournies à titre indicatif uniquement, et le fournisseur est libre de mettre en œuvre son propre signification spécifique de chaque indicateur.</span><span class="sxs-lookup"><span data-stu-id="931bb-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="931bb-135">Le fournisseur ne doit pas renvoyer toute indication de l’erreur si elle a pas d’implémentation d’un indicateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="931bb-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="931bb-136">Le résultat d’une restriction de contenu imposée par rapport à une propriété est non défini lorsque la propriété n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="931bb-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="931bb-137">Lorsqu’un client requiert un comportement bien défini pour une telle restriction et n’est pas certain que si la propriété existe par exemple, il n’est pas une colonne d’une table requise, il doit créer une restriction **et** pour participer à la restriction de contenu avec une restriction existent.</span><span class="sxs-lookup"><span data-stu-id="931bb-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="931bb-138">Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction existent et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** .</span><span class="sxs-lookup"><span data-stu-id="931bb-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="931bb-139">Pour plus d’informations sur les restrictions de structure **SContentRestriction** en général, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="931bb-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="931bb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="931bb-140">See also</span></span>

- [<span data-ttu-id="931bb-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="931bb-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="931bb-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="931bb-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="931bb-143">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="931bb-143">MAPI Structures</span></span>](mapi-structures.md)

