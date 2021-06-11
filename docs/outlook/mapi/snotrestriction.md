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
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426652"
---
# <a name="snotrestriction"></a><span data-ttu-id="443fc-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="443fc-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="443fc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="443fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="443fc-105">Décrit une restriction **NOT,** qui est utilisée pour appliquer une opération **LOGIQUE NOT** à une restriction.</span><span class="sxs-lookup"><span data-stu-id="443fc-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="443fc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="443fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="443fc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="443fc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="443fc-108">Members</span><span class="sxs-lookup"><span data-stu-id="443fc-108">Members</span></span>

 <span data-ttu-id="443fc-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="443fc-109">**ulReserved**</span></span>
  
> <span data-ttu-id="443fc-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="443fc-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="443fc-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="443fc-111">**lpRes**</span></span>
  
> <span data-ttu-id="443fc-112">Pointeur vers une structure [SRestriction](srestriction.md) décrivant la restriction à joindre à l’opérateur **logique NOT.**</span><span class="sxs-lookup"><span data-stu-id="443fc-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="443fc-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="443fc-113">Remarks</span></span>

<span data-ttu-id="443fc-114">Pour plus d’informations sur la structure **SNotRestriction,** voir [À propos des restrictions.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="443fc-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="443fc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="443fc-115">See also</span></span>



[<span data-ttu-id="443fc-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="443fc-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="443fc-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="443fc-117">MAPI Structures</span></span>](mapi-structures.md)

