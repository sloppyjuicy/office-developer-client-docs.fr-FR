---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a44974accea30b5d1406c9cc74570012f61639e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580648"
---
# <a name="slongarray"></a><span data-ttu-id="2f617-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="2f617-103">SLongArray</span></span>

  
  
<span data-ttu-id="2f617-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f617-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f617-105">Contient un tableau de types de valeur de type LONG qui sont utilisées pour décrire une propriété de type PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="2f617-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f617-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2f617-106">Header file:</span></span>  <br/> |<span data-ttu-id="2f617-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f617-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="2f617-108">Members</span><span class="sxs-lookup"><span data-stu-id="2f617-108">Members</span></span>

 <span data-ttu-id="2f617-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2f617-109">**cValues**</span></span>
  
> <span data-ttu-id="2f617-110">Nombre de valeurs dans le tableau indiqué par le membre **lpl** .</span><span class="sxs-lookup"><span data-stu-id="2f617-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="2f617-111">**LPL**</span><span class="sxs-lookup"><span data-stu-id="2f617-111">**lpl**</span></span>
  
> <span data-ttu-id="2f617-112">Pointeur vers un tableau de valeurs de type LONG.</span><span class="sxs-lookup"><span data-stu-id="2f617-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f617-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f617-113">Remarks</span></span>

<span data-ttu-id="2f617-114">Pour plus d’informations sur PT_MV_LONG, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2f617-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f617-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f617-115">See also</span></span>



[<span data-ttu-id="2f617-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2f617-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2f617-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="2f617-117">MAPI Structures</span></span>](mapi-structures.md)

