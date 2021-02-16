---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406338"
---
# <a name="ppropfindprop"></a><span data-ttu-id="6ed24-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="6ed24-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="6ed24-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ed24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ed24-105">Recherche une propriété spécifiée dans un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6ed24-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ed24-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6ed24-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ed24-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6ed24-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6ed24-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="6ed24-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6ed24-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ed24-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6ed24-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="6ed24-110">Called by:</span></span>  <br/> |<span data-ttu-id="6ed24-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="6ed24-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="6ed24-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ed24-112">Parameters</span></span>

 <span data-ttu-id="6ed24-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="6ed24-113">_rgprop_</span></span>
  
> <span data-ttu-id="6ed24-114">[in] Tableau de [structures SPropValue](spropvalue.md) qui définissent les propriétés à rechercher.</span><span class="sxs-lookup"><span data-stu-id="6ed24-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="6ed24-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="6ed24-115">_cprop_</span></span>
  
> <span data-ttu-id="6ed24-116">[in] Nombre de propriétés dans le jeu de propriétés indiqué par le _paramètre rgprop._</span><span class="sxs-lookup"><span data-stu-id="6ed24-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="6ed24-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="6ed24-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="6ed24-118">[in] Balise de propriété de la propriété à rechercher dans le jeu de propriétés indiqué par le _paramètre rgprop._</span><span class="sxs-lookup"><span data-stu-id="6ed24-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6ed24-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ed24-119">Return value</span></span>

 <span data-ttu-id="6ed24-120">**PpropFindProp** renvoie une structure [SPropValue](spropvalue.md) définissant la propriété qui correspond à la balise de propriété d’entrée, ou NULL en l’absence de correspondance.</span><span class="sxs-lookup"><span data-stu-id="6ed24-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6ed24-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ed24-121">Remarks</span></span>

<span data-ttu-id="6ed24-122">Si la balise de propriété donnée indique une propriété de type PT_UNSPECIFIED, la fonction **PpropFindProp** trouve une correspondance uniquement pour l’identificateur de propriété dans la balise.</span><span class="sxs-lookup"><span data-stu-id="6ed24-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="6ed24-123">Sinon, il trouve une correspondance pour l’ensemble de la balise de propriété, y compris le type de propriété, et renvoie la propriété identifiée.</span><span class="sxs-lookup"><span data-stu-id="6ed24-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6ed24-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6ed24-124">MFCMAPI reference</span></span>

<span data-ttu-id="6ed24-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6ed24-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6ed24-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6ed24-126">**File**</span></span>|<span data-ttu-id="6ed24-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6ed24-127">**Function**</span></span>|<span data-ttu-id="6ed24-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6ed24-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6ed24-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="6ed24-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="6ed24-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="6ed24-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="6ed24-131">MFCMAPI utilise la **méthode PpropFindProp** pour rechercher les propriétés d’un jeu de propriétés ajouté à la liste.</span><span class="sxs-lookup"><span data-stu-id="6ed24-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ed24-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ed24-132">See also</span></span>



[<span data-ttu-id="6ed24-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6ed24-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

