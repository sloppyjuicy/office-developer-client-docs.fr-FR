---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406779"
---
# <a name="sdatetimearray"></a><span data-ttu-id="f5883-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="f5883-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="f5883-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5883-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5883-105">Contient un tableau de valeurs d’heure utilisées pour décrire une propriété de type PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="f5883-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5883-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f5883-106">Header file:</span></span>  <br/> |<span data-ttu-id="f5883-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5883-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="f5883-108">Members</span><span class="sxs-lookup"><span data-stu-id="f5883-108">Members</span></span>

 <span data-ttu-id="f5883-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f5883-109">**cValues**</span></span>
  
> <span data-ttu-id="f5883-110">Nombre de valeurs dans le tableau pointées par **le membre lpft.**</span><span class="sxs-lookup"><span data-stu-id="f5883-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="f5883-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="f5883-111">**lpft**</span></span>
  
> <span data-ttu-id="f5883-112">Pointeur vers un tableau de structures [FILETIME](filetime.md) qui contiennent les valeurs d’heure.</span><span class="sxs-lookup"><span data-stu-id="f5883-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f5883-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5883-113">Remarks</span></span>

<span data-ttu-id="f5883-114">Pour plus d’informations PT_MV_SYSTIME, voir [Liste des types de propriétés.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="f5883-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5883-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5883-115">See also</span></span>



[<span data-ttu-id="f5883-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="f5883-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="f5883-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f5883-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f5883-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="f5883-118">MAPI Structures</span></span>](mapi-structures.md)

