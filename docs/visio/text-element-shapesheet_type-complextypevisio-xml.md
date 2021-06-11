---
title: Élément Text (ShapeSheet_Type complexType) (Visio XML)
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
# <a name="text-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="7c39c-103">Élément Text (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7c39c-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7c39c-104">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="7c39c-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c39c-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="7c39c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c39c-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="7c39c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7c39c-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="7c39c-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7c39c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c39c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7c39c-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7c39c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7c39c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7c39c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7c39c-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="7c39c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7c39c-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="7c39c-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c39c-113">Définition</span><span class="sxs-lookup"><span data-stu-id="7c39c-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c39c-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7c39c-114">Elements and attributes</span></span>

<span data-ttu-id="7c39c-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="7c39c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7c39c-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7c39c-116">Parent elements</span></span>

|<span data-ttu-id="7c39c-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7c39c-117">**Element**</span></span>|<span data-ttu-id="7c39c-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="7c39c-118">**Type**</span></span>|<span data-ttu-id="7c39c-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="7c39c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c39c-120">Forme</span><span class="sxs-lookup"><span data-stu-id="7c39c-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c39c-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="7c39c-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c39c-122">Contient des éléments qui définissent une forme dans un **élément de forme de** groupe, page ou maître. </span><span class="sxs-lookup"><span data-stu-id="7c39c-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7c39c-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7c39c-123">Child elements</span></span>

|<span data-ttu-id="7c39c-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7c39c-124">**Element**</span></span>|<span data-ttu-id="7c39c-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="7c39c-125">**Type**</span></span>|<span data-ttu-id="7c39c-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="7c39c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c39c-127">cp</span><span class="sxs-lookup"><span data-stu-id="7c39c-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c39c-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="7c39c-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c39c-129">Marque le début d’une exécute de propriétés de caractères mise en forme en fonction de l’élément Char correspondant.</span><span class="sxs-lookup"><span data-stu-id="7c39c-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="7c39c-130">fld</span><span class="sxs-lookup"><span data-stu-id="7c39c-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c39c-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="7c39c-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c39c-132">Indique un point d’insertion de champ de texte pour l’élément Field correspondant.</span><span class="sxs-lookup"><span data-stu-id="7c39c-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="7c39c-133">pp</span><span class="sxs-lookup"><span data-stu-id="7c39c-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c39c-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="7c39c-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c39c-135">Spécifie le début d’une exécute de propriétés de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="7c39c-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="7c39c-136">tp</span><span class="sxs-lookup"><span data-stu-id="7c39c-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c39c-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="7c39c-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c39c-138">Spécifie le début d’une utilisation des propriétés d’onglets.</span><span class="sxs-lookup"><span data-stu-id="7c39c-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7c39c-139">Attributs</span><span class="sxs-lookup"><span data-stu-id="7c39c-139">Attributes</span></span>

<span data-ttu-id="7c39c-140">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7c39c-140">None.</span></span>
  

