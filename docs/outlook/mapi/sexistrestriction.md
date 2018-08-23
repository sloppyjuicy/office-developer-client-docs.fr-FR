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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 218238bea277a2d57c77fcc9d71cd622f7da42fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571947"
---
# <a name="sexistrestriction"></a><span data-ttu-id="2b32b-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="2b32b-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="2b32b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b32b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b32b-105">Décrit une restriction existent qui est utilisée pour déterminer si une propriété particulière existe en tant que colonne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2b32b-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b32b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2b32b-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b32b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b32b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="2b32b-108">Members</span><span class="sxs-lookup"><span data-stu-id="2b32b-108">Members</span></span>

 <span data-ttu-id="2b32b-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="2b32b-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="2b32b-110">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2b32b-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="2b32b-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="2b32b-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="2b32b-112">Balise de propriété qui identifie la colonne à tester l’existence de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="2b32b-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="2b32b-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="2b32b-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="2b32b-114">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2b32b-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b32b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="2b32b-115">Remarks</span></span>

<span data-ttu-id="2b32b-116">La restriction existent est utilisée pour garantir des résultats pertinents pour les autres types de restrictions qui impliquent des propriétés, telles que des restrictions de propriété et de contenu.</span><span class="sxs-lookup"><span data-stu-id="2b32b-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="2b32b-117">Lorsqu’une restriction qui implique une propriété est transmise à [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) et la propriété n’existe pas, les résultats de la restriction ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="2b32b-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="2b32b-118">En créant une restriction **et** qui rejoint la restriction de propriété avec une restriction existe, l’appelant peut être garanti des résultats précis.</span><span class="sxs-lookup"><span data-stu-id="2b32b-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="2b32b-119">Il existe restrictions ne peut être utilisées avec les propriétés d’objet sous-sites dont type PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="2b32b-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="2b32b-120">Pour plus d’informations sur la structure **SExistRestriction** , voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="2b32b-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b32b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b32b-121">See also</span></span>



[<span data-ttu-id="2b32b-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="2b32b-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="2b32b-123">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="2b32b-123">MAPI Structures</span></span>](mapi-structures.md)

