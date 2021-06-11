---
title: élément tp (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Spécifie le début d’une utilisation des propriétés d’onglets. La suite est définie à la fin du texte ou jusqu’à la balise suivante.
ms.openlocfilehash: dad7a3de715473a75c601c1e391c9d51fc1cab85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542974"
---
# <a name="tp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="a42f8-104">élément tp (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a42f8-104">tp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a42f8-105">Spécifie le début d’une utilisation des propriétés d’onglets.</span><span class="sxs-lookup"><span data-stu-id="a42f8-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="a42f8-106">La suite est définie à la fin du texte ou jusqu’à la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="a42f8-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a42f8-107">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a42f8-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a42f8-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a42f8-108">**Element type**</span></span> <br/> |[<span data-ttu-id="a42f8-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="a42f8-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a42f8-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a42f8-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a42f8-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a42f8-111">**Schema file**</span></span> <br/> |<span data-ttu-id="a42f8-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a42f8-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a42f8-113">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="a42f8-113">**Document parts**</span></span> <br/> |<span data-ttu-id="a42f8-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="a42f8-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a42f8-115">Définition</span><span class="sxs-lookup"><span data-stu-id="a42f8-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a42f8-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a42f8-116">Elements and attributes</span></span>

<span data-ttu-id="a42f8-117">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="a42f8-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a42f8-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a42f8-118">Parent elements</span></span>

|<span data-ttu-id="a42f8-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a42f8-119">**Element**</span></span>|<span data-ttu-id="a42f8-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="a42f8-120">**Type**</span></span>|<span data-ttu-id="a42f8-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="a42f8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a42f8-122">Text</span><span class="sxs-lookup"><span data-stu-id="a42f8-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a42f8-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="a42f8-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a42f8-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="a42f8-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a42f8-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a42f8-125">Child elements</span></span>

<span data-ttu-id="a42f8-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a42f8-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a42f8-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="a42f8-127">Attributes</span></span>

|<span data-ttu-id="a42f8-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a42f8-128">**Attribute**</span></span>|<span data-ttu-id="a42f8-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="a42f8-129">**Type**</span></span>|<span data-ttu-id="a42f8-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a42f8-130">**Required**</span></span>|<span data-ttu-id="a42f8-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="a42f8-131">**Description**</span></span>|<span data-ttu-id="a42f8-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a42f8-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a42f8-133">IX</span><span class="sxs-lookup"><span data-stu-id="a42f8-133">IX</span></span>  <br/> |<span data-ttu-id="a42f8-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a42f8-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a42f8-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a42f8-135">required</span></span>  <br/> |<span data-ttu-id="a42f8-136">Index de base 0 de l’élément au sein de son élément parent.</span><span class="sxs-lookup"><span data-stu-id="a42f8-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="a42f8-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a42f8-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

