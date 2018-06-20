---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787099"
---
# <a name="sdoublearray"></a><span data-ttu-id="19156-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="19156-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="19156-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19156-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19156-105">Contient un tableau de type double utilisé pour décrire une propriété de type PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="19156-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19156-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="19156-106">Header file:</span></span>  <br/> |<span data-ttu-id="19156-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19156-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="19156-108">Membres</span><span class="sxs-lookup"><span data-stu-id="19156-108">Members</span></span>

 <span data-ttu-id="19156-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="19156-109">**cValues**</span></span>
  
> <span data-ttu-id="19156-110">Nombre de valeurs dans le tableau indiqué par le membre **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="19156-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="19156-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="19156-111">**lpdbl**</span></span>
  
> <span data-ttu-id="19156-112">Pointeur vers un tableau de valeurs de type doubles.</span><span class="sxs-lookup"><span data-stu-id="19156-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19156-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="19156-113">Remarks</span></span>

<span data-ttu-id="19156-114">Pour plus d’informations sur PT_MV_DOUBLE, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="19156-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19156-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19156-115">See also</span></span>



[<span data-ttu-id="19156-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="19156-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="19156-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="19156-117">MAPI Structures</span></span>](mapi-structures.md)

