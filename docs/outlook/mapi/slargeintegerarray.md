---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382728"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="0e6e9-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="0e6e9-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="0e6e9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e6e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e6e9-105">Contient un tableau de structures [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) qui sont utilisées pour décrire une propriété de type PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="0e6e9-105">Contains an array of [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e6e9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0e6e9-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e6e9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e6e9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="0e6e9-108">Members</span><span class="sxs-lookup"><span data-stu-id="0e6e9-108">Members</span></span>

 <span data-ttu-id="0e6e9-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0e6e9-109">**cValues**</span></span>
  
> <span data-ttu-id="0e6e9-110">Nombre de valeurs dans le tableau indiqué par le membre **lpli** .</span><span class="sxs-lookup"><span data-stu-id="0e6e9-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="0e6e9-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="0e6e9-111">**lpli**</span></span>
  
> <span data-ttu-id="0e6e9-112">Pointeur vers un tableau de structures **LARGE_INTEGER** contenant les valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="0e6e9-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e6e9-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e6e9-113">Remarks</span></span>

<span data-ttu-id="0e6e9-114">Pour plus d’informations sur PT_MV_18, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="0e6e9-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e6e9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e6e9-115">See also</span></span>



[<span data-ttu-id="0e6e9-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0e6e9-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0e6e9-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="0e6e9-117">MAPI Structures</span></span>](mapi-structures.md)

