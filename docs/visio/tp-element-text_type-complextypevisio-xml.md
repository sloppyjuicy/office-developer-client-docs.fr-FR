---
title: élément TP (Text_Type complexType) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Indique le début d’une propriété Tabs. L’exécution est définie à la fin du texte ou jusqu’à la balise suivante.
ms.openlocfilehash: dad7a3de715473a75c601c1e391c9d51fc1cab85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542974"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="0212e-104">élément TP (Text_Type complexType) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="0212e-104">tp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0212e-105">Indique le début d’une propriété Tabs.</span><span class="sxs-lookup"><span data-stu-id="0212e-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="0212e-106">L’exécution est définie à la fin du texte ou jusqu’à la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="0212e-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0212e-107">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="0212e-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0212e-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0212e-108">**Element type**</span></span> <br/> |[<span data-ttu-id="0212e-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="0212e-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0212e-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0212e-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0212e-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0212e-111">**Schema file**</span></span> <br/> |<span data-ttu-id="0212e-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0212e-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0212e-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="0212e-113">**Document parts**</span></span> <br/> |<span data-ttu-id="0212e-114">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="0212e-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0212e-115">Définition</span><span class="sxs-lookup"><span data-stu-id="0212e-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0212e-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0212e-116">Elements and attributes</span></span>

<span data-ttu-id="0212e-117">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="0212e-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0212e-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0212e-118">Parent elements</span></span>

|<span data-ttu-id="0212e-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0212e-119">**Element**</span></span>|<span data-ttu-id="0212e-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="0212e-120">**Type**</span></span>|<span data-ttu-id="0212e-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="0212e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0212e-122">Text</span><span class="sxs-lookup"><span data-stu-id="0212e-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0212e-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="0212e-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0212e-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="0212e-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0212e-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0212e-125">Child elements</span></span>

<span data-ttu-id="0212e-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0212e-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0212e-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="0212e-127">Attributes</span></span>

|<span data-ttu-id="0212e-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0212e-128">**Attribute**</span></span>|<span data-ttu-id="0212e-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="0212e-129">**Type**</span></span>|<span data-ttu-id="0212e-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0212e-130">**Required**</span></span>|<span data-ttu-id="0212e-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="0212e-131">**Description**</span></span>|<span data-ttu-id="0212e-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0212e-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0212e-133">IX</span><span class="sxs-lookup"><span data-stu-id="0212e-133">IX</span></span>  <br/> |<span data-ttu-id="0212e-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0212e-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0212e-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0212e-135">required</span></span>  <br/> |<span data-ttu-id="0212e-136">Index de base zéro de l’élément au sein de son élément parent.</span><span class="sxs-lookup"><span data-stu-id="0212e-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="0212e-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0212e-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

