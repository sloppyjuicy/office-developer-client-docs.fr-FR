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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787195"
---
# <a name="slpstrarray"></a><span data-ttu-id="e5aa8-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="e5aa8-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="e5aa8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5aa8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5aa8-105">Contient un tableau de valeurs de chaîne qui sont utilisés pour décrire une propriété de type PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5aa8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e5aa8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5aa8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5aa8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="e5aa8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e5aa8-108">Members</span></span>

 <span data-ttu-id="e5aa8-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e5aa8-109">**cValues**</span></span>
  
> <span data-ttu-id="e5aa8-110">Nombre de valeurs dans le tableau indiqué par le membre **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="e5aa8-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="e5aa8-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="e5aa8-111">**lppszA**</span></span>
  
> <span data-ttu-id="e5aa8-112">Pointeur vers un tableau de chaînes de caractères de 8 bits fin à la valeur null.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5aa8-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5aa8-113">Remarks</span></span>

<span data-ttu-id="e5aa8-114">Pour plus d’informations sur PT_MV_STRING8, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="e5aa8-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5aa8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5aa8-115">See also</span></span>



[<span data-ttu-id="e5aa8-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e5aa8-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e5aa8-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="e5aa8-117">MAPI Structures</span></span>](mapi-structures.md)

