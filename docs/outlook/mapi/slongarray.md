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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414528"
---
# <a name="slongarray"></a><span data-ttu-id="117bc-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="117bc-103">SLongArray</span></span>

  
  
<span data-ttu-id="117bc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="117bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="117bc-105">Contient un tableau de types de valeur LONG utilisés pour décrire une propriété de type PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="117bc-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="117bc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="117bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="117bc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="117bc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="117bc-108">Members</span><span class="sxs-lookup"><span data-stu-id="117bc-108">Members</span></span>

 <span data-ttu-id="117bc-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="117bc-109">**cValues**</span></span>
  
> <span data-ttu-id="117bc-110">Nombre de valeurs dans le tableau pointées par le **membre lpl.**</span><span class="sxs-lookup"><span data-stu-id="117bc-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="117bc-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="117bc-111">**lpl**</span></span>
  
> <span data-ttu-id="117bc-112">Pointeur vers un tableau de valeurs LONG.</span><span class="sxs-lookup"><span data-stu-id="117bc-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="117bc-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="117bc-113">Remarks</span></span>

<span data-ttu-id="117bc-114">Pour plus d’informations sur PT_MV_LONG, voir [Liste des types de propriétés.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="117bc-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="117bc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="117bc-115">See also</span></span>



[<span data-ttu-id="117bc-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="117bc-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="117bc-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="117bc-117">MAPI Structures</span></span>](mapi-structures.md)

