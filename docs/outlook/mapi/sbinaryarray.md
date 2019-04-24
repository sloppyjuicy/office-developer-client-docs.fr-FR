---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351057"
---
# <a name="sbinaryarray"></a><span data-ttu-id="59f5f-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="59f5f-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="59f5f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59f5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59f5f-105">Contient un tableau de valeurs binaires.</span><span class="sxs-lookup"><span data-stu-id="59f5f-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59f5f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="59f5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="59f5f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="59f5f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="59f5f-108">Members</span><span class="sxs-lookup"><span data-stu-id="59f5f-108">Members</span></span>

 <span data-ttu-id="59f5f-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="59f5f-109">**cValues**</span></span>
  
> <span data-ttu-id="59f5f-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="59f5f-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="59f5f-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="59f5f-111">**lpbin**</span></span>
  
> <span data-ttu-id="59f5f-112">Pointeur vers un tableau de structures [SBinary](sbinary.md) qui contient les valeurs binaires.</span><span class="sxs-lookup"><span data-stu-id="59f5f-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="59f5f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="59f5f-113">Remarks</span></span>

<span data-ttu-id="59f5f-114">La structure **SBinaryArray** est utilisée pour décrire les propriétés de type PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="59f5f-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="59f5f-115">Pour plus d'informations sur PT_MV_BINARY, consultez la rubrique [liste des types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="59f5f-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59f5f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59f5f-116">See also</span></span>



[<span data-ttu-id="59f5f-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="59f5f-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="59f5f-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="59f5f-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="59f5f-119">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="59f5f-119">MAPI Structures</span></span>](mapi-structures.md)

