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
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787243"
---
# <a name="spropproblemarray"></a><span data-ttu-id="38af6-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="38af6-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="38af6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38af6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38af6-105">Contient un tableau d’une ou plusieurs structures [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="38af6-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38af6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="38af6-106">Header file:</span></span>  <br/> |<span data-ttu-id="38af6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38af6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="38af6-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="38af6-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="38af6-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="38af6-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="38af6-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="38af6-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="38af6-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="38af6-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="38af6-112">Membres</span><span class="sxs-lookup"><span data-stu-id="38af6-112">Members</span></span>

 <span data-ttu-id="38af6-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="38af6-113">**cProblem**</span></span>
  
> <span data-ttu-id="38af6-114">Nombre de structures [SPropProblem](spropproblem.md) dans le tableau indiqué par le membre **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="38af6-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="38af6-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="38af6-115">**aProblem**</span></span>
  
> <span data-ttu-id="38af6-116">Tableau de structures **SPropProblem** , décrivant chacun une erreur de propriété.</span><span class="sxs-lookup"><span data-stu-id="38af6-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="38af6-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="38af6-117">Remarks</span></span>

<span data-ttu-id="38af6-118">Pour plus d’informations sur le fonctionnement des structures **SPropProblem** et **SPropProblemArray** avec des erreurs liées aux propriétés, voir [Les propriétés MAPI nommée](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="38af6-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38af6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38af6-119">See also</span></span>



[<span data-ttu-id="38af6-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="38af6-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="38af6-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="38af6-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="38af6-122">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="38af6-122">MAPI Structures</span></span>](mapi-structures.md)

