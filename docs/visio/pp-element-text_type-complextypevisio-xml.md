---
title: pp, élément (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Indique le début des propriétés de paragraphe exécutées. L'exécution est définie à la fin du texte ou jusqu'à la balise suivante.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356076"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="3dea4-104">pp, élément (Text_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="3dea4-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3dea4-105">Indique le début des propriétés de paragraphe exécutées.</span><span class="sxs-lookup"><span data-stu-id="3dea4-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="3dea4-106">L'exécution est définie à la fin du texte ou jusqu'à la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="3dea4-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3dea4-107">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="3dea4-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3dea4-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="3dea4-108">**Element type**</span></span> <br/> |[<span data-ttu-id="3dea4-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="3dea4-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3dea4-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3dea4-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3dea4-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3dea4-111">**Schema file**</span></span> <br/> |<span data-ttu-id="3dea4-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3dea4-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3dea4-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="3dea4-113">**Document parts**</span></span> <br/> |<span data-ttu-id="3dea4-114">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="3dea4-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3dea4-115">Définition</span><span class="sxs-lookup"><span data-stu-id="3dea4-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3dea4-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3dea4-116">Elements and attributes</span></span>

<span data-ttu-id="3dea4-117">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="3dea4-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3dea4-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3dea4-118">Parent elements</span></span>

|<span data-ttu-id="3dea4-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3dea4-119">**Element**</span></span>|<span data-ttu-id="3dea4-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="3dea4-120">**Type**</span></span>|<span data-ttu-id="3dea4-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="3dea4-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3dea4-122">Text</span><span class="sxs-lookup"><span data-stu-id="3dea4-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3dea4-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="3dea4-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3dea4-124">Contient le texte d'une forme.</span><span class="sxs-lookup"><span data-stu-id="3dea4-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3dea4-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3dea4-125">Child elements</span></span>

<span data-ttu-id="3dea4-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3dea4-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3dea4-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="3dea4-127">Attributes</span></span>

|<span data-ttu-id="3dea4-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3dea4-128">**Attribute**</span></span>|<span data-ttu-id="3dea4-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="3dea4-129">**Type**</span></span>|<span data-ttu-id="3dea4-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3dea4-130">**Required**</span></span>|<span data-ttu-id="3dea4-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="3dea4-131">**Description**</span></span>|<span data-ttu-id="3dea4-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="3dea4-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3dea4-133">IX</span><span class="sxs-lookup"><span data-stu-id="3dea4-133">IX</span></span>  <br/> |<span data-ttu-id="3dea4-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3dea4-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3dea4-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="3dea4-135">required</span></span>  <br/> |<span data-ttu-id="3dea4-136">Index de l'élément **para** qui spécifie la mise en forme appliquée à cette exécution.</span><span class="sxs-lookup"><span data-stu-id="3dea4-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="3dea4-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3dea4-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

