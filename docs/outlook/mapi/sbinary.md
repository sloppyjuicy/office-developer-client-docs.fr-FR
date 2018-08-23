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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f54ef96443e5c9fc5fb587f5a9c25388c1ff9cdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577421"
---
# <a name="sbinary"></a><span data-ttu-id="c5c1f-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="c5c1f-103">SBinary</span></span>

  
  
<span data-ttu-id="c5c1f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5c1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5c1f-105">Décrit une propriété de type PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="c5c1f-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5c1f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c5c1f-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5c1f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5c1f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="c5c1f-108">Members</span><span class="sxs-lookup"><span data-stu-id="c5c1f-108">Members</span></span>

 <span data-ttu-id="c5c1f-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="c5c1f-109">**cb**</span></span>
  
> <span data-ttu-id="c5c1f-110">Nombre d’octets dans le membre **lpb** .</span><span class="sxs-lookup"><span data-stu-id="c5c1f-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="c5c1f-111">**LPB**</span><span class="sxs-lookup"><span data-stu-id="c5c1f-111">**lpb**</span></span>
  
> <span data-ttu-id="c5c1f-112">Pointeur vers la valeur de la propriété PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="c5c1f-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5c1f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5c1f-113">Remarks</span></span>

<span data-ttu-id="c5c1f-114">Pour plus d’informations sur les types de propriété, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c5c1f-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5c1f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5c1f-115">See also</span></span>



[<span data-ttu-id="c5c1f-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c5c1f-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c5c1f-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c5c1f-117">MAPI Structures</span></span>](mapi-structures.md)

