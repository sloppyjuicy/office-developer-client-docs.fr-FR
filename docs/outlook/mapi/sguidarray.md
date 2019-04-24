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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339213"
---
# <a name="sguidarray"></a><span data-ttu-id="6763f-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="6763f-103">SGuidArray</span></span>

  
  
<span data-ttu-id="6763f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6763f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6763f-105">Contient un tableau de structures [GUID](guid.md) utilisées pour décrire une propriété de type PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="6763f-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6763f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6763f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6763f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6763f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="6763f-108">Members</span><span class="sxs-lookup"><span data-stu-id="6763f-108">Members</span></span>

 <span data-ttu-id="6763f-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="6763f-109">**cValues**</span></span>
  
> <span data-ttu-id="6763f-110">Nombre de valeurs dans le tableau vers lequel pointe le membre **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="6763f-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="6763f-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="6763f-111">**lpguid**</span></span>
  
> <span data-ttu-id="6763f-112">Pointeur vers un tableau de structures **GUID** qui contient les valeurs d'identificateurs de classe.</span><span class="sxs-lookup"><span data-stu-id="6763f-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6763f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="6763f-113">Remarks</span></span>

<span data-ttu-id="6763f-114">Pour plus d'informations sur PT_MV_CLSID, consultez la rubrique [liste des types de propriétés](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="6763f-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6763f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6763f-115">See also</span></span>



[<span data-ttu-id="6763f-116">GUID</span><span class="sxs-lookup"><span data-stu-id="6763f-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="6763f-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6763f-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6763f-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="6763f-118">MAPI Structures</span></span>](mapi-structures.md)

