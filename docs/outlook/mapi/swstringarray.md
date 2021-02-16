---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413604"
---
# <a name="swstringarray"></a><span data-ttu-id="d7c91-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="d7c91-103">SWStringArray</span></span>

  
  
<span data-ttu-id="d7c91-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7c91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7c91-105">Contient un tableau de chaînes de caractères qui sont utilisées pour décrire une propriété de type PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d7c91-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7c91-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d7c91-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7c91-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7c91-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="d7c91-108">Members</span><span class="sxs-lookup"><span data-stu-id="d7c91-108">Members</span></span>

 <span data-ttu-id="d7c91-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d7c91-109">**cValues**</span></span>
  
> <span data-ttu-id="d7c91-110">Nombre de chaînes dans le tableau pointées par **le membre lppszW.**</span><span class="sxs-lookup"><span data-stu-id="d7c91-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="d7c91-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="d7c91-111">**lppszW**</span></span>
  
> <span data-ttu-id="d7c91-112">Pointeur vers un tableau de chaînes de caractères Unicode terminées par null.</span><span class="sxs-lookup"><span data-stu-id="d7c91-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7c91-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7c91-113">Remarks</span></span>

<span data-ttu-id="d7c91-114">Pour plus d’informations sur PT_MV_UNICODE, voir [Types de propriétés.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="d7c91-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7c91-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7c91-115">See also</span></span>



[<span data-ttu-id="d7c91-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d7c91-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d7c91-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="d7c91-117">MAPI Structures</span></span>](mapi-structures.md)

