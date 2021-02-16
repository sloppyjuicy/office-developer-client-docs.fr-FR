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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433646"
---
# <a name="fbadproptag"></a><span data-ttu-id="d7ee5-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="d7ee5-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="d7ee5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7ee5-105">Valide une balise de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7ee5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d7ee5-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7ee5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d7ee5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d7ee5-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d7ee5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7ee5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7ee5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7ee5-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d7ee5-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7ee5-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d7ee5-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="d7ee5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7ee5-112">Parameters</span></span>

 <span data-ttu-id="d7ee5-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d7ee5-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="d7ee5-114">[in] Balise de propriété à valider.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7ee5-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7ee5-115">Return value</span></span>

<span data-ttu-id="d7ee5-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="d7ee5-116">TRUE</span></span> 
  
> <span data-ttu-id="d7ee5-117">La balise de propriété spécifiée n’est pas une balise de propriété MAPI valide.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="d7ee5-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="d7ee5-118">FALSE</span></span> 
  
> <span data-ttu-id="d7ee5-119">La balise de propriété spécifiée est une balise de propriété MAPI valide.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7ee5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7ee5-120">Remarks</span></span>

<span data-ttu-id="d7ee5-121">La **fonction FBadPropTag** valide la balise de propriété spécifiée en fonction des définitions MAPI.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="d7ee5-122">Il s’assure que le type de propriété est l’un des types définis par MAPI et que l’identificateur de propriété est défini comme étant de ce type.</span><span class="sxs-lookup"><span data-stu-id="d7ee5-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7ee5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7ee5-123">See also</span></span>



[<span data-ttu-id="d7ee5-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="d7ee5-124">FBadProp</span></span>](fbadprop.md)

