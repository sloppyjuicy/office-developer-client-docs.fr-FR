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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9f8da0902ea4c4a862d279ee80ba566c0473c44e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592324"
---
# <a name="sandrestriction"></a><span data-ttu-id="47a21-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="47a21-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="47a21-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47a21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47a21-105">Décrit une restriction **AND** , qui est utilisée pour participer à un groupe de restrictions à l’aide d’une opération **AND** logique.</span><span class="sxs-lookup"><span data-stu-id="47a21-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47a21-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="47a21-106">Header file:</span></span>  <br/> |<span data-ttu-id="47a21-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47a21-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="47a21-108">Members</span><span class="sxs-lookup"><span data-stu-id="47a21-108">Members</span></span>

 <span data-ttu-id="47a21-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="47a21-109">**cRes**</span></span>
  
> <span data-ttu-id="47a21-110">Nombre de restrictions de recherche dans le tableau indiqué par le membre **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="47a21-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="47a21-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="47a21-111">**lpRes**</span></span>
  
> <span data-ttu-id="47a21-112">Pointeur vers un tableau de structures [SRestriction](srestriction.md) vont être combinées avec une opération **AND** logique.</span><span class="sxs-lookup"><span data-stu-id="47a21-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47a21-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="47a21-113">Remarks</span></span>

<span data-ttu-id="47a21-114">Le résultat de la **SAndRestriction** a la valeur TRUE si toutes les restrictions de ses enfants ont la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="47a21-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="47a21-115">Elle a la valeur FALSE si aucune restriction enfant a la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="47a21-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="47a21-116">Pour obtenir une description des types de restrictions, comment les créer et exemple de code, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="47a21-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47a21-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47a21-117">See also</span></span>



[<span data-ttu-id="47a21-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="47a21-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="47a21-119">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="47a21-119">MAPI Structures</span></span>](mapi-structures.md)

