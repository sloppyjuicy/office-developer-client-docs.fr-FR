---
title: Type complexe Sheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: f171f250fbe37ebf1d0d434709b06ab56804407f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789705"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="579c0-102">Type complexe Sheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="579c0-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="579c0-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="579c0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="579c0-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="579c0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="579c0-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="579c0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="579c0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="579c0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="579c0-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="579c0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="579c0-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="579c0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="579c0-109">Définition</span><span class="sxs-lookup"><span data-stu-id="579c0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="579c0-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="579c0-110">Elements and attributes</span></span>

<span data-ttu-id="579c0-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="579c0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="579c0-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="579c0-112">Child elements</span></span>

|<span data-ttu-id="579c0-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="579c0-113">**Element**</span></span>|<span data-ttu-id="579c0-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="579c0-114">**Type**</span></span>|<span data-ttu-id="579c0-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="579c0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="579c0-116">Cell</span><span class="sxs-lookup"><span data-stu-id="579c0-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="579c0-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="579c0-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="579c0-118">Section</span><span class="sxs-lookup"><span data-stu-id="579c0-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="579c0-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="579c0-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="579c0-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="579c0-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="579c0-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="579c0-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="579c0-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="579c0-122">Attributes</span></span>

|<span data-ttu-id="579c0-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="579c0-123">**Attribute**</span></span>|<span data-ttu-id="579c0-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="579c0-124">**Type**</span></span>|<span data-ttu-id="579c0-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="579c0-125">**Required**</span></span>|<span data-ttu-id="579c0-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="579c0-126">**Description**</span></span>|<span data-ttu-id="579c0-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="579c0-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="579c0-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="579c0-128">FillStyle</span></span>  <br/> |<span data-ttu-id="579c0-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="579c0-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="579c0-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="579c0-130">optional</span></span>  <br/> ||<span data-ttu-id="579c0-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="579c0-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="579c0-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="579c0-132">LineStyle</span></span>  <br/> |<span data-ttu-id="579c0-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="579c0-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="579c0-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="579c0-134">optional</span></span>  <br/> ||<span data-ttu-id="579c0-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="579c0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="579c0-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="579c0-136">TextStyle</span></span>  <br/> |<span data-ttu-id="579c0-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="579c0-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="579c0-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="579c0-138">optional</span></span>  <br/> ||<span data-ttu-id="579c0-139">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="579c0-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

