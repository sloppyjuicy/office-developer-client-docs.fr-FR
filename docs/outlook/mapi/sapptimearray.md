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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d277908d3ec96537f63511e4d50488a694696bd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581222"
---
# <a name="sapptimearray"></a><span data-ttu-id="8b117-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="8b117-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="8b117-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b117-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b117-105">Contient un tableau de valeurs d’heure.</span><span class="sxs-lookup"><span data-stu-id="8b117-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b117-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8b117-106">Header file:</span></span>  <br/> |<span data-ttu-id="8b117-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b117-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="8b117-108">Members</span><span class="sxs-lookup"><span data-stu-id="8b117-108">Members</span></span>

 <span data-ttu-id="8b117-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8b117-109">**cValues**</span></span>
  
> <span data-ttu-id="8b117-110">Nombre de valeurs dans le tableau indiqué par le membre **lpat** .</span><span class="sxs-lookup"><span data-stu-id="8b117-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="8b117-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="8b117-111">**lpat**</span></span>
  
> <span data-ttu-id="8b117-112">Pointeur vers un tableau de valeurs de temps d’application.</span><span class="sxs-lookup"><span data-stu-id="8b117-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8b117-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b117-113">Remarks</span></span>

<span data-ttu-id="8b117-114">La structure **SAppTimeArray** est utilisée pour définir les propriétés de type PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="8b117-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="8b117-115">Pour plus d’informations sur PT_MV_APPTIME, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8b117-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b117-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b117-116">See also</span></span>



[<span data-ttu-id="8b117-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8b117-117">MAPI Structures</span></span>](mapi-structures.md)

