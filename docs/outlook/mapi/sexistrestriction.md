---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339276"
---
# <a name="sexistrestriction"></a><span data-ttu-id="40fce-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="40fce-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="40fce-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40fce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40fce-105">Décrit une restriction existante qui est utilisée pour tester si une propriété particulière existe sous forme de colonne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="40fce-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40fce-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="40fce-106">Header file:</span></span>  <br/> |<span data-ttu-id="40fce-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="40fce-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="40fce-108">Members</span><span class="sxs-lookup"><span data-stu-id="40fce-108">Members</span></span>

 <span data-ttu-id="40fce-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="40fce-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="40fce-110">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="40fce-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="40fce-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="40fce-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="40fce-112">Balise de propriété identifiant la colonne devant être testée pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="40fce-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="40fce-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="40fce-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="40fce-114">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="40fce-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40fce-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="40fce-115">Remarks</span></span>

<span data-ttu-id="40fce-116">La restriction EXISTS est utilisée pour garantir des résultats significatifs pour d'autres types de restrictions qui impliquent des propriétés, telles que les restrictions de propriété et de contenu.</span><span class="sxs-lookup"><span data-stu-id="40fce-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="40fce-117">Lorsqu'une restriction impliquant une propriété est transmise à une propriété [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md) et que la propriété n'existe pas, les résultats de la restriction ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="40fce-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="40fce-118">En créant une restriction **et** qui rejoint la restriction de propriété avec une restriction existante, un appelant peut être assuré de résultats précis.</span><span class="sxs-lookup"><span data-stu-id="40fce-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="40fce-119">Les restrictions d'existence ne peuvent pas être utilisées avec des propriétés de sous-objet de type PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="40fce-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="40fce-120">Pour plus d'informations sur la structure **SExistRestriction** , consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="40fce-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40fce-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40fce-121">See also</span></span>



[<span data-ttu-id="40fce-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="40fce-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="40fce-123">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="40fce-123">MAPI Structures</span></span>](mapi-structures.md)

