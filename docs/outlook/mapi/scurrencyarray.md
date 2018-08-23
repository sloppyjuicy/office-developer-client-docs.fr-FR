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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572451"
---
# <a name="scurrencyarray"></a><span data-ttu-id="2a1e2-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="2a1e2-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="2a1e2-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a1e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a1e2-105">Contient un tableau de valeurs monétaires qui sont utilisées pour décrire une propriété de type PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="2a1e2-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a1e2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2a1e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a1e2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a1e2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="2a1e2-108">Members</span><span class="sxs-lookup"><span data-stu-id="2a1e2-108">Members</span></span>

 <span data-ttu-id="2a1e2-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2a1e2-109">**cValues**</span></span>
  
> <span data-ttu-id="2a1e2-110">Nombre de valeurs dans le tableau indiqué par le membre **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="2a1e2-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="2a1e2-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="2a1e2-111">**lpcur**</span></span>
  
> <span data-ttu-id="2a1e2-112">Pointeur vers un tableau de structures de [devise](currency.md) qui contiennent les valeurs monétaires.</span><span class="sxs-lookup"><span data-stu-id="2a1e2-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2a1e2-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a1e2-113">Remarks</span></span>

<span data-ttu-id="2a1e2-114">Pour plus d’informations sur PT_MV_CURRENCY, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2a1e2-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a1e2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a1e2-115">See also</span></span>



[<span data-ttu-id="2a1e2-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="2a1e2-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="2a1e2-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2a1e2-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2a1e2-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="2a1e2-118">MAPI Structures</span></span>](mapi-structures.md)

