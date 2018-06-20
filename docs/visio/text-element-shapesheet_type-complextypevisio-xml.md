---
title: Text, élément (ShapeSheet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contient le texte d’une forme.
ms.openlocfilehash: 636f349b0a93719cd157db563b238147af5584cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789859"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="9ded6-103">Text, élément (ShapeSheet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9ded6-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9ded6-104">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="9ded6-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ded6-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="9ded6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ded6-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="9ded6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9ded6-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="9ded6-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9ded6-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9ded6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9ded6-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9ded6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9ded6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9ded6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9ded6-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="9ded6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9ded6-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="9ded6-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ded6-113">Définition</span><span class="sxs-lookup"><span data-stu-id="9ded6-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ded6-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9ded6-114">Elements and attributes</span></span>

<span data-ttu-id="9ded6-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9ded6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9ded6-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9ded6-116">Parent elements</span></span>

|<span data-ttu-id="9ded6-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9ded6-117">**Element**</span></span>|<span data-ttu-id="9ded6-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="9ded6-118">**Type**</span></span>|<span data-ttu-id="9ded6-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="9ded6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ded6-120">Forme</span><span class="sxs-lookup"><span data-stu-id="9ded6-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ded6-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9ded6-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ded6-122">Contient des éléments qui définissent une forme dans une **forme de base**, **Page**ou élément de forme de groupe.</span><span class="sxs-lookup"><span data-stu-id="9ded6-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9ded6-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9ded6-123">Child elements</span></span>

|<span data-ttu-id="9ded6-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9ded6-124">**Element**</span></span>|<span data-ttu-id="9ded6-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="9ded6-125">**Type**</span></span>|<span data-ttu-id="9ded6-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="9ded6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ded6-127">CP</span><span class="sxs-lookup"><span data-stu-id="9ded6-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ded6-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="9ded6-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ded6-129">Marque le début de des propriétés de caractère exécuter qui est mis en forme en fonction de l’élément de caractère correspondant.</span><span class="sxs-lookup"><span data-stu-id="9ded6-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="9ded6-130">fld</span><span class="sxs-lookup"><span data-stu-id="9ded6-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ded6-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="9ded6-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ded6-132">Indique un point d’insertion de champs de texte pour l’élément de champ correspondant.</span><span class="sxs-lookup"><span data-stu-id="9ded6-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="9ded6-133">PP</span><span class="sxs-lookup"><span data-stu-id="9ded6-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ded6-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="9ded6-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ded6-135">Indique le début de des propriétés de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="9ded6-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="9ded6-136">TP</span><span class="sxs-lookup"><span data-stu-id="9ded6-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ded6-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="9ded6-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ded6-138">Spécifie le début d’un propriétés onglets exécuter.</span><span class="sxs-lookup"><span data-stu-id="9ded6-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9ded6-139">Attributs</span><span class="sxs-lookup"><span data-stu-id="9ded6-139">Attributes</span></span>

<span data-ttu-id="9ded6-140">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9ded6-140">None.</span></span>
  

