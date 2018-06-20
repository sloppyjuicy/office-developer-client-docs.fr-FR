---
title: Propriété canonique PidNameCrossReference
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 148d71dc0e99e23ffe10445068170617cb26b01b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785595"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="c5430-103">Propriété canonique PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="c5430-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="c5430-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5430-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5430-105">Contient une valeur de champ d’en-tête référence croisée [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="c5430-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5430-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="c5430-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="c5430-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="c5430-107">None</span></span>  <br/> |
|<span data-ttu-id="c5430-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="c5430-108">Property set:</span></span>  <br/> |<span data-ttu-id="c5430-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="c5430-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="c5430-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="c5430-110">Property name:</span></span>  <br/> |<span data-ttu-id="c5430-111">Référence croisée</span><span class="sxs-lookup"><span data-stu-id="c5430-111">Xref</span></span>  <br/> |
|<span data-ttu-id="c5430-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c5430-112">Data type:</span></span>  <br/> |<span data-ttu-id="c5430-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c5430-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c5430-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="c5430-114">Area:</span></span>  <br/> |<span data-ttu-id="c5430-115">Courier électronique</span><span class="sxs-lookup"><span data-stu-id="c5430-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5430-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5430-116">Remarks</span></span>

<span data-ttu-id="c5430-117">Pour définir la valeur de cette propriété, clients Message Extensions MIME (Multipurpose Internet) doivent écrire la valeur souhaitée dans un champ d’en-tête référence croisée.</span><span class="sxs-lookup"><span data-stu-id="c5430-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="c5430-118">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête de référence croisée sur la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c5430-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5430-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c5430-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5430-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c5430-120">Protocol specifications</span></span>

<span data-ttu-id="c5430-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5430-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5430-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="c5430-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5430-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5430-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5430-124">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="c5430-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5430-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c5430-125">Header files</span></span>

<span data-ttu-id="c5430-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5430-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5430-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c5430-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5430-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5430-128">See also</span></span>



[<span data-ttu-id="c5430-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c5430-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5430-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c5430-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5430-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c5430-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5430-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c5430-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

