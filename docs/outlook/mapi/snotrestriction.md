---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575062"
---
# <a name="snotrestriction"></a><span data-ttu-id="d183b-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="d183b-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="d183b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d183b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d183b-105">Décrit une restriction **pas** , qui est utilisée pour appliquer une opération **NOT** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="d183b-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d183b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d183b-106">Header file:</span></span>  <br/> |<span data-ttu-id="d183b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d183b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="d183b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d183b-108">Members</span></span>

 <span data-ttu-id="d183b-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="d183b-109">**ulReserved**</span></span>
  
> <span data-ttu-id="d183b-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="d183b-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d183b-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="d183b-111">**lpRes**</span></span>
  
> <span data-ttu-id="d183b-112">Pointeur vers une structure [SRestriction](srestriction.md) décrivant la restriction être lié à l’opérateur **NOT** logique.</span><span class="sxs-lookup"><span data-stu-id="d183b-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d183b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="d183b-113">Remarks</span></span>

<span data-ttu-id="d183b-114">Pour plus d’informations sur la structure **SNotRestriction** , voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="d183b-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d183b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d183b-115">See also</span></span>



[<span data-ttu-id="d183b-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="d183b-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="d183b-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="d183b-117">MAPI Structures</span></span>](mapi-structures.md)

