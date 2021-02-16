---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430384"
---
# <a name="sapptimearray"></a><span data-ttu-id="8b7f2-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="8b7f2-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="8b7f2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b7f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b7f2-105">Contient un tableau de valeurs d’heure.</span><span class="sxs-lookup"><span data-stu-id="8b7f2-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b7f2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8b7f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="8b7f2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b7f2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="8b7f2-108">Members</span><span class="sxs-lookup"><span data-stu-id="8b7f2-108">Members</span></span>

 <span data-ttu-id="8b7f2-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8b7f2-109">**cValues**</span></span>
  
> <span data-ttu-id="8b7f2-110">Nombre de valeurs dans le tableau pointées par **le membre lpat.**</span><span class="sxs-lookup"><span data-stu-id="8b7f2-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="8b7f2-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="8b7f2-111">**lpat**</span></span>
  
> <span data-ttu-id="8b7f2-112">Pointeur vers un tableau de valeurs d’heure d’application.</span><span class="sxs-lookup"><span data-stu-id="8b7f2-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8b7f2-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b7f2-113">Remarks</span></span>

<span data-ttu-id="8b7f2-114">La structure **SAppTimeArray permet** de définir des propriétés de type PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="8b7f2-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="8b7f2-115">Pour plus d’informations PT_MV_APPTIME, voir [Liste des types de propriétés.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="8b7f2-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b7f2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b7f2-116">See also</span></span>



[<span data-ttu-id="8b7f2-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8b7f2-117">MAPI Structures</span></span>](mapi-structures.md)

