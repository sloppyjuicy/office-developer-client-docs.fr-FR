---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315133"
---
# <a name="currency"></a><span data-ttu-id="49154-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="49154-103">CURRENCY</span></span>

  
  
<span data-ttu-id="49154-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49154-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49154-105">Contient un entier 64 bits signé représentant une valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="49154-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49154-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="49154-106">Header file:</span></span>  <br/> |<span data-ttu-id="49154-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="49154-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="49154-108">Members</span><span class="sxs-lookup"><span data-stu-id="49154-108">Members</span></span>

 <span data-ttu-id="49154-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="49154-109">**Lo**</span></span>
  
> <span data-ttu-id="49154-110">Ordre bas 32 bits de la valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="49154-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="49154-111">**Salut**</span><span class="sxs-lookup"><span data-stu-id="49154-111">**Hi**</span></span>
  
> <span data-ttu-id="49154-112">Ordre 32 bits de poids fort de la valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="49154-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49154-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="49154-113">Remarks</span></span>

<span data-ttu-id="49154-114">La structure **monétaire** est une représentation entière à l'horizontale d'un nombre décimal à quatre chiffres à droite de la virgule.</span><span class="sxs-lookup"><span data-stu-id="49154-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="49154-115">Par exemple, une valeur stockée de 327500 doit être interprétée comme représentant une valeur monétaire de 32,7500.</span><span class="sxs-lookup"><span data-stu-id="49154-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="49154-116">La structure **Currency** est utilisée pour décrire une propriété de type PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="49154-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="49154-117">Pour plus d'informations sur les types de propriétés, voir [MAPI Property type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="49154-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49154-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49154-118">See also</span></span>



[<span data-ttu-id="49154-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="49154-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="49154-120">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="49154-120">MAPI Structures</span></span>](mapi-structures.md)

