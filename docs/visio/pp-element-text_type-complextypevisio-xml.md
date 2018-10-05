---
title: élément PP (Text_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Indique le début de des propriétés de paragraphe. L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400099"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="17994-104">élément PP (Text_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="17994-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="17994-105">Indique le début de des propriétés de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="17994-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="17994-106">L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="17994-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17994-107">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="17994-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17994-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="17994-108">**Element type**</span></span> <br/> |[<span data-ttu-id="17994-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="17994-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="17994-110">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="17994-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="17994-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="17994-111">**Schema file**</span></span> <br/> |<span data-ttu-id="17994-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="17994-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="17994-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="17994-113">**Document parts**</span></span> <br/> |<span data-ttu-id="17994-114">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="17994-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17994-115">Définition</span><span class="sxs-lookup"><span data-stu-id="17994-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17994-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="17994-116">Elements and attributes</span></span>

<span data-ttu-id="17994-117">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="17994-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17994-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="17994-118">Parent elements</span></span>

|<span data-ttu-id="17994-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="17994-119">**Element**</span></span>|<span data-ttu-id="17994-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="17994-120">**Type**</span></span>|<span data-ttu-id="17994-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="17994-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17994-122">Text</span><span class="sxs-lookup"><span data-stu-id="17994-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17994-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="17994-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17994-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="17994-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17994-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17994-125">Child elements</span></span>

<span data-ttu-id="17994-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="17994-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17994-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="17994-127">Attributes</span></span>

|<span data-ttu-id="17994-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="17994-128">**Attribute**</span></span>|<span data-ttu-id="17994-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="17994-129">**Type**</span></span>|<span data-ttu-id="17994-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="17994-130">**Required**</span></span>|<span data-ttu-id="17994-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="17994-131">**Description**</span></span>|<span data-ttu-id="17994-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="17994-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="17994-133">IX</span><span class="sxs-lookup"><span data-stu-id="17994-133">IX</span></span>  <br/> |<span data-ttu-id="17994-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17994-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17994-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="17994-135">required</span></span>  <br/> |<span data-ttu-id="17994-136">L’index de l’élément de **paragraphe** qui spécifie la mise en forme appliquée à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="17994-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="17994-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17994-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

