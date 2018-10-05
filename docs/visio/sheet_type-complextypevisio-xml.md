---
title: Type complexe Sheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: dc8930ffa89baf059074a12bb285e6b53e329e41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388748"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="a8487-102">Type complexe Sheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a8487-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a8487-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a8487-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8487-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a8487-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a8487-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a8487-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a8487-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a8487-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a8487-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a8487-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a8487-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="a8487-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8487-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a8487-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a8487-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a8487-110">Elements and attributes</span></span>

<span data-ttu-id="a8487-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a8487-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a8487-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8487-112">Child elements</span></span>

|<span data-ttu-id="a8487-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a8487-113">**Element**</span></span>|<span data-ttu-id="a8487-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8487-114">**Type**</span></span>|<span data-ttu-id="a8487-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8487-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8487-116">Cell</span><span class="sxs-lookup"><span data-stu-id="a8487-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="a8487-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a8487-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a8487-118">Section</span><span class="sxs-lookup"><span data-stu-id="a8487-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a8487-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="a8487-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a8487-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="a8487-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="a8487-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="a8487-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a8487-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8487-122">Attributes</span></span>

|<span data-ttu-id="a8487-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a8487-123">**Attribute**</span></span>|<span data-ttu-id="a8487-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8487-124">**Type**</span></span>|<span data-ttu-id="a8487-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a8487-125">**Required**</span></span>|<span data-ttu-id="a8487-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8487-126">**Description**</span></span>|<span data-ttu-id="a8487-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a8487-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8487-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="a8487-128">FillStyle</span></span>  <br/> |<span data-ttu-id="a8487-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8487-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8487-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8487-130">optional</span></span>  <br/> ||<span data-ttu-id="a8487-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8487-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8487-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="a8487-132">LineStyle</span></span>  <br/> |<span data-ttu-id="a8487-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8487-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8487-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8487-134">optional</span></span>  <br/> ||<span data-ttu-id="a8487-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8487-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8487-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="a8487-136">TextStyle</span></span>  <br/> |<span data-ttu-id="a8487-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8487-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8487-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8487-138">optional</span></span>  <br/> ||<span data-ttu-id="a8487-139">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8487-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

