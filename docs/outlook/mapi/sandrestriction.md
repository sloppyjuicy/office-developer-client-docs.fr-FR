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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438882"
---
# <a name="sandrestriction"></a><span data-ttu-id="4a229-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="4a229-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="4a229-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a229-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a229-105">Décrit une restriction **AND,** qui est utilisée pour joindre un groupe de restrictions à l’aide d’une **opération LOGIQUE AND.**</span><span class="sxs-lookup"><span data-stu-id="4a229-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a229-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4a229-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a229-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a229-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="4a229-108">Members</span><span class="sxs-lookup"><span data-stu-id="4a229-108">Members</span></span>

 <span data-ttu-id="4a229-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="4a229-109">**cRes**</span></span>
  
> <span data-ttu-id="4a229-110">Nombre de restrictions de recherche dans le tableau pointés par le membre **lpRes.**</span><span class="sxs-lookup"><span data-stu-id="4a229-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="4a229-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="4a229-111">**lpRes**</span></span>
  
> <span data-ttu-id="4a229-112">Pointeur vers un tableau de structures [SRestriction](srestriction.md) qui seront combinées avec une opération **LOGIQUE AND.**</span><span class="sxs-lookup"><span data-stu-id="4a229-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4a229-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a229-113">Remarks</span></span>

<span data-ttu-id="4a229-114">Le résultat de **la SAndRestriction** est TRUE si toutes ses restrictions enfants sont évaluées à TRUE.</span><span class="sxs-lookup"><span data-stu-id="4a229-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="4a229-115">Elle est FALSE si une restriction enfant est évaluée à FALSE.</span><span class="sxs-lookup"><span data-stu-id="4a229-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="4a229-116">Pour obtenir une description des types de restrictions, comment les créer et un exemple de code, voir [à propos des restrictions.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="4a229-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a229-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a229-117">See also</span></span>



[<span data-ttu-id="4a229-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="4a229-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="4a229-119">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="4a229-119">MAPI Structures</span></span>](mapi-structures.md)

