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
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344974"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="ed962-103">Propriété canonique PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="ed962-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="ed962-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed962-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed962-105">Spécifie une liste de catégories pour un élément.</span><span class="sxs-lookup"><span data-stu-id="ed962-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed962-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ed962-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed962-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="ed962-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="ed962-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="ed962-108">Property set:</span></span>  <br/> |<span data-ttu-id="ed962-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ed962-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="ed962-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="ed962-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ed962-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="ed962-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="ed962-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ed962-112">Data type:</span></span>  <br/> |<span data-ttu-id="ed962-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed962-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed962-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ed962-114">Area:</span></span>  <br/> |<span data-ttu-id="ed962-115">Courant</span><span class="sxs-lookup"><span data-stu-id="ed962-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed962-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed962-116">Remarks</span></span>

<span data-ttu-id="ed962-117">Pour générer un champ d'en-tête de mots clés, les clients doivent définir la valeur de cette propriété sur les valeurs souhaitées.</span><span class="sxs-lookup"><span data-stu-id="ed962-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="ed962-118">Cette propriété comporte plusieurs chaînes; chaque catégorie doit être mappée à un mot-clé unique.</span><span class="sxs-lookup"><span data-stu-id="ed962-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="ed962-119">Les Writers MIME (Multipurpose Internet Mail Extensions) doivent copier chaque sous-valeur de cette propriété sur un mot clé distinct dans le champ d'en-tête de mots clés, avec une virgule (U + 002C) et un espace (U + 0020) séparant chaque mot clé.</span><span class="sxs-lookup"><span data-stu-id="ed962-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="ed962-120">Les rédacteurs MIME peuvent supprimer cette propriété au lieu de la copier dans le champ d'en-tête Mots clés, afin d'éviter tout conflit entre différents ensembles de catégories dans différentes organisations.</span><span class="sxs-lookup"><span data-stu-id="ed962-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed962-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="ed962-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed962-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ed962-122">Protocol specifications</span></span>

<span data-ttu-id="ed962-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed962-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed962-124">Fournit la définition des jeux de propriétés et les références aux spécifications du protocole Exchange Server associé.</span><span class="sxs-lookup"><span data-stu-id="ed962-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed962-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed962-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed962-126">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="ed962-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed962-127">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="ed962-127">Header files</span></span>

<span data-ttu-id="ed962-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ed962-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed962-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ed962-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed962-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed962-130">See also</span></span>



[<span data-ttu-id="ed962-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ed962-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed962-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ed962-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed962-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ed962-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed962-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ed962-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

