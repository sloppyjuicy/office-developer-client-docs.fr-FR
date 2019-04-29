---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435907"
---
# <a name="slpstrarray"></a><span data-ttu-id="7c8a9-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="7c8a9-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="7c8a9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c8a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c8a9-105">Contient un tableau de valeurs de chaîne utilisées pour décrire une propriété de type PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="7c8a9-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c8a9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7c8a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c8a9-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7c8a9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="7c8a9-108">Members</span><span class="sxs-lookup"><span data-stu-id="7c8a9-108">Members</span></span>

 <span data-ttu-id="7c8a9-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7c8a9-109">**cValues**</span></span>
  
> <span data-ttu-id="7c8a9-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="7c8a9-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="7c8a9-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="7c8a9-111">**lppszA**</span></span>
  
> <span data-ttu-id="7c8a9-112">Pointeur vers un tableau de chaînes de caractères 8 bits terminées par null.</span><span class="sxs-lookup"><span data-stu-id="7c8a9-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c8a9-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="7c8a9-113">Remarks</span></span>

<span data-ttu-id="7c8a9-114">Pour plus d'informations sur PT_MV_STRING8, consultez la rubrique [liste des types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="7c8a9-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c8a9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c8a9-115">See also</span></span>



[<span data-ttu-id="7c8a9-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7c8a9-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7c8a9-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="7c8a9-117">MAPI Structures</span></span>](mapi-structures.md)

