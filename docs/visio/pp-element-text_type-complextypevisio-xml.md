---
title: élément PP (Text_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Indique le début de des propriétés de paragraphe. L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.
ms.openlocfilehash: ce1bdd89ca9a5eb5b7ce9b73cc2354ccfde1c125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789334"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="0c54a-104">élément PP (Text_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0c54a-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0c54a-105">Indique le début de des propriétés de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="0c54a-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="0c54a-106">L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="0c54a-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c54a-107">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="0c54a-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c54a-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0c54a-108">**Element type**</span></span> <br/> |[<span data-ttu-id="0c54a-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="0c54a-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0c54a-110">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0c54a-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0c54a-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0c54a-111">**Schema file**</span></span> <br/> |<span data-ttu-id="0c54a-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0c54a-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0c54a-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="0c54a-113">**Document parts**</span></span> <br/> |<span data-ttu-id="0c54a-114">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="0c54a-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c54a-115">Définition</span><span class="sxs-lookup"><span data-stu-id="0c54a-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0c54a-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0c54a-116">Elements and attributes</span></span>

<span data-ttu-id="0c54a-117">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0c54a-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0c54a-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0c54a-118">Parent elements</span></span>

|<span data-ttu-id="0c54a-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0c54a-119">**Element**</span></span>|<span data-ttu-id="0c54a-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="0c54a-120">**Type**</span></span>|<span data-ttu-id="0c54a-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c54a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0c54a-122">Text</span><span class="sxs-lookup"><span data-stu-id="0c54a-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c54a-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="0c54a-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0c54a-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="0c54a-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0c54a-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0c54a-125">Child elements</span></span>

<span data-ttu-id="0c54a-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0c54a-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c54a-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="0c54a-127">Attributes</span></span>

|<span data-ttu-id="0c54a-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0c54a-128">**Attribute**</span></span>|<span data-ttu-id="0c54a-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="0c54a-129">**Type**</span></span>|<span data-ttu-id="0c54a-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0c54a-130">**Required**</span></span>|<span data-ttu-id="0c54a-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c54a-131">**Description**</span></span>|<span data-ttu-id="0c54a-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0c54a-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c54a-133">IX</span><span class="sxs-lookup"><span data-stu-id="0c54a-133">IX</span></span>  <br/> |<span data-ttu-id="0c54a-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c54a-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c54a-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0c54a-135">required</span></span>  <br/> |<span data-ttu-id="0c54a-136">L’index de l’élément de **paragraphe** qui spécifie la mise en forme appliquée à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0c54a-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="0c54a-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0c54a-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

