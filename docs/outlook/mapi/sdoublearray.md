---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339730"
---
# <a name="sdoublearray"></a><span data-ttu-id="11c4e-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="11c4e-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="11c4e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11c4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11c4e-105">Contient un tableau de doubles utilisés pour décrire une propriété de type PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="11c4e-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11c4e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="11c4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="11c4e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="11c4e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="11c4e-108">Members</span><span class="sxs-lookup"><span data-stu-id="11c4e-108">Members</span></span>

 <span data-ttu-id="11c4e-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="11c4e-109">**cValues**</span></span>
  
> <span data-ttu-id="11c4e-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="11c4e-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="11c4e-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="11c4e-111">**lpdbl**</span></span>
  
> <span data-ttu-id="11c4e-112">Pointeur vers un tableau de valeurs de type double.</span><span class="sxs-lookup"><span data-stu-id="11c4e-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11c4e-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="11c4e-113">Remarks</span></span>

<span data-ttu-id="11c4e-114">Pour plus d'informations sur PT_MV_DOUBLE, consultez la rubrique [liste des types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="11c4e-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11c4e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11c4e-115">See also</span></span>



[<span data-ttu-id="11c4e-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="11c4e-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="11c4e-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="11c4e-117">MAPI Structures</span></span>](mapi-structures.md)

