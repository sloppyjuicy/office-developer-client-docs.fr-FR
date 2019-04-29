---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437930"
---
# <a name="sorrestriction"></a><span data-ttu-id="48539-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="48539-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="48539-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48539-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48539-105">Décrit une restriction **ou** qui est utilisée pour appliquer une opération **or** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="48539-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48539-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="48539-106">Header file:</span></span>  <br/> |<span data-ttu-id="48539-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="48539-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="48539-108">Members</span><span class="sxs-lookup"><span data-stu-id="48539-108">Members</span></span>

 <span data-ttu-id="48539-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="48539-109">**cRes**</span></span>
  
> <span data-ttu-id="48539-110">Nombre de structures dans le tableau vers lequel pointe le membre **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="48539-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="48539-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="48539-111">**lpRes**</span></span>
  
> <span data-ttu-id="48539-112">Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à joindre à l'aide de l'opération **or** logique.</span><span class="sxs-lookup"><span data-stu-id="48539-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="48539-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="48539-113">Remarks</span></span>

<span data-ttu-id="48539-114">Pour plus d'informations sur la structure **SOrRestriction** , consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="48539-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48539-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48539-115">See also</span></span>



[<span data-ttu-id="48539-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="48539-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="48539-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="48539-117">MAPI Structures</span></span>](mapi-structures.md)

