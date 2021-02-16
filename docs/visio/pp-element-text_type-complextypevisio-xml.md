---
title: élément pp (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Spécifie le début d’une exécute de propriétés de paragraphe. La suite est définie à la fin du texte ou jusqu’à la balise suivante.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537737"
---
# <a name="pp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="4f9a5-104">élément pp (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4f9a5-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4f9a5-105">Spécifie le début d’une exécute de propriétés de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="4f9a5-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="4f9a5-106">La suite est définie à la fin du texte ou jusqu’à la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="4f9a5-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f9a5-107">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="4f9a5-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f9a5-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-108">**Element type**</span></span> <br/> |[<span data-ttu-id="4f9a5-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="4f9a5-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4f9a5-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4f9a5-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-111">**Schema file**</span></span> <br/> |<span data-ttu-id="4f9a5-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4f9a5-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4f9a5-113">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-113">**Document parts**</span></span> <br/> |<span data-ttu-id="4f9a5-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="4f9a5-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f9a5-115">Définition</span><span class="sxs-lookup"><span data-stu-id="4f9a5-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f9a5-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4f9a5-116">Elements and attributes</span></span>

<span data-ttu-id="4f9a5-117">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="4f9a5-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f9a5-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4f9a5-118">Parent elements</span></span>

|<span data-ttu-id="4f9a5-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-119">**Element**</span></span>|<span data-ttu-id="4f9a5-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-120">**Type**</span></span>|<span data-ttu-id="4f9a5-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f9a5-122">Text</span><span class="sxs-lookup"><span data-stu-id="4f9a5-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f9a5-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="4f9a5-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f9a5-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="4f9a5-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f9a5-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4f9a5-125">Child elements</span></span>

<span data-ttu-id="4f9a5-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4f9a5-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f9a5-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="4f9a5-127">Attributes</span></span>

|<span data-ttu-id="4f9a5-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-128">**Attribute**</span></span>|<span data-ttu-id="4f9a5-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-129">**Type**</span></span>|<span data-ttu-id="4f9a5-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-130">**Required**</span></span>|<span data-ttu-id="4f9a5-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-131">**Description**</span></span>|<span data-ttu-id="4f9a5-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4f9a5-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f9a5-133">IX</span><span class="sxs-lookup"><span data-stu-id="4f9a5-133">IX</span></span>  <br/> |<span data-ttu-id="4f9a5-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4f9a5-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4f9a5-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4f9a5-135">required</span></span>  <br/> |<span data-ttu-id="4f9a5-136">Index de **l’élément Para** qui spécifie la mise en forme appliquée à cette run.</span><span class="sxs-lookup"><span data-stu-id="4f9a5-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="4f9a5-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4f9a5-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

