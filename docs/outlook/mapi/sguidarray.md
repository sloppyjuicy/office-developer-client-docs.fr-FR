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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424923"
---
# <a name="sguidarray"></a><span data-ttu-id="0e59c-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="0e59c-103">SGuidArray</span></span>

  
  
<span data-ttu-id="0e59c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e59c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e59c-105">Contient un tableau de structures [GUID](guid.md) utilisées pour décrire une propriété de type PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="0e59c-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e59c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0e59c-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e59c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e59c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="0e59c-108">Members</span><span class="sxs-lookup"><span data-stu-id="0e59c-108">Members</span></span>

 <span data-ttu-id="0e59c-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0e59c-109">**cValues**</span></span>
  
> <span data-ttu-id="0e59c-110">Nombre de valeurs dans le tableau pointées par **le membre lpguid.**</span><span class="sxs-lookup"><span data-stu-id="0e59c-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="0e59c-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="0e59c-111">**lpguid**</span></span>
  
> <span data-ttu-id="0e59c-112">Pointeur vers un tableau de structures **GUID** qui contient les valeurs d’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="0e59c-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e59c-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e59c-113">Remarks</span></span>

<span data-ttu-id="0e59c-114">Pour plus d’informations PT_MV_CLSID, voir [Liste des types de propriétés.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="0e59c-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e59c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e59c-115">See also</span></span>



[<span data-ttu-id="0e59c-116">GUID</span><span class="sxs-lookup"><span data-stu-id="0e59c-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="0e59c-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0e59c-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0e59c-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="0e59c-118">MAPI Structures</span></span>](mapi-structures.md)

