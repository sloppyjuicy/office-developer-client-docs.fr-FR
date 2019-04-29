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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429872"
---
# <a name="srealarray"></a><span data-ttu-id="e0cca-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="e0cca-103">SRealArray</span></span>

  
  
<span data-ttu-id="e0cca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0cca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0cca-105">Contient un tableau de valeurs de type float qui permettent de décrire une propriété de type PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="e0cca-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0cca-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e0cca-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0cca-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e0cca-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="e0cca-108">Members</span><span class="sxs-lookup"><span data-stu-id="e0cca-108">Members</span></span>

 <span data-ttu-id="e0cca-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e0cca-109">**cValues**</span></span>
  
> <span data-ttu-id="e0cca-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="e0cca-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="e0cca-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="e0cca-111">**lpflt**</span></span>
  
> <span data-ttu-id="e0cca-112">Pointeur vers un tableau de valeurs de type float.</span><span class="sxs-lookup"><span data-stu-id="e0cca-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0cca-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0cca-113">Remarks</span></span>

<span data-ttu-id="e0cca-114">Pour plus d'informations sur le type de propriété PT_MV_R4, consultez la rubrique [types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="e0cca-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0cca-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0cca-115">See also</span></span>



[<span data-ttu-id="e0cca-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e0cca-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e0cca-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e0cca-117">MAPI Structures</span></span>](mapi-structures.md)

