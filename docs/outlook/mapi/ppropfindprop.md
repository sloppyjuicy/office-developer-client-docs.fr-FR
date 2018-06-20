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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786942"
---
# <a name="ppropfindprop"></a><span data-ttu-id="5416e-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="5416e-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="5416e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5416e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5416e-105">Recherche une propriété spécifiée dans une propriété définie.</span><span class="sxs-lookup"><span data-stu-id="5416e-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5416e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5416e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5416e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5416e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5416e-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="5416e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5416e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5416e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5416e-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="5416e-110">Called by:</span></span>  <br/> |<span data-ttu-id="5416e-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5416e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="5416e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5416e-112">Parameters</span></span>

 <span data-ttu-id="5416e-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="5416e-113">_rgprop_</span></span>
  
> <span data-ttu-id="5416e-114">[in] Tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à rechercher.</span><span class="sxs-lookup"><span data-stu-id="5416e-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="5416e-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="5416e-115">_cprop_</span></span>
  
> <span data-ttu-id="5416e-116">[in] Nombre de propriétés dans le jeu de propriétés indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="5416e-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="5416e-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="5416e-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="5416e-118">[in] Balise de propriété pour la propriété à rechercher dans le jeu de propriétés indiqué par le paramètre _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="5416e-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5416e-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="5416e-119">Return value</span></span>

 <span data-ttu-id="5416e-120">**PpropFindProp** renvoie une structure [SPropValue](spropvalue.md) définissant la propriété qui correspond à la balise de propriété d’entrée, ou NULL si aucune correspondance n’existe.</span><span class="sxs-lookup"><span data-stu-id="5416e-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5416e-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="5416e-121">Remarks</span></span>

<span data-ttu-id="5416e-122">Si la balise de propriété donnée indique une propriété de type PT_UNSPECIFIED, la fonction **PpropFindProp** trouve une correspondance uniquement pour l’identificateur de propriété dans la balise.</span><span class="sxs-lookup"><span data-stu-id="5416e-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="5416e-123">Dans le cas contraire, elle trouve une correspondance pour la balise de propriété entière, y compris le type de propriété et renvoie la propriété identifiée.</span><span class="sxs-lookup"><span data-stu-id="5416e-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5416e-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5416e-124">MFCMAPI reference</span></span>

<span data-ttu-id="5416e-125">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5416e-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5416e-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5416e-126">**File**</span></span>|<span data-ttu-id="5416e-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5416e-127">**Function**</span></span>|<span data-ttu-id="5416e-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5416e-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5416e-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="5416e-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5416e-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="5416e-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="5416e-131">MFCMAPI utilise la méthode **PpropFindProp** pour rechercher des propriétés dans une propriété définie en cours d’ajout à la liste.</span><span class="sxs-lookup"><span data-stu-id="5416e-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5416e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5416e-132">See also</span></span>



[<span data-ttu-id="5416e-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5416e-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

