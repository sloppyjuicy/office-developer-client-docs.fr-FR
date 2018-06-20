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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787307"
---
# <a name="swstringarray"></a><span data-ttu-id="ac8b2-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="ac8b2-103">SWStringArray</span></span>

  
  
<span data-ttu-id="ac8b2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac8b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac8b2-105">Contient un tableau de chaînes de caractères qui sont utilisées pour décrire une propriété de type PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ac8b2-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac8b2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ac8b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="ac8b2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac8b2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="ac8b2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ac8b2-108">Members</span></span>

 <span data-ttu-id="ac8b2-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="ac8b2-109">**cValues**</span></span>
  
> <span data-ttu-id="ac8b2-110">Nombre de chaînes dans le tableau indiqué par le membre **lppszW** .</span><span class="sxs-lookup"><span data-stu-id="ac8b2-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="ac8b2-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="ac8b2-111">**lppszW**</span></span>
  
> <span data-ttu-id="ac8b2-112">Pointeur vers un tableau de chaînes de caractères Unicode terminée-null.</span><span class="sxs-lookup"><span data-stu-id="ac8b2-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac8b2-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac8b2-113">Remarks</span></span>

<span data-ttu-id="ac8b2-114">Pour plus d’informations sur PT_MV_UNICODE, reportez-vous à [Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="ac8b2-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac8b2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac8b2-115">See also</span></span>



[<span data-ttu-id="ac8b2-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ac8b2-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ac8b2-117">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8b2-117">MAPI Structures</span></span>](mapi-structures.md)

