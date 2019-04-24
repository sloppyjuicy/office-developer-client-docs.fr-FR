---
title: Élément Shapes (PageContents_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contient une collection d'éléments Shape.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349167"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="8a7fa-103">Élément Shapes (PageContents_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8a7fa-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8a7fa-104">Contient une collection d'éléments Shape.</span><span class="sxs-lookup"><span data-stu-id="8a7fa-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a7fa-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="8a7fa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a7fa-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8a7fa-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="8a7fa-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8a7fa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8a7fa-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8a7fa-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8a7fa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8a7fa-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8a7fa-112">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="8a7fa-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8a7fa-113">Définition</span><span class="sxs-lookup"><span data-stu-id="8a7fa-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8a7fa-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="8a7fa-114">Elements and attributes</span></span>

<span data-ttu-id="8a7fa-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="8a7fa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8a7fa-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8a7fa-116">Parent elements</span></span>

|<span data-ttu-id="8a7fa-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-117">**Element**</span></span>|<span data-ttu-id="8a7fa-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-118">**Type**</span></span>|<span data-ttu-id="8a7fa-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8a7fa-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="8a7fa-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="8a7fa-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="8a7fa-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a7fa-122">Cette énumération spécifie les informations relatives aux formes d'une forme de base dans un dessin Web.</span><span class="sxs-lookup"><span data-stu-id="8a7fa-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="8a7fa-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="8a7fa-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="8a7fa-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="8a7fa-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a7fa-125">Cette énumération spécifie les informations relatives aux formes d'une forme de base dans un dessin Web.</span><span class="sxs-lookup"><span data-stu-id="8a7fa-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8a7fa-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8a7fa-126">Child elements</span></span>

|<span data-ttu-id="8a7fa-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-127">**Element**</span></span>|<span data-ttu-id="8a7fa-128">**Type**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-128">**Type**</span></span>|<span data-ttu-id="8a7fa-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a7fa-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8a7fa-130">Forme</span><span class="sxs-lookup"><span data-stu-id="8a7fa-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a7fa-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="8a7fa-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a7fa-132">Contient des éléments qui définissent une forme dans un élément de forme de forme de **base**, de **page**ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="8a7fa-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8a7fa-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="8a7fa-133">Attributes</span></span>

<span data-ttu-id="8a7fa-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8a7fa-134">None.</span></span>
  

