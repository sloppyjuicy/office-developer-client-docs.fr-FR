---
title: Propriété canonique PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785086"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="9c66f-103">Propriété canonique PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="9c66f-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="9c66f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c66f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c66f-105">Spécifie une liste de catégories pour un élément.</span><span class="sxs-lookup"><span data-stu-id="9c66f-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c66f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9c66f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c66f-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="9c66f-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="9c66f-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="9c66f-108">Property set:</span></span>  <br/> |<span data-ttu-id="9c66f-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="9c66f-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="9c66f-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="9c66f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9c66f-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="9c66f-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="9c66f-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9c66f-112">Data type:</span></span>  <br/> |<span data-ttu-id="9c66f-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c66f-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9c66f-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="9c66f-114">Area:</span></span>  <br/> |<span data-ttu-id="9c66f-115">Common</span><span class="sxs-lookup"><span data-stu-id="9c66f-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c66f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="9c66f-116">Remarks</span></span>

<span data-ttu-id="9c66f-117">Pour générer un champ d’en-tête de mots clés, les clients doivent définir la valeur de cette propriété avec les valeurs souhaitées.</span><span class="sxs-lookup"><span data-stu-id="9c66f-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="9c66f-118">Cette propriété a plusieurs chaînes ; chaque catégorie doit être mappé à un mot clé unique.</span><span class="sxs-lookup"><span data-stu-id="9c66f-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="9c66f-119">Les auteurs Multipurpose Internet Mail Extensions (MIME) doivent copier chaque valeur sous-sites de cette propriété à un mot clé distinct dans le champ en-tête de mots clés, avec une virgule (U + 002 C) et espace (U + 0020) séparant chaque mot clé.</span><span class="sxs-lookup"><span data-stu-id="9c66f-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="9c66f-120">Rédacteurs MIME peuvent supprimer cette propriété au lieu de la copier dans le champ en-tête de mots clés, afin d’éviter les conflits entre les différentes catégories dans différentes organisations.</span><span class="sxs-lookup"><span data-stu-id="9c66f-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c66f-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9c66f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9c66f-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9c66f-122">Protocol specifications</span></span>

<span data-ttu-id="9c66f-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c66f-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c66f-124">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="9c66f-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9c66f-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c66f-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c66f-126">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="9c66f-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9c66f-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9c66f-127">Header files</span></span>

<span data-ttu-id="9c66f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c66f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c66f-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9c66f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c66f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c66f-130">See also</span></span>



[<span data-ttu-id="9c66f-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9c66f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c66f-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9c66f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c66f-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9c66f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c66f-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9c66f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

