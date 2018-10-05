---
title: élément fld (Text_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Indique un point d’insertion de champs de texte pour l’élément de champ correspondant.
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383323"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="6ba0e-103">élément fld (Text_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="6ba0e-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6ba0e-104">Indique un point d’insertion de champs de texte pour l’élément de **champ** correspondant.</span><span class="sxs-lookup"><span data-stu-id="6ba0e-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6ba0e-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="6ba0e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ba0e-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6ba0e-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="6ba0e-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6ba0e-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6ba0e-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6ba0e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6ba0e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6ba0e-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6ba0e-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="6ba0e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ba0e-113">Définition</span><span class="sxs-lookup"><span data-stu-id="6ba0e-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ba0e-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6ba0e-114">Elements and attributes</span></span>

<span data-ttu-id="6ba0e-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="6ba0e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6ba0e-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6ba0e-116">Parent elements</span></span>

|<span data-ttu-id="6ba0e-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-117">**Element**</span></span>|<span data-ttu-id="6ba0e-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-118">**Type**</span></span>|<span data-ttu-id="6ba0e-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ba0e-120">Text</span><span class="sxs-lookup"><span data-stu-id="6ba0e-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ba0e-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="6ba0e-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ba0e-122">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="6ba0e-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6ba0e-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6ba0e-123">Child elements</span></span>

<span data-ttu-id="6ba0e-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6ba0e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ba0e-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="6ba0e-125">Attributes</span></span>

|<span data-ttu-id="6ba0e-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-126">**Attribute**</span></span>|<span data-ttu-id="6ba0e-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-127">**Type**</span></span>|<span data-ttu-id="6ba0e-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-128">**Required**</span></span>|<span data-ttu-id="6ba0e-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-129">**Description**</span></span>|<span data-ttu-id="6ba0e-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="6ba0e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6ba0e-131">IX</span><span class="sxs-lookup"><span data-stu-id="6ba0e-131">IX</span></span>  <br/> |<span data-ttu-id="6ba0e-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ba0e-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6ba0e-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6ba0e-133">required</span></span>  <br/> |<span data-ttu-id="6ba0e-134">Index de base zéro de l’élément dans l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="6ba0e-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="6ba0e-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6ba0e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

