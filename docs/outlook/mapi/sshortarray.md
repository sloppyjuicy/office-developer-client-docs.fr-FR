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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787256"
---
# <a name="sshortarray"></a><span data-ttu-id="76b0a-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="76b0a-103">SShortArray</span></span>

  
  
<span data-ttu-id="76b0a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76b0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76b0a-105">Contient un tableau d’entiers non signés sont utilisées pour décrire une propriété de type PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="76b0a-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76b0a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="76b0a-106">Header file:</span></span>  <br/> |<span data-ttu-id="76b0a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76b0a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="76b0a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="76b0a-108">Members</span></span>

 <span data-ttu-id="76b0a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="76b0a-109">**cValues**</span></span>
  
> <span data-ttu-id="76b0a-110">Nombre de valeurs dans le tableau indiqué par le membre **LPP** .</span><span class="sxs-lookup"><span data-stu-id="76b0a-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="76b0a-111">**LPP**</span><span class="sxs-lookup"><span data-stu-id="76b0a-111">**lpi**</span></span>
  
> <span data-ttu-id="76b0a-112">Pointeur vers un tableau de valeurs de nombre entier non signé.</span><span class="sxs-lookup"><span data-stu-id="76b0a-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76b0a-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="76b0a-113">Remarks</span></span>

<span data-ttu-id="76b0a-114">Pour plus d’informations sur PT_MV_SHORT et d’autres types de propriété, voir [Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="76b0a-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76b0a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76b0a-115">See also</span></span>



[<span data-ttu-id="76b0a-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="76b0a-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="76b0a-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="76b0a-117">MAPI Structures</span></span>](mapi-structures.md)

