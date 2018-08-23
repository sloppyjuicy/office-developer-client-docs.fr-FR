---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578093"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="92c60-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="92c60-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="92c60-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92c60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92c60-105">Recherche une propriété spécifiée dans une propriété définie.</span><span class="sxs-lookup"><span data-stu-id="92c60-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92c60-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="92c60-106">Header file:</span></span>  <br/> |<span data-ttu-id="92c60-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="92c60-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="92c60-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="92c60-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="92c60-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="92c60-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="92c60-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="92c60-110">Called by:</span></span>  <br/> |<span data-ttu-id="92c60-111">Applications clientes et des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="92c60-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="92c60-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92c60-112">Parameters</span></span>

 <span data-ttu-id="92c60-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="92c60-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="92c60-114">[in] Balise de la propriété à rechercher dans le jeu de propriétés, indiqué par le paramètre _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="92c60-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="92c60-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="92c60-115">_cValues_</span></span>
  
> <span data-ttu-id="92c60-116">[in] Nombre de propriétés dans le jeu de propriétés, indiquée par le paramètre _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="92c60-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="92c60-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="92c60-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="92c60-118">[in] Tableau des structures **SPropValue** qui définit les propriétés à rechercher.</span><span class="sxs-lookup"><span data-stu-id="92c60-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="92c60-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="92c60-119">Return value</span></span>

<span data-ttu-id="92c60-120">La fonction **LpValFindProp** renvoie une structure **SPropValue** qui définit la propriété qui correspond à la balise de propriété d’entrée, ou NULL si aucune correspondance n’existe.</span><span class="sxs-lookup"><span data-stu-id="92c60-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="92c60-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="92c60-121">Remarks</span></span>

<span data-ttu-id="92c60-122">La fonction **LpValFindProp** est identique à **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="92c60-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="92c60-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92c60-123">See also</span></span>



[<span data-ttu-id="92c60-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="92c60-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="92c60-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="92c60-125">SPropValue</span></span>](spropvalue.md)

