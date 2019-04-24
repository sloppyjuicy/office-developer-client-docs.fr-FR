---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351288"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="c0e0d-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="c0e0d-103">SComparePropsRestriction</span></span>

<span data-ttu-id="c0e0d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0e0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0e0d-105">Décrit une restriction de propriété compare, qui teste deux propriétés à l'aide d'un opérateur relationnel.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0e0d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c0e0d-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0e0d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c0e0d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="c0e0d-108">Members</span><span class="sxs-lookup"><span data-stu-id="c0e0d-108">Members</span></span>

<span data-ttu-id="c0e0d-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="c0e0d-109">**relop**</span></span>
  
> <span data-ttu-id="c0e0d-110">Opérateur relationnel à utiliser pour comparer les deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="c0e0d-111">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="c0e0d-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="c0e0d-112">RELOP_GE: la comparaison est effectuée en fonction d'une première valeur supérieure ou égale.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="c0e0d-113">RELOP_GT: la comparaison est effectuée en fonction d'une valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="c0e0d-114">RELOP_LE: la comparaison est effectuée en fonction d'une valeur inférieure ou égale à la première valeur.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="c0e0d-115">RELOP_LT: la comparaison est effectuée en fonction d'une valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="c0e0d-116">RELOP_NE: la comparaison est effectuée en fonction de valeurs inégales.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="c0e0d-117">RELOP_RE: la comparaison est effectuée en fonction des valeurs LIKE (expression régulière).</span><span class="sxs-lookup"><span data-stu-id="c0e0d-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="c0e0d-118">RELOP_EQ: la comparaison est effectuée en fonction de valeurs égales.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="c0e0d-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="c0e0d-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="c0e0d-120">Balise de propriété de la première propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="c0e0d-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="c0e0d-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="c0e0d-122">Balise de propriété de la deuxième propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0e0d-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0e0d-123">Remarks</span></span>

<span data-ttu-id="c0e0d-124">L'ordre de comparaison est _(balise de propriété 1) (opérateur relationnel) (balise de propriété 2)_.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="c0e0d-125">Les propriétés à comparer doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="c0e0d-126">Si vous tentez de comparer des propriétés de types différents, MAPI ou le fournisseur de services renvoie la valeur d'erreur MAPI_E_TOO_COMPLEX à partir de la méthode [IMAPITable](imapitableiunknown.md) que la structure est transmise en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="c0e0d-127">Le résultat d'une restriction de valeur de la propriété compare n'est pas défini lorsque l'une ou les deux propriétés n'existent pas.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="c0e0d-128">Lorsqu'un client a besoin d'un comportement bien défini pour une restriction de ce type et qu'il n'est pas certain que la propriété existe, (par exemple, il ne s'agit pas d'une colonne obligatoire d'un tableau), il doit créer une restriction **et** rejoigne la restriction de propriété compare existante. restreindre.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="c0e0d-129">Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction exist et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** .</span><span class="sxs-lookup"><span data-stu-id="c0e0d-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="c0e0d-130">Les propriétés spécifiées dans les membres **ulPropTag1** et **ulPropTag2** peuvent être à valeurs multiples si le fournisseur de services le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="c0e0d-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="c0e0d-131">Pour plus d'informations sur la structure **SComparePropsRestriction** et les restrictions en général, consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c0e0d-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0e0d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0e0d-132">See also</span></span>

- [<span data-ttu-id="c0e0d-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="c0e0d-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="c0e0d-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c0e0d-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="c0e0d-135">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c0e0d-135">MAPI Structures</span></span>](mapi-structures.md)

