---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8c7ce2805248bf91ce7da071c67ece28a5b8ca07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564282"
---
# <a name="srealarray"></a><span data-ttu-id="03951-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="03951-103">SRealArray</span></span>

  
  
<span data-ttu-id="03951-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03951-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03951-105">Contient un tableau de valeurs float qui sont utilisées pour décrire une propriété de type PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="03951-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03951-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="03951-106">Header file:</span></span>  <br/> |<span data-ttu-id="03951-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03951-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="03951-108">Members</span><span class="sxs-lookup"><span data-stu-id="03951-108">Members</span></span>

 <span data-ttu-id="03951-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="03951-109">**cValues**</span></span>
  
> <span data-ttu-id="03951-110">Nombre de valeurs dans le tableau indiqué par le membre **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="03951-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="03951-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="03951-111">**lpflt**</span></span>
  
> <span data-ttu-id="03951-112">Pointeur vers un tableau de valeurs float.</span><span class="sxs-lookup"><span data-stu-id="03951-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03951-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="03951-113">Remarks</span></span>

<span data-ttu-id="03951-114">Pour plus d’informations sur le type de propriété PT_MV_R4, voir [Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="03951-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03951-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03951-115">See also</span></span>



[<span data-ttu-id="03951-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="03951-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="03951-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="03951-117">MAPI Structures</span></span>](mapi-structures.md)

