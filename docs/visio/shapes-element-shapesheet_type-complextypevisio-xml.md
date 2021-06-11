---
title: Élément Shapes (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contient une collection d’éléments Shape.
ms.openlocfilehash: e9f45d1f61b83339274d24aea2c0473adf282bac
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542099"
---
# <a name="shapes-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="82ce6-103">Élément Shapes (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="82ce6-103">Shapes element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="82ce6-104">Contient une collection d’éléments Shape.</span><span class="sxs-lookup"><span data-stu-id="82ce6-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82ce6-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="82ce6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82ce6-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="82ce6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="82ce6-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="82ce6-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="82ce6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="82ce6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="82ce6-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="82ce6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="82ce6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="82ce6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="82ce6-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="82ce6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="82ce6-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="82ce6-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="82ce6-113">Définition</span><span class="sxs-lookup"><span data-stu-id="82ce6-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="82ce6-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="82ce6-114">Elements and attributes</span></span>

<span data-ttu-id="82ce6-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="82ce6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="82ce6-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="82ce6-116">Parent elements</span></span>

|<span data-ttu-id="82ce6-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="82ce6-117">**Element**</span></span>|<span data-ttu-id="82ce6-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="82ce6-118">**Type**</span></span>|<span data-ttu-id="82ce6-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="82ce6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82ce6-120">Forme</span><span class="sxs-lookup"><span data-stu-id="82ce6-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82ce6-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="82ce6-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="82ce6-122">Spécifie une collection de propriétés associées à une forme.</span><span class="sxs-lookup"><span data-stu-id="82ce6-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="82ce6-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="82ce6-123">Child elements</span></span>

|<span data-ttu-id="82ce6-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="82ce6-124">**Element**</span></span>|<span data-ttu-id="82ce6-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="82ce6-125">**Type**</span></span>|<span data-ttu-id="82ce6-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="82ce6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82ce6-127">Forme</span><span class="sxs-lookup"><span data-stu-id="82ce6-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82ce6-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="82ce6-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="82ce6-129">Contient des éléments qui définissent une forme dans un **élément de forme de** groupe, page ou maître. </span><span class="sxs-lookup"><span data-stu-id="82ce6-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="82ce6-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="82ce6-130">Attributes</span></span>

<span data-ttu-id="82ce6-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="82ce6-131">None.</span></span>
  

