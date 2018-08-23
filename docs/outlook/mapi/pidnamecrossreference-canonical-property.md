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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5daf8c1ee249cfc7fb1bc1ffb6dfc68b400fe953
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571128"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="50cf4-103">Propriété canonique PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="50cf4-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="50cf4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50cf4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50cf4-105">Contient une valeur de champ d’en-tête référence croisée [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="50cf4-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50cf4-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="50cf4-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="50cf4-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="50cf4-107">None</span></span>  <br/> |
|<span data-ttu-id="50cf4-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="50cf4-108">Property set:</span></span>  <br/> |<span data-ttu-id="50cf4-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="50cf4-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="50cf4-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="50cf4-110">Property name:</span></span>  <br/> |<span data-ttu-id="50cf4-111">Référence croisée</span><span class="sxs-lookup"><span data-stu-id="50cf4-111">Xref</span></span>  <br/> |
|<span data-ttu-id="50cf4-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="50cf4-112">Data type:</span></span>  <br/> |<span data-ttu-id="50cf4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50cf4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="50cf4-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="50cf4-114">Area:</span></span>  <br/> |<span data-ttu-id="50cf4-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="50cf4-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50cf4-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="50cf4-116">Remarks</span></span>

<span data-ttu-id="50cf4-117">Pour définir la valeur de cette propriété, clients Message Extensions MIME (Multipurpose Internet) doivent écrire la valeur souhaitée dans un champ d’en-tête référence croisée.</span><span class="sxs-lookup"><span data-stu-id="50cf4-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="50cf4-118">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête de référence croisée sur la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="50cf4-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50cf4-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="50cf4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50cf4-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="50cf4-120">Protocol specifications</span></span>

<span data-ttu-id="50cf4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50cf4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50cf4-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="50cf4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50cf4-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50cf4-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50cf4-124">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="50cf4-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50cf4-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="50cf4-125">Header files</span></span>

<span data-ttu-id="50cf4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50cf4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="50cf4-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="50cf4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50cf4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50cf4-128">See also</span></span>



[<span data-ttu-id="50cf4-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="50cf4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50cf4-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="50cf4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50cf4-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="50cf4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50cf4-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="50cf4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

