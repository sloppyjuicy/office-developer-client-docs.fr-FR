---
title: Élément de formes (PageContents_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contient une collection d’éléments de la forme.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397568"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="bcf84-103">Élément de formes (PageContents_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="bcf84-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="bcf84-104">Contient une collection d’éléments de la forme.</span><span class="sxs-lookup"><span data-stu-id="bcf84-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bcf84-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="bcf84-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcf84-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="bcf84-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bcf84-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="bcf84-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bcf84-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="bcf84-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bcf84-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="bcf84-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bcf84-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bcf84-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bcf84-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="bcf84-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bcf84-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="bcf84-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bcf84-113">Définition</span><span class="sxs-lookup"><span data-stu-id="bcf84-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bcf84-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="bcf84-114">Elements and attributes</span></span>

<span data-ttu-id="bcf84-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="bcf84-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bcf84-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bcf84-116">Parent elements</span></span>

|<span data-ttu-id="bcf84-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="bcf84-117">**Element**</span></span>|<span data-ttu-id="bcf84-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="bcf84-118">**Type**</span></span>|<span data-ttu-id="bcf84-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="bcf84-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bcf84-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="bcf84-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="bcf84-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="bcf84-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bcf84-122">Spécifie des informations sur les formes dans une forme de base dans un dessin Web.</span><span class="sxs-lookup"><span data-stu-id="bcf84-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="bcf84-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="bcf84-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="bcf84-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="bcf84-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bcf84-125">Spécifie des informations sur les formes dans une forme de base dans un dessin Web.</span><span class="sxs-lookup"><span data-stu-id="bcf84-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bcf84-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bcf84-126">Child elements</span></span>

|<span data-ttu-id="bcf84-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="bcf84-127">**Element**</span></span>|<span data-ttu-id="bcf84-128">**Type**</span><span class="sxs-lookup"><span data-stu-id="bcf84-128">**Type**</span></span>|<span data-ttu-id="bcf84-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="bcf84-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bcf84-130">Forme</span><span class="sxs-lookup"><span data-stu-id="bcf84-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bcf84-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="bcf84-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bcf84-132">Contient des éléments qui définissent une forme dans une **forme de base**, **Page**ou élément de forme de groupe.</span><span class="sxs-lookup"><span data-stu-id="bcf84-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bcf84-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="bcf84-133">Attributes</span></span>

<span data-ttu-id="bcf84-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bcf84-134">None.</span></span>
  

