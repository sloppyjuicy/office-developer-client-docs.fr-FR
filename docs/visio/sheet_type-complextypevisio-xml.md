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
# <a name="sheet_type-complextype-visio-xml"></a><span data-ttu-id="5a500-102">Sheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5a500-102">Sheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5a500-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="5a500-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a500-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5a500-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5a500-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5a500-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5a500-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5a500-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5a500-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="5a500-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5a500-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="5a500-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5a500-109">Définition</span><span class="sxs-lookup"><span data-stu-id="5a500-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5a500-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5a500-110">Elements and attributes</span></span>

<span data-ttu-id="5a500-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="5a500-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5a500-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5a500-112">Child elements</span></span>

|<span data-ttu-id="5a500-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5a500-113">**Element**</span></span>|<span data-ttu-id="5a500-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="5a500-114">**Type**</span></span>|<span data-ttu-id="5a500-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="5a500-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5a500-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5a500-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="5a500-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5a500-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5a500-118">Section</span><span class="sxs-lookup"><span data-stu-id="5a500-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5a500-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5a500-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5a500-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="5a500-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="5a500-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="5a500-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5a500-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="5a500-122">Attributes</span></span>

|<span data-ttu-id="5a500-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5a500-123">**Attribute**</span></span>|<span data-ttu-id="5a500-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="5a500-124">**Type**</span></span>|<span data-ttu-id="5a500-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="5a500-125">**Required**</span></span>|<span data-ttu-id="5a500-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="5a500-126">**Description**</span></span>|<span data-ttu-id="5a500-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="5a500-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5a500-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="5a500-128">FillStyle</span></span>  <br/> |<span data-ttu-id="5a500-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5a500-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5a500-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="5a500-130">optional</span></span>  <br/> ||<span data-ttu-id="5a500-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5a500-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5a500-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="5a500-132">LineStyle</span></span>  <br/> |<span data-ttu-id="5a500-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5a500-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5a500-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="5a500-134">optional</span></span>  <br/> ||<span data-ttu-id="5a500-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5a500-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5a500-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="5a500-136">TextStyle</span></span>  <br/> |<span data-ttu-id="5a500-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5a500-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5a500-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="5a500-138">optional</span></span>  <br/> ||<span data-ttu-id="5a500-139">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5a500-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

