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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787087"
---
# <a name="sdatetimearray"></a><span data-ttu-id="9dc34-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="9dc34-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="9dc34-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9dc34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9dc34-105">Contient un tableau de valeurs de temps qui sont utilisés pour décrire une propriété de type PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="9dc34-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9dc34-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9dc34-106">Header file:</span></span>  <br/> |<span data-ttu-id="9dc34-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9dc34-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="9dc34-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9dc34-108">Members</span></span>

 <span data-ttu-id="9dc34-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="9dc34-109">**cValues**</span></span>
  
> <span data-ttu-id="9dc34-110">Nombre de valeurs dans le tableau indiqué par le membre **lpft** .</span><span class="sxs-lookup"><span data-stu-id="9dc34-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="9dc34-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="9dc34-111">**lpft**</span></span>
  
> <span data-ttu-id="9dc34-112">Pointeur vers un tableau de structures [FILETIME](filetime.md) qui contiennent les valeurs d’heure.</span><span class="sxs-lookup"><span data-stu-id="9dc34-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9dc34-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="9dc34-113">Remarks</span></span>

<span data-ttu-id="9dc34-114">Pour plus d’informations sur PT_MV_SYSTIME, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="9dc34-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9dc34-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dc34-115">See also</span></span>



[<span data-ttu-id="9dc34-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="9dc34-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="9dc34-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9dc34-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="9dc34-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="9dc34-118">MAPI Structures</span></span>](mapi-structures.md)

