---
title: élément TP (Text_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Spécifie le début d’un propriétés onglets exécuter. L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.
ms.openlocfilehash: 9b98374af4ffbf2eaeaea61dcb1dbb49214f01b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789919"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="d7300-104">élément TP (Text_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="d7300-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d7300-105">Spécifie le début d’un propriétés onglets exécuter.</span><span class="sxs-lookup"><span data-stu-id="d7300-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="d7300-106">L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="d7300-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7300-107">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="d7300-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7300-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="d7300-108">**Element type**</span></span> <br/> |[<span data-ttu-id="d7300-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="d7300-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d7300-110">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="d7300-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d7300-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d7300-111">**Schema file**</span></span> <br/> |<span data-ttu-id="d7300-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d7300-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d7300-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="d7300-113">**Document parts**</span></span> <br/> |<span data-ttu-id="d7300-114">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="d7300-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7300-115">Définition</span><span class="sxs-lookup"><span data-stu-id="d7300-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d7300-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d7300-116">Elements and attributes</span></span>

<span data-ttu-id="d7300-117">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="d7300-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d7300-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d7300-118">Parent elements</span></span>

|<span data-ttu-id="d7300-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d7300-119">**Element**</span></span>|<span data-ttu-id="d7300-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="d7300-120">**Type**</span></span>|<span data-ttu-id="d7300-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7300-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d7300-122">Text</span><span class="sxs-lookup"><span data-stu-id="d7300-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7300-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="d7300-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7300-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="d7300-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d7300-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d7300-125">Child elements</span></span>

<span data-ttu-id="d7300-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d7300-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7300-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="d7300-127">Attributes</span></span>

|<span data-ttu-id="d7300-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d7300-128">**Attribute**</span></span>|<span data-ttu-id="d7300-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="d7300-129">**Type**</span></span>|<span data-ttu-id="d7300-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d7300-130">**Required**</span></span>|<span data-ttu-id="d7300-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7300-131">**Description**</span></span>|<span data-ttu-id="d7300-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d7300-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7300-133">IX</span><span class="sxs-lookup"><span data-stu-id="d7300-133">IX</span></span>  <br/> |<span data-ttu-id="d7300-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d7300-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d7300-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d7300-135">required</span></span>  <br/> |<span data-ttu-id="d7300-136">Index de base zéro de l’élément dans l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="d7300-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="d7300-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d7300-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

