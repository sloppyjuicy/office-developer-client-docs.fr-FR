---
title: Text, élément (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contient le texte d’une forme.
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541924"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="6998b-103">Text, élément (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6998b-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6998b-104">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="6998b-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6998b-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="6998b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6998b-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="6998b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6998b-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="6998b-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6998b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6998b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6998b-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6998b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6998b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6998b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6998b-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="6998b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6998b-112">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="6998b-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6998b-113">Définition</span><span class="sxs-lookup"><span data-stu-id="6998b-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6998b-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6998b-114">Elements and attributes</span></span>

<span data-ttu-id="6998b-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="6998b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6998b-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6998b-116">Parent elements</span></span>

|<span data-ttu-id="6998b-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6998b-117">**Element**</span></span>|<span data-ttu-id="6998b-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="6998b-118">**Type**</span></span>|<span data-ttu-id="6998b-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="6998b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6998b-120">Forme</span><span class="sxs-lookup"><span data-stu-id="6998b-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6998b-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6998b-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6998b-122">Contient des éléments qui définissent une forme dans un élément de forme de forme de **base**, de **page**ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="6998b-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6998b-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6998b-123">Child elements</span></span>

|<span data-ttu-id="6998b-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6998b-124">**Element**</span></span>|<span data-ttu-id="6998b-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="6998b-125">**Type**</span></span>|<span data-ttu-id="6998b-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="6998b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6998b-127">revendications</span><span class="sxs-lookup"><span data-stu-id="6998b-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6998b-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="6998b-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6998b-129">Marque le début d’une exécution de propriétés de caractère qui est mise en forme en fonction de l’élément char correspondant.</span><span class="sxs-lookup"><span data-stu-id="6998b-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="6998b-130">FLD</span><span class="sxs-lookup"><span data-stu-id="6998b-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6998b-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="6998b-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6998b-132">Indique un point d’insertion de champ de texte pour l’élément Field correspondant.</span><span class="sxs-lookup"><span data-stu-id="6998b-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="6998b-133">po</span><span class="sxs-lookup"><span data-stu-id="6998b-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6998b-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="6998b-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6998b-135">Indique le début des propriétés de paragraphe exécutées.</span><span class="sxs-lookup"><span data-stu-id="6998b-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="6998b-136">partenaire</span><span class="sxs-lookup"><span data-stu-id="6998b-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6998b-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="6998b-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6998b-138">Indique le début d’une propriété Tabs.</span><span class="sxs-lookup"><span data-stu-id="6998b-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6998b-139">Attributs</span><span class="sxs-lookup"><span data-stu-id="6998b-139">Attributes</span></span>

<span data-ttu-id="6998b-140">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6998b-140">None.</span></span>
  

