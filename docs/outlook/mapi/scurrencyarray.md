---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360696"
---
# <a name="scurrencyarray"></a><span data-ttu-id="8780d-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="8780d-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="8780d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8780d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8780d-105">Contient un tableau de valeurs monétaires qui sont utilisées pour décrire une propriété de type PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="8780d-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8780d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8780d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8780d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8780d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="8780d-108">Members</span><span class="sxs-lookup"><span data-stu-id="8780d-108">Members</span></span>

 <span data-ttu-id="8780d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8780d-109">**cValues**</span></span>
  
> <span data-ttu-id="8780d-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="8780d-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="8780d-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="8780d-111">**lpcur**</span></span>
  
> <span data-ttu-id="8780d-112">Pointeur vers un tableau de [](currency.md) structures monétaires qui contiennent les valeurs monétaires.</span><span class="sxs-lookup"><span data-stu-id="8780d-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8780d-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8780d-113">Remarks</span></span>

<span data-ttu-id="8780d-114">Pour plus d'informations sur PT_MV_CURRENCY, consultez la [liste des types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8780d-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8780d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8780d-115">See also</span></span>



[<span data-ttu-id="8780d-116">CONCURRENT</span><span class="sxs-lookup"><span data-stu-id="8780d-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="8780d-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8780d-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8780d-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8780d-118">MAPI Structures</span></span>](mapi-structures.md)

