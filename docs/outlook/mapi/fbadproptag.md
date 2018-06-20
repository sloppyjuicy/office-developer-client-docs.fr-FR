---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783285"
---
# <a name="fbadproptag"></a><span data-ttu-id="34914-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="34914-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="34914-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34914-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34914-105">Valide une balise de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="34914-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34914-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="34914-106">Header file:</span></span>  <br/> |<span data-ttu-id="34914-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="34914-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="34914-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="34914-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="34914-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="34914-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="34914-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="34914-110">Called by:</span></span>  <br/> |<span data-ttu-id="34914-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="34914-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="34914-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34914-112">Parameters</span></span>

 <span data-ttu-id="34914-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="34914-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="34914-114">[in] La balise de propriété à valider.</span><span class="sxs-lookup"><span data-stu-id="34914-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34914-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="34914-115">Return value</span></span>

<span data-ttu-id="34914-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="34914-116">TRUE</span></span> 
  
> <span data-ttu-id="34914-117">La balise de propriété spécifié n’est pas une balise de propriété MAPI valide.</span><span class="sxs-lookup"><span data-stu-id="34914-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="34914-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="34914-118">FALSE</span></span> 
  
> <span data-ttu-id="34914-119">La balise de propriété spécifiée est une balise de propriété MAPI valide.</span><span class="sxs-lookup"><span data-stu-id="34914-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34914-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="34914-120">Remarks</span></span>

<span data-ttu-id="34914-121">La fonction **FBadPropTag** valide la balise de propriété spécifiée en fonction des définitions de MAPI.</span><span class="sxs-lookup"><span data-stu-id="34914-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="34914-122">Il se sures que le type de propriété est un des types définis par MAPI et que l’identificateur de propriété est définie comme étant de ce type.</span><span class="sxs-lookup"><span data-stu-id="34914-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34914-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34914-123">See also</span></span>



[<span data-ttu-id="34914-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="34914-124">FBadProp</span></span>](fbadprop.md)

