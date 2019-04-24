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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345100"
---
# <a name="sorrestriction"></a><span data-ttu-id="96583-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="96583-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="96583-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96583-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96583-105">Décrit une restriction **ou** qui est utilisée pour appliquer une opération **or** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="96583-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96583-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="96583-106">Header file:</span></span>  <br/> |<span data-ttu-id="96583-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="96583-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="96583-108">Members</span><span class="sxs-lookup"><span data-stu-id="96583-108">Members</span></span>

 <span data-ttu-id="96583-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="96583-109">**cRes**</span></span>
  
> <span data-ttu-id="96583-110">Nombre de structures dans le tableau vers lequel pointe le membre **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="96583-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="96583-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="96583-111">**lpRes**</span></span>
  
> <span data-ttu-id="96583-112">Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à joindre à l'aide de l'opération **or** logique.</span><span class="sxs-lookup"><span data-stu-id="96583-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="96583-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="96583-113">Remarks</span></span>

<span data-ttu-id="96583-114">Pour plus d'informations sur la structure **SOrRestriction** , consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="96583-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96583-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96583-115">See also</span></span>



[<span data-ttu-id="96583-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="96583-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="96583-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="96583-117">MAPI Structures</span></span>](mapi-structures.md)

