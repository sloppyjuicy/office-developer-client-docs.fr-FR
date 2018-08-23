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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572871"
---
# <a name="slpstrarray"></a><span data-ttu-id="18b4c-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="18b4c-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="18b4c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18b4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18b4c-105">Contient un tableau de valeurs de chaîne qui sont utilisés pour décrire une propriété de type PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="18b4c-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18b4c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="18b4c-106">Header file:</span></span>  <br/> |<span data-ttu-id="18b4c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18b4c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="18b4c-108">Members</span><span class="sxs-lookup"><span data-stu-id="18b4c-108">Members</span></span>

 <span data-ttu-id="18b4c-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="18b4c-109">**cValues**</span></span>
  
> <span data-ttu-id="18b4c-110">Nombre de valeurs dans le tableau indiqué par le membre **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="18b4c-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="18b4c-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="18b4c-111">**lppszA**</span></span>
  
> <span data-ttu-id="18b4c-112">Pointeur vers un tableau de chaînes de caractères de 8 bits fin à la valeur null.</span><span class="sxs-lookup"><span data-stu-id="18b4c-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18b4c-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="18b4c-113">Remarks</span></span>

<span data-ttu-id="18b4c-114">Pour plus d’informations sur PT_MV_STRING8, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="18b4c-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18b4c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18b4c-115">See also</span></span>



[<span data-ttu-id="18b4c-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="18b4c-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="18b4c-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="18b4c-117">MAPI Structures</span></span>](mapi-structures.md)

