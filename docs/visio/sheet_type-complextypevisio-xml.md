---
title: Sheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: b747f2257f2b09083b72a17a59856be0a985b270
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540405"
---
# <a name="sheet_type-complextype-visio-xml"></a><span data-ttu-id="210ca-102">Sheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="210ca-102">Sheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="210ca-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="210ca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="210ca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="210ca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="210ca-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="210ca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="210ca-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="210ca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="210ca-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="210ca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="210ca-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="210ca-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="210ca-109">Définition</span><span class="sxs-lookup"><span data-stu-id="210ca-109">Definition</span></span>

```XML
        <xs:complexType name="Sheet_Type" abstract="true">
        
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Section"  type="Section_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
    <xs:attribute name="LineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="FillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TextStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="210ca-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="210ca-110">Elements and attributes</span></span>

<span data-ttu-id="210ca-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="210ca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="210ca-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="210ca-112">Child elements</span></span>

|<span data-ttu-id="210ca-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="210ca-113">**Element**</span></span>|<span data-ttu-id="210ca-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="210ca-114">**Type**</span></span>|<span data-ttu-id="210ca-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="210ca-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="210ca-116">Cell</span><span class="sxs-lookup"><span data-stu-id="210ca-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="210ca-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="210ca-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="210ca-118">Section</span><span class="sxs-lookup"><span data-stu-id="210ca-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="210ca-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="210ca-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="210ca-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="210ca-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="210ca-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="210ca-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="210ca-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="210ca-122">Attributes</span></span>

|<span data-ttu-id="210ca-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="210ca-123">**Attribute**</span></span>|<span data-ttu-id="210ca-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="210ca-124">**Type**</span></span>|<span data-ttu-id="210ca-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="210ca-125">**Required**</span></span>|<span data-ttu-id="210ca-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="210ca-126">**Description**</span></span>|<span data-ttu-id="210ca-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="210ca-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="210ca-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="210ca-128">FillStyle</span></span>  <br/> |<span data-ttu-id="210ca-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="210ca-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="210ca-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="210ca-130">optional</span></span>  <br/> ||<span data-ttu-id="210ca-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="210ca-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="210ca-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="210ca-132">LineStyle</span></span>  <br/> |<span data-ttu-id="210ca-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="210ca-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="210ca-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="210ca-134">optional</span></span>  <br/> ||<span data-ttu-id="210ca-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="210ca-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="210ca-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="210ca-136">TextStyle</span></span>  <br/> |<span data-ttu-id="210ca-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="210ca-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="210ca-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="210ca-138">optional</span></span>  <br/> ||<span data-ttu-id="210ca-139">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="210ca-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

