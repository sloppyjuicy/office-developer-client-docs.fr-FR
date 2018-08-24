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
ms.openlocfilehash: 054625601b496a8ec8f7745aa4cbc4715eed81a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585058"
---
# <a name="sorrestriction"></a><span data-ttu-id="f5058-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="f5058-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="f5058-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5058-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5058-105">Décrit une restriction **ou** qui est utilisée pour appliquer une opération **ou** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="f5058-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5058-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f5058-106">Header file:</span></span>  <br/> |<span data-ttu-id="f5058-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5058-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="f5058-108">Members</span><span class="sxs-lookup"><span data-stu-id="f5058-108">Members</span></span>

 <span data-ttu-id="f5058-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="f5058-109">**cRes**</span></span>
  
> <span data-ttu-id="f5058-110">Nombre de structures dans le tableau indiqué par le membre **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="f5058-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="f5058-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="f5058-111">**lpRes**</span></span>
  
> <span data-ttu-id="f5058-112">Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à être joint à l’aide de l’opération **OR** logique.</span><span class="sxs-lookup"><span data-stu-id="f5058-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f5058-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5058-113">Remarks</span></span>

<span data-ttu-id="f5058-114">Pour plus d’informations sur la structure **SOrRestriction** , voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="f5058-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5058-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5058-115">See also</span></span>



[<span data-ttu-id="f5058-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f5058-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="f5058-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="f5058-117">MAPI Structures</span></span>](mapi-structures.md)

