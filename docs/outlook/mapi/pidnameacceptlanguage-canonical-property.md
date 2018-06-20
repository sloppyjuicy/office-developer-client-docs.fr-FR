---
title: Propriété canonique PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d2c2fb31b722e76034b08077632c817d6adde802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785547"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="14d65-103">Propriété canonique PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="14d65-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="14d65-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14d65-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14d65-105">Contient une valeur de champ d’en-tête Accept-Language [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="14d65-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14d65-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="14d65-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="14d65-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="14d65-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="14d65-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="14d65-108">Property set:</span></span>  <br/> |<span data-ttu-id="14d65-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="14d65-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="14d65-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="14d65-110">Property name:</span></span>  <br/> |<span data-ttu-id="14d65-111">Langue acceptée</span><span class="sxs-lookup"><span data-stu-id="14d65-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="14d65-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="14d65-112">Data type:</span></span>  <br/> |<span data-ttu-id="14d65-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="14d65-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="14d65-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="14d65-114">Area:</span></span>  <br/> |<span data-ttu-id="14d65-115">Courier électronique</span><span class="sxs-lookup"><span data-stu-id="14d65-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14d65-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="14d65-116">Remarks</span></span>

<span data-ttu-id="14d65-117">Pour définir la valeur de cette propriété, les clients Message Extensions MIME (Multipurpose Internet) doivent écrire un champ d’en-tête Accept-Language avec la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="14d65-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="14d65-118">Clients MIME peuvent écrire un champ d’en-tête X-Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="14d65-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="14d65-119">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête à la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="14d65-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="14d65-120">Si les deux champs d’en-tête sont présentes, lecteurs MIME doivent utiliser le champ d’en-tête Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="14d65-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14d65-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="14d65-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14d65-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="14d65-122">Protocol specifications</span></span>

<span data-ttu-id="14d65-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14d65-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14d65-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="14d65-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14d65-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14d65-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14d65-126">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="14d65-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14d65-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="14d65-127">Header files</span></span>

<span data-ttu-id="14d65-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14d65-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="14d65-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="14d65-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14d65-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14d65-130">See also</span></span>



[<span data-ttu-id="14d65-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="14d65-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14d65-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="14d65-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14d65-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="14d65-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14d65-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="14d65-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

