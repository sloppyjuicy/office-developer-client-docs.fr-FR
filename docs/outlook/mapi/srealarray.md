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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787238"
---
# <a name="srealarray"></a><span data-ttu-id="500ab-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="500ab-103">SRealArray</span></span>

  
  
<span data-ttu-id="500ab-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="500ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="500ab-105">Contient un tableau de valeurs float qui sont utilisées pour décrire une propriété de type PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="500ab-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="500ab-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="500ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="500ab-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="500ab-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="500ab-108">Membres</span><span class="sxs-lookup"><span data-stu-id="500ab-108">Members</span></span>

 <span data-ttu-id="500ab-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="500ab-109">**cValues**</span></span>
  
> <span data-ttu-id="500ab-110">Nombre de valeurs dans le tableau indiqué par le membre **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="500ab-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="500ab-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="500ab-111">**lpflt**</span></span>
  
> <span data-ttu-id="500ab-112">Pointeur vers un tableau de valeurs float.</span><span class="sxs-lookup"><span data-stu-id="500ab-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="500ab-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="500ab-113">Remarks</span></span>

<span data-ttu-id="500ab-114">Pour plus d’informations sur le type de propriété PT_MV_R4, voir [Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="500ab-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="500ab-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="500ab-115">See also</span></span>



[<span data-ttu-id="500ab-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="500ab-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="500ab-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="500ab-117">MAPI Structures</span></span>](mapi-structures.md)

