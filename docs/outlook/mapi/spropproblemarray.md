---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357840"
---
# <a name="spropproblemarray"></a><span data-ttu-id="42733-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="42733-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="42733-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42733-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42733-105">Contient un tableau d'une ou de plusieurs structures [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="42733-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42733-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="42733-106">Header file:</span></span>  <br/> |<span data-ttu-id="42733-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="42733-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="42733-108">Macros connexes:</span><span class="sxs-lookup"><span data-stu-id="42733-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="42733-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="42733-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="42733-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="42733-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="42733-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="42733-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="42733-112">Members</span><span class="sxs-lookup"><span data-stu-id="42733-112">Members</span></span>

 <span data-ttu-id="42733-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="42733-113">**cProblem**</span></span>
  
> <span data-ttu-id="42733-114">Nombre de structures [SPropProblem](spropproblem.md) dans le tableau indiqué par le membre **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="42733-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="42733-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="42733-115">**aProblem**</span></span>
  
> <span data-ttu-id="42733-116">Tableau de structures **SPropProblem** , qui décrivent chacune une erreur de propriété.</span><span class="sxs-lookup"><span data-stu-id="42733-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42733-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="42733-117">Remarks</span></span>

<span data-ttu-id="42733-118">Pour plus d'informations sur la façon dont les structures **SPropProblem** et **SPropProblemArray** fonctionnent avec les erreurs liées aux propriétés, voir [MAPI named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="42733-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42733-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42733-119">See also</span></span>



[<span data-ttu-id="42733-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="42733-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="42733-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="42733-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="42733-122">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="42733-122">MAPI Structures</span></span>](mapi-structures.md)

