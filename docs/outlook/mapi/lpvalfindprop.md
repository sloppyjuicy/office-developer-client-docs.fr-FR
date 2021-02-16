---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419638"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="ca06a-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="ca06a-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="ca06a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca06a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca06a-105">Recherche une propriété spécifiée dans un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ca06a-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca06a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ca06a-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca06a-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ca06a-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ca06a-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ca06a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ca06a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ca06a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ca06a-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ca06a-110">Called by:</span></span>  <br/> |<span data-ttu-id="ca06a-111">Applications clientes et fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="ca06a-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="ca06a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca06a-112">Parameters</span></span>

 <span data-ttu-id="ca06a-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="ca06a-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="ca06a-114">[in] Balise de la propriété à rechercher dans le jeu de propriétés, indiquée par le _paramètre lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="ca06a-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="ca06a-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="ca06a-115">_cValues_</span></span>
  
> <span data-ttu-id="ca06a-116">[in] Nombre de propriétés dans le jeu de propriétés, indiqué par _le paramètre lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="ca06a-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="ca06a-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="ca06a-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="ca06a-118">[in] Tableau de **structures SPropValue** qui définit les propriétés à rechercher.</span><span class="sxs-lookup"><span data-stu-id="ca06a-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca06a-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca06a-119">Return value</span></span>

<span data-ttu-id="ca06a-120">La **fonction LpValFindProp** renvoie une structure **SPropValue** qui définit la propriété qui correspond à la balise de propriété d’entrée, ou NULL en l’absence de correspondance.</span><span class="sxs-lookup"><span data-stu-id="ca06a-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ca06a-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca06a-121">Remarks</span></span>

<span data-ttu-id="ca06a-122">La **fonction LpValFindProp** est identique à **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="ca06a-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca06a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca06a-123">See also</span></span>



[<span data-ttu-id="ca06a-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="ca06a-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="ca06a-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ca06a-125">SPropValue</span></span>](spropvalue.md)

