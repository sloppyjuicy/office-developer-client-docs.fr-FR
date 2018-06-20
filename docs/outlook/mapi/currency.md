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
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783122"
---
# <a name="currency"></a><span data-ttu-id="b4722-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b4722-103">CURRENCY</span></span>

  
  
<span data-ttu-id="b4722-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4722-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4722-105">Contient un entier signé de 64 bits représentant une valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="b4722-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4722-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b4722-106">Header file:</span></span>  <br/> |<span data-ttu-id="b4722-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4722-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="b4722-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b4722-108">Members</span></span>

 <span data-ttu-id="b4722-109">**LO**</span><span class="sxs-lookup"><span data-stu-id="b4722-109">**Lo**</span></span>
  
> <span data-ttu-id="b4722-110">Poids faible 32 bits de la valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="b4722-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="b4722-111">**Salut**</span><span class="sxs-lookup"><span data-stu-id="b4722-111">**Hi**</span></span>
  
> <span data-ttu-id="b4722-112">Ordre haut 32 bits de la valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="b4722-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4722-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4722-113">Remarks</span></span>

<span data-ttu-id="b4722-114">La structure de **devise** est une représentation sous forme d’entier à l’échelle d’un nombre décimal avec quatre chiffres à droite du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="b4722-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="b4722-115">Par exemple, une valeur stockée de 327500 doit être interprété comme représentant une valeur de devise de 32.7500.</span><span class="sxs-lookup"><span data-stu-id="b4722-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="b4722-116">La structure de la **devise** est utilisée pour décrire une propriété de type PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="b4722-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="b4722-117">Pour plus d’informations sur les types de propriété, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b4722-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4722-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4722-118">See also</span></span>



[<span data-ttu-id="b4722-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b4722-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b4722-120">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b4722-120">MAPI Structures</span></span>](mapi-structures.md)

