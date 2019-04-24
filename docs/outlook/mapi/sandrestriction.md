---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344659"
---
# <a name="sandrestriction"></a><span data-ttu-id="87e52-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="87e52-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="87e52-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87e52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87e52-105">Décrit une restriction **et** , utilisée pour joindre un groupe de restrictions à l'aide d'une opération **and** logique.</span><span class="sxs-lookup"><span data-stu-id="87e52-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87e52-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="87e52-106">Header file:</span></span>  <br/> |<span data-ttu-id="87e52-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="87e52-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="87e52-108">Members</span><span class="sxs-lookup"><span data-stu-id="87e52-108">Members</span></span>

 <span data-ttu-id="87e52-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="87e52-109">**cRes**</span></span>
  
> <span data-ttu-id="87e52-110">Nombre de restrictions de recherche dans le tableau vers lequel pointe le membre **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="87e52-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="87e52-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="87e52-111">**lpRes**</span></span>
  
> <span data-ttu-id="87e52-112">Pointeur vers un tableau de structures [SRestriction](srestriction.md) qui seront combinées avec une opération **and** logique.</span><span class="sxs-lookup"><span data-stu-id="87e52-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="87e52-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="87e52-113">Remarks</span></span>

<span data-ttu-id="87e52-114">Le résultat de l' **SAndRestriction** est true si toutes ses restrictions enfants ont la valeur true.</span><span class="sxs-lookup"><span data-stu-id="87e52-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="87e52-115">Elle a la valeur FALSe si une restriction enfant prend la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="87e52-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="87e52-116">Pour obtenir une description des types de restrictions, de leur création et de l'exemple de code, reportez-vous à la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="87e52-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87e52-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87e52-117">See also</span></span>



[<span data-ttu-id="87e52-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="87e52-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="87e52-119">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="87e52-119">MAPI Structures</span></span>](mapi-structures.md)

