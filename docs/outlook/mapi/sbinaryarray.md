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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438287"
---
# <a name="sbinaryarray"></a><span data-ttu-id="2027d-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="2027d-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="2027d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2027d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2027d-105">Contient un tableau de valeurs binaires.</span><span class="sxs-lookup"><span data-stu-id="2027d-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2027d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2027d-106">Header file:</span></span>  <br/> |<span data-ttu-id="2027d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2027d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="2027d-108">Members</span><span class="sxs-lookup"><span data-stu-id="2027d-108">Members</span></span>

 <span data-ttu-id="2027d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2027d-109">**cValues**</span></span>
  
> <span data-ttu-id="2027d-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="2027d-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="2027d-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="2027d-111">**lpbin**</span></span>
  
> <span data-ttu-id="2027d-112">Pointeur vers un tableau de structures [SBinary](sbinary.md) qui contient les valeurs binaires.</span><span class="sxs-lookup"><span data-stu-id="2027d-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2027d-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="2027d-113">Remarks</span></span>

<span data-ttu-id="2027d-114">La structure **SBinaryArray** est utilisée pour décrire les propriétés de type PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="2027d-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="2027d-115">Pour plus d'informations sur PT_MV_BINARY, consultez la rubrique [liste des types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2027d-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2027d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2027d-116">See also</span></span>



[<span data-ttu-id="2027d-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="2027d-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="2027d-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2027d-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2027d-119">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="2027d-119">MAPI Structures</span></span>](mapi-structures.md)

