---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357518"
---
# <a name="sbinary"></a><span data-ttu-id="d5130-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="d5130-103">SBinary</span></span>

  
  
<span data-ttu-id="d5130-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5130-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5130-105">Décrit une propriété de type PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="d5130-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5130-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d5130-106">Header file:</span></span>  <br/> |<span data-ttu-id="d5130-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d5130-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="d5130-108">Members</span><span class="sxs-lookup"><span data-stu-id="d5130-108">Members</span></span>

 <span data-ttu-id="d5130-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="d5130-109">**cb**</span></span>
  
> <span data-ttu-id="d5130-110">Nombre d'octets dans le membre **LPB** .</span><span class="sxs-lookup"><span data-stu-id="d5130-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="d5130-111">**LPB**</span><span class="sxs-lookup"><span data-stu-id="d5130-111">**lpb**</span></span>
  
> <span data-ttu-id="d5130-112">Pointeur vers la valeur de la propriété PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="d5130-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5130-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5130-113">Remarks</span></span>

<span data-ttu-id="d5130-114">Pour plus d'informations sur les types de propriétés, voir [MAPI Property type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5130-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5130-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5130-115">See also</span></span>



[<span data-ttu-id="d5130-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d5130-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d5130-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="d5130-117">MAPI Structures</span></span>](mapi-structures.md)

