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
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787220"
---
# <a name="sorrestriction"></a><span data-ttu-id="42d72-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="42d72-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="42d72-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42d72-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42d72-105">Décrit une restriction **ou** qui est utilisée pour appliquer une opération **ou** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="42d72-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42d72-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="42d72-106">Header file:</span></span>  <br/> |<span data-ttu-id="42d72-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42d72-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="42d72-108">Membres</span><span class="sxs-lookup"><span data-stu-id="42d72-108">Members</span></span>

 <span data-ttu-id="42d72-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="42d72-109">**cRes**</span></span>
  
> <span data-ttu-id="42d72-110">Nombre de structures dans le tableau indiqué par le membre **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="42d72-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="42d72-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="42d72-111">**lpRes**</span></span>
  
> <span data-ttu-id="42d72-112">Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à être joint à l’aide de l’opération **OR** logique.</span><span class="sxs-lookup"><span data-stu-id="42d72-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42d72-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="42d72-113">Remarks</span></span>

<span data-ttu-id="42d72-114">Pour plus d’informations sur la structure **SOrRestriction** , voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="42d72-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42d72-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42d72-115">See also</span></span>



[<span data-ttu-id="42d72-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="42d72-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="42d72-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="42d72-117">MAPI Structures</span></span>](mapi-structures.md)

