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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787040"
---
# <a name="sapptimearray"></a><span data-ttu-id="b6c7d-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="b6c7d-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="b6c7d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6c7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6c7d-105">Contient un tableau de valeurs d’heure.</span><span class="sxs-lookup"><span data-stu-id="b6c7d-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6c7d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b6c7d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b6c7d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6c7d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="b6c7d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b6c7d-108">Members</span></span>

 <span data-ttu-id="b6c7d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b6c7d-109">**cValues**</span></span>
  
> <span data-ttu-id="b6c7d-110">Nombre de valeurs dans le tableau indiqué par le membre **lpat** .</span><span class="sxs-lookup"><span data-stu-id="b6c7d-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="b6c7d-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="b6c7d-111">**lpat**</span></span>
  
> <span data-ttu-id="b6c7d-112">Pointeur vers un tableau de valeurs de temps d’application.</span><span class="sxs-lookup"><span data-stu-id="b6c7d-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b6c7d-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6c7d-113">Remarks</span></span>

<span data-ttu-id="b6c7d-114">La structure **SAppTimeArray** est utilisée pour définir les propriétés de type PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="b6c7d-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="b6c7d-115">Pour plus d’informations sur PT_MV_APPTIME, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b6c7d-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6c7d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6c7d-116">See also</span></span>



[<span data-ttu-id="b6c7d-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c7d-117">MAPI Structures</span></span>](mapi-structures.md)

