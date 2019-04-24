---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361165"
---
# <a name="slongarray"></a><span data-ttu-id="44716-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="44716-103">SLongArray</span></span>

  
  
<span data-ttu-id="44716-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44716-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44716-105">Contient un tableau de types de valeurs longues qui sont utilisés pour décrire une propriété de type PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="44716-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44716-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="44716-106">Header file:</span></span>  <br/> |<span data-ttu-id="44716-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="44716-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="44716-108">Members</span><span class="sxs-lookup"><span data-stu-id="44716-108">Members</span></span>

 <span data-ttu-id="44716-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="44716-109">**cValues**</span></span>
  
> <span data-ttu-id="44716-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **LPL** .</span><span class="sxs-lookup"><span data-stu-id="44716-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="44716-111">**LPL**</span><span class="sxs-lookup"><span data-stu-id="44716-111">**lpl**</span></span>
  
> <span data-ttu-id="44716-112">Pointeur vers un tableau de valeurs de type LONG.</span><span class="sxs-lookup"><span data-stu-id="44716-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44716-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="44716-113">Remarks</span></span>

<span data-ttu-id="44716-114">Pour plus d'informations sur PT_MV_LONG, consultez la rubrique [liste des types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="44716-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44716-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44716-115">See also</span></span>



[<span data-ttu-id="44716-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="44716-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="44716-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="44716-117">MAPI Structures</span></span>](mapi-structures.md)

