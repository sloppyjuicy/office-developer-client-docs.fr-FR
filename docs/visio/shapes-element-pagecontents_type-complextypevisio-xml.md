---
title: Élément Shapes (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contient une collection d’éléments Shape.
ms.openlocfilehash: 5d248dd2683a1ccc153d15477c888e1b13d24d0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542120"
---
# <a name="shapes-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="c6ee0-103">Élément Shapes (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c6ee0-103">Shapes element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c6ee0-104">Contient une collection d’éléments Shape.</span><span class="sxs-lookup"><span data-stu-id="c6ee0-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6ee0-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="c6ee0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6ee0-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c6ee0-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="c6ee0-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c6ee0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c6ee0-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c6ee0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c6ee0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c6ee0-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c6ee0-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="c6ee0-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c6ee0-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c6ee0-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c6ee0-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c6ee0-114">Elements and attributes</span></span>

<span data-ttu-id="c6ee0-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c6ee0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c6ee0-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c6ee0-116">Parent elements</span></span>

|<span data-ttu-id="c6ee0-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-117">**Element**</span></span>|<span data-ttu-id="c6ee0-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-118">**Type**</span></span>|<span data-ttu-id="c6ee0-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6ee0-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="c6ee0-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c6ee0-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c6ee0-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6ee0-122">Spécifie des informations sur les formes d’une forme de base dans un dessin Web.</span><span class="sxs-lookup"><span data-stu-id="c6ee0-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="c6ee0-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="c6ee0-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c6ee0-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c6ee0-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6ee0-125">Spécifie des informations sur les formes d’une forme de base dans un dessin Web.</span><span class="sxs-lookup"><span data-stu-id="c6ee0-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c6ee0-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c6ee0-126">Child elements</span></span>

|<span data-ttu-id="c6ee0-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-127">**Element**</span></span>|<span data-ttu-id="c6ee0-128">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-128">**Type**</span></span>|<span data-ttu-id="c6ee0-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="c6ee0-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6ee0-130">Forme</span><span class="sxs-lookup"><span data-stu-id="c6ee0-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c6ee0-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c6ee0-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6ee0-132">Contient des éléments qui définissent une forme dans un **élément de forme de** groupe, page ou maître. </span><span class="sxs-lookup"><span data-stu-id="c6ee0-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c6ee0-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6ee0-133">Attributes</span></span>

<span data-ttu-id="c6ee0-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c6ee0-134">None.</span></span>
  

