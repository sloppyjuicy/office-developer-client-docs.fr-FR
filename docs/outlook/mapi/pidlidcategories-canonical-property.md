---
title: Propri t canonique PidLidCategories
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344974"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="8fd08-103">Propri t canonique PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="8fd08-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="8fd08-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fd08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fd08-105">Spécifie une liste de catégories pour un élément.</span><span class="sxs-lookup"><span data-stu-id="8fd08-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8fd08-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8fd08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8fd08-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="8fd08-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="8fd08-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="8fd08-108">Property set:</span></span>  <br/> |<span data-ttu-id="8fd08-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="8fd08-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="8fd08-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="8fd08-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8fd08-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="8fd08-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="8fd08-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8fd08-112">Data type:</span></span>  <br/> |<span data-ttu-id="8fd08-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8fd08-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8fd08-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8fd08-114">Area:</span></span>  <br/> |<span data-ttu-id="8fd08-115">Courant</span><span class="sxs-lookup"><span data-stu-id="8fd08-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fd08-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="8fd08-116">Remarks</span></span>

<span data-ttu-id="8fd08-117">Pour générer un champ d’en-tête de mots clés, les clients doivent définir la valeur de cette propriété sur les valeurs souhaitées.</span><span class="sxs-lookup"><span data-stu-id="8fd08-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="8fd08-118">Cette propriété possède plusieurs chaînes ; chaque catégorie doit être mappée à un mot clé unique.</span><span class="sxs-lookup"><span data-stu-id="8fd08-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="8fd08-119">Les rédacteurs MIME (Multipurpose Internet Mail Extensions) doivent copier chaque sous-valeur de cette propriété dans un mot clé distinct dans le champ d’en-tête Keywords, avec une virgule (U+002C) et un espace (U+0020) séparant chaque mot clé.</span><span class="sxs-lookup"><span data-stu-id="8fd08-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="8fd08-120">Les rédacteurs MIME peuvent abandonner cette propriété au lieu de la copier dans le champ d’en-tête des mots clés, afin d’éviter tout conflit entre différents ensembles de catégories dans différentes organisations.</span><span class="sxs-lookup"><span data-stu-id="8fd08-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8fd08-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8fd08-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8fd08-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8fd08-122">Protocol specifications</span></span>

<span data-ttu-id="8fd08-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fd08-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fd08-124">Fournit une définition de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="8fd08-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8fd08-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8fd08-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8fd08-126">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="8fd08-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8fd08-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8fd08-127">Header files</span></span>

<span data-ttu-id="8fd08-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8fd08-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8fd08-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8fd08-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fd08-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fd08-130">See also</span></span>



[<span data-ttu-id="8fd08-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8fd08-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8fd08-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8fd08-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8fd08-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8fd08-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8fd08-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8fd08-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

