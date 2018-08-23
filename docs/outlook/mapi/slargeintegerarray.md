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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 29b26996bc337045489758a14857a30fafe48e54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576434"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="7dd76-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="7dd76-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="7dd76-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dd76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dd76-105">Contient un tableau de structures [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) qui sont utilisées pour décrire une propriété de type PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="7dd76-105">Contains an array of [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7dd76-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7dd76-106">Header file:</span></span>  <br/> |<span data-ttu-id="7dd76-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7dd76-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="7dd76-108">Members</span><span class="sxs-lookup"><span data-stu-id="7dd76-108">Members</span></span>

 <span data-ttu-id="7dd76-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7dd76-109">**cValues**</span></span>
  
> <span data-ttu-id="7dd76-110">Nombre de valeurs dans le tableau indiqué par le membre **lpli** .</span><span class="sxs-lookup"><span data-stu-id="7dd76-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="7dd76-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="7dd76-111">**lpli**</span></span>
  
> <span data-ttu-id="7dd76-112">Pointeur vers un tableau de structures **LARGE_INTEGER** contenant les valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="7dd76-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7dd76-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="7dd76-113">Remarks</span></span>

<span data-ttu-id="7dd76-114">Pour plus d’informations sur PT_MV_18, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="7dd76-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7dd76-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dd76-115">See also</span></span>



[<span data-ttu-id="7dd76-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7dd76-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7dd76-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="7dd76-117">MAPI Structures</span></span>](mapi-structures.md)

