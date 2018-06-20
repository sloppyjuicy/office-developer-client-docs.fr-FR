---
title: Élément de formes (ShapeSheet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contient une collection d’éléments de la forme.
ms.openlocfilehash: d2e725a28873cac8dded49587a98400df1d9bf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789673"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="ccb25-103">Élément de formes (ShapeSheet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ccb25-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ccb25-104">Contient une collection d’éléments de la forme.</span><span class="sxs-lookup"><span data-stu-id="ccb25-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccb25-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="ccb25-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccb25-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ccb25-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ccb25-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="ccb25-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ccb25-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ccb25-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ccb25-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ccb25-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ccb25-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ccb25-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ccb25-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ccb25-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ccb25-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="ccb25-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ccb25-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ccb25-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ccb25-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ccb25-114">Elements and attributes</span></span>

<span data-ttu-id="ccb25-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ccb25-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ccb25-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ccb25-116">Parent elements</span></span>

|<span data-ttu-id="ccb25-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ccb25-117">**Element**</span></span>|<span data-ttu-id="ccb25-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ccb25-118">**Type**</span></span>|<span data-ttu-id="ccb25-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ccb25-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ccb25-120">Forme</span><span class="sxs-lookup"><span data-stu-id="ccb25-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ccb25-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ccb25-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ccb25-122">Spécifie une collection de propriétés associées à une forme.</span><span class="sxs-lookup"><span data-stu-id="ccb25-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ccb25-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ccb25-123">Child elements</span></span>

|<span data-ttu-id="ccb25-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ccb25-124">**Element**</span></span>|<span data-ttu-id="ccb25-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="ccb25-125">**Type**</span></span>|<span data-ttu-id="ccb25-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="ccb25-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ccb25-127">Forme</span><span class="sxs-lookup"><span data-stu-id="ccb25-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ccb25-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ccb25-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ccb25-129">Contient des éléments qui définissent une forme dans une **forme de base**, **Page**ou élément de forme de groupe.</span><span class="sxs-lookup"><span data-stu-id="ccb25-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ccb25-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="ccb25-130">Attributes</span></span>

<span data-ttu-id="ccb25-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ccb25-131">None.</span></span>
  

