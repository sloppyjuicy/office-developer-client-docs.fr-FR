---
title: Text, élément (ShapeSheet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contient le texte d’une forme.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385913"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="e08c9-103">Text, élément (ShapeSheet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e08c9-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e08c9-104">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="e08c9-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e08c9-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="e08c9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e08c9-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e08c9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e08c9-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="e08c9-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e08c9-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e08c9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e08c9-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e08c9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e08c9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e08c9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e08c9-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e08c9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e08c9-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="e08c9-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e08c9-113">Définition</span><span class="sxs-lookup"><span data-stu-id="e08c9-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e08c9-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e08c9-114">Elements and attributes</span></span>

<span data-ttu-id="e08c9-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e08c9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e08c9-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e08c9-116">Parent elements</span></span>

|<span data-ttu-id="e08c9-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e08c9-117">**Element**</span></span>|<span data-ttu-id="e08c9-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="e08c9-118">**Type**</span></span>|<span data-ttu-id="e08c9-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e08c9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e08c9-120">Forme</span><span class="sxs-lookup"><span data-stu-id="e08c9-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e08c9-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e08c9-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e08c9-122">Contient des éléments qui définissent une forme dans une **forme de base**, **Page**ou élément de forme de groupe.</span><span class="sxs-lookup"><span data-stu-id="e08c9-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e08c9-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e08c9-123">Child elements</span></span>

|<span data-ttu-id="e08c9-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e08c9-124">**Element**</span></span>|<span data-ttu-id="e08c9-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="e08c9-125">**Type**</span></span>|<span data-ttu-id="e08c9-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="e08c9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e08c9-127">CP</span><span class="sxs-lookup"><span data-stu-id="e08c9-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e08c9-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="e08c9-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e08c9-129">Marque le début de des propriétés de caractère exécuter qui est mis en forme en fonction de l’élément de caractère correspondant.</span><span class="sxs-lookup"><span data-stu-id="e08c9-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="e08c9-130">chp</span><span class="sxs-lookup"><span data-stu-id="e08c9-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e08c9-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="e08c9-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e08c9-132">Indique un point d’insertion de champs de texte pour l’élément de champ correspondant.</span><span class="sxs-lookup"><span data-stu-id="e08c9-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="e08c9-133">PP</span><span class="sxs-lookup"><span data-stu-id="e08c9-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e08c9-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="e08c9-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e08c9-135">Indique le début de des propriétés de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="e08c9-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="e08c9-136">TP</span><span class="sxs-lookup"><span data-stu-id="e08c9-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e08c9-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="e08c9-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e08c9-138">Spécifie le début d’un propriétés onglets exécuter.</span><span class="sxs-lookup"><span data-stu-id="e08c9-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e08c9-139">Attributs</span><span class="sxs-lookup"><span data-stu-id="e08c9-139">Attributes</span></span>

<span data-ttu-id="e08c9-140">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e08c9-140">None.</span></span>
  

