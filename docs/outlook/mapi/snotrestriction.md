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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787212"
---
# <a name="snotrestriction"></a><span data-ttu-id="e010f-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="e010f-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="e010f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e010f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e010f-105">Décrit une restriction **pas** , qui est utilisée pour appliquer une opération **NOT** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="e010f-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e010f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e010f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e010f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e010f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="e010f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e010f-108">Members</span></span>

 <span data-ttu-id="e010f-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="e010f-109">**ulReserved**</span></span>
  
> <span data-ttu-id="e010f-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="e010f-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e010f-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="e010f-111">**lpRes**</span></span>
  
> <span data-ttu-id="e010f-112">Pointeur vers une structure [SRestriction](srestriction.md) décrivant la restriction être lié à l’opérateur **NOT** logique.</span><span class="sxs-lookup"><span data-stu-id="e010f-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e010f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="e010f-113">Remarks</span></span>

<span data-ttu-id="e010f-114">Pour plus d’informations sur la structure **SNotRestriction** , voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="e010f-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e010f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e010f-115">See also</span></span>



[<span data-ttu-id="e010f-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="e010f-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="e010f-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e010f-117">MAPI Structures</span></span>](mapi-structures.md)

