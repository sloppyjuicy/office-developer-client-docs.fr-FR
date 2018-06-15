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
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19787151"
---
# <a name="sguidarray"></a><span data-ttu-id="908da-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="908da-103">SGuidArray</span></span>

  
  
<span data-ttu-id="908da-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="908da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="908da-105">Contient un tableau de [GUID](guid.md) structures qui sont utilisées pour décrire une propriété de type PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="908da-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="908da-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="908da-106">Header file:</span></span>  <br/> |<span data-ttu-id="908da-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="908da-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="908da-108">Membres</span><span class="sxs-lookup"><span data-stu-id="908da-108">Members</span></span>

 <span data-ttu-id="908da-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="908da-109">**cValues**</span></span>
  
> <span data-ttu-id="908da-110">Nombre de valeurs dans le tableau indiqué par le membre **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="908da-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="908da-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="908da-111">**lpguid**</span></span>
  
> <span data-ttu-id="908da-112">Pointeur vers un tableau de structures **GUID** qui contient les valeurs d’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="908da-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="908da-113">Note</span><span class="sxs-lookup"><span data-stu-id="908da-113">Remarks</span></span>

<span data-ttu-id="908da-114">Pour plus d’informations sur PT_MV_CLSID, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="908da-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="908da-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="908da-115">See also</span></span>



[<span data-ttu-id="908da-116">GUID</span><span class="sxs-lookup"><span data-stu-id="908da-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="908da-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="908da-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="908da-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="908da-118">MAPI Structures</span></span>](mapi-structures.md)

