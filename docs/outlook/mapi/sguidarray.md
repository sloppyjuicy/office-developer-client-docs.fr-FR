---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585569"
---
# <a name="sguidarray"></a><span data-ttu-id="f3548-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="f3548-103">SGuidArray</span></span>

  
  
<span data-ttu-id="f3548-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3548-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3548-105">Contient un tableau de [GUID](guid.md) structures qui sont utilisées pour décrire une propriété de type PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="f3548-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3548-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f3548-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3548-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3548-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="f3548-108">Members</span><span class="sxs-lookup"><span data-stu-id="f3548-108">Members</span></span>

 <span data-ttu-id="f3548-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f3548-109">**cValues**</span></span>
  
> <span data-ttu-id="f3548-110">Nombre de valeurs dans le tableau indiqué par le membre **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="f3548-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="f3548-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="f3548-111">**lpguid**</span></span>
  
> <span data-ttu-id="f3548-112">Pointeur vers un tableau de structures **GUID** qui contient les valeurs d’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="f3548-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f3548-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3548-113">Remarks</span></span>

<span data-ttu-id="f3548-114">Pour plus d’informations sur PT_MV_CLSID, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f3548-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3548-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3548-115">See also</span></span>



[<span data-ttu-id="f3548-116">GUID</span><span class="sxs-lookup"><span data-stu-id="f3548-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="f3548-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f3548-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f3548-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="f3548-118">MAPI Structures</span></span>](mapi-structures.md)

