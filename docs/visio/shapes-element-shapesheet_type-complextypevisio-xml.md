---
title: Élément Shapes (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contient une collection d'éléments Shape.
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348250"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="f4937-103">Élément Shapes (ShapeSheet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f4937-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f4937-104">Contient une collection d'éléments Shape.</span><span class="sxs-lookup"><span data-stu-id="f4937-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4937-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="f4937-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4937-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="f4937-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f4937-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="f4937-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f4937-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f4937-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f4937-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f4937-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f4937-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f4937-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f4937-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="f4937-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f4937-112">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="f4937-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4937-113">Définition</span><span class="sxs-lookup"><span data-stu-id="f4937-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f4937-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f4937-114">Elements and attributes</span></span>

<span data-ttu-id="f4937-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="f4937-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f4937-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f4937-116">Parent elements</span></span>

|<span data-ttu-id="f4937-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f4937-117">**Element**</span></span>|<span data-ttu-id="f4937-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="f4937-118">**Type**</span></span>|<span data-ttu-id="f4937-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4937-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4937-120">Forme</span><span class="sxs-lookup"><span data-stu-id="f4937-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f4937-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f4937-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f4937-122">Spécifie une collection de propriétés associée à une forme.</span><span class="sxs-lookup"><span data-stu-id="f4937-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f4937-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f4937-123">Child elements</span></span>

|<span data-ttu-id="f4937-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f4937-124">**Element**</span></span>|<span data-ttu-id="f4937-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="f4937-125">**Type**</span></span>|<span data-ttu-id="f4937-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4937-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4937-127">Forme</span><span class="sxs-lookup"><span data-stu-id="f4937-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f4937-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f4937-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f4937-129">Contient des éléments qui définissent une forme dans un élément de forme de forme de **base**, de **page**ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="f4937-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f4937-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="f4937-130">Attributes</span></span>

<span data-ttu-id="f4937-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f4937-131">None.</span></span>
  

