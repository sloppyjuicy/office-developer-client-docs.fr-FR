---
title: élément pp (Text_Type complexType) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Indique le début des propriétés de paragraphe exécutées. L’exécution est définie à la fin du texte ou jusqu’à la balise suivante.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537737"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="82e0f-104">élément pp (Text_Type complexType) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="82e0f-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="82e0f-105">Indique le début des propriétés de paragraphe exécutées.</span><span class="sxs-lookup"><span data-stu-id="82e0f-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="82e0f-106">L’exécution est définie à la fin du texte ou jusqu’à la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="82e0f-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82e0f-107">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="82e0f-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82e0f-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="82e0f-108">**Element type**</span></span> <br/> |[<span data-ttu-id="82e0f-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="82e0f-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="82e0f-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="82e0f-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="82e0f-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="82e0f-111">**Schema file**</span></span> <br/> |<span data-ttu-id="82e0f-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="82e0f-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="82e0f-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="82e0f-113">**Document parts**</span></span> <br/> |<span data-ttu-id="82e0f-114">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="82e0f-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="82e0f-115">Définition</span><span class="sxs-lookup"><span data-stu-id="82e0f-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="82e0f-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="82e0f-116">Elements and attributes</span></span>

<span data-ttu-id="82e0f-117">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="82e0f-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="82e0f-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="82e0f-118">Parent elements</span></span>

|<span data-ttu-id="82e0f-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="82e0f-119">**Element**</span></span>|<span data-ttu-id="82e0f-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="82e0f-120">**Type**</span></span>|<span data-ttu-id="82e0f-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="82e0f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82e0f-122">Text</span><span class="sxs-lookup"><span data-stu-id="82e0f-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e0f-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="82e0f-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="82e0f-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="82e0f-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="82e0f-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="82e0f-125">Child elements</span></span>

<span data-ttu-id="82e0f-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="82e0f-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82e0f-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="82e0f-127">Attributes</span></span>

|<span data-ttu-id="82e0f-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="82e0f-128">**Attribute**</span></span>|<span data-ttu-id="82e0f-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="82e0f-129">**Type**</span></span>|<span data-ttu-id="82e0f-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="82e0f-130">**Required**</span></span>|<span data-ttu-id="82e0f-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="82e0f-131">**Description**</span></span>|<span data-ttu-id="82e0f-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="82e0f-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="82e0f-133">IX</span><span class="sxs-lookup"><span data-stu-id="82e0f-133">IX</span></span>  <br/> |<span data-ttu-id="82e0f-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="82e0f-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="82e0f-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="82e0f-135">required</span></span>  <br/> |<span data-ttu-id="82e0f-136">Index de l’élément **para** qui spécifie la mise en forme appliquée à cette exécution.</span><span class="sxs-lookup"><span data-stu-id="82e0f-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="82e0f-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="82e0f-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

