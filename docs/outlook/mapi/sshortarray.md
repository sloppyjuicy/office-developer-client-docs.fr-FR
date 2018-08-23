---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573032"
---
# <a name="sshortarray"></a><span data-ttu-id="bac0d-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="bac0d-103">SShortArray</span></span>

  
  
<span data-ttu-id="bac0d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bac0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bac0d-105">Contient un tableau d’entiers non signés sont utilisées pour décrire une propriété de type PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="bac0d-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bac0d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bac0d-106">Header file:</span></span>  <br/> |<span data-ttu-id="bac0d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bac0d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="bac0d-108">Members</span><span class="sxs-lookup"><span data-stu-id="bac0d-108">Members</span></span>

 <span data-ttu-id="bac0d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bac0d-109">**cValues**</span></span>
  
> <span data-ttu-id="bac0d-110">Nombre de valeurs dans le tableau indiqué par le membre **LPP** .</span><span class="sxs-lookup"><span data-stu-id="bac0d-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="bac0d-111">**LPP**</span><span class="sxs-lookup"><span data-stu-id="bac0d-111">**lpi**</span></span>
  
> <span data-ttu-id="bac0d-112">Pointeur vers un tableau de valeurs de nombre entier non signé.</span><span class="sxs-lookup"><span data-stu-id="bac0d-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bac0d-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="bac0d-113">Remarks</span></span>

<span data-ttu-id="bac0d-114">Pour plus d’informations sur PT_MV_SHORT et d’autres types de propriété, voir [Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="bac0d-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bac0d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bac0d-115">See also</span></span>



[<span data-ttu-id="bac0d-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bac0d-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="bac0d-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="bac0d-117">MAPI Structures</span></span>](mapi-structures.md)

