---
title: ComplexType HeaderFooter_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 581101909096d4ee8a4f44c8e9e95dab0313ed7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342237"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="4bbb3-102">ComplexType HeaderFooter_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4bbb3-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4bbb3-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4bbb3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4bbb3-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4bbb3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="4bbb3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4bbb3-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4bbb3-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="4bbb3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4bbb3-109">Définition</span><span class="sxs-lookup"><span data-stu-id="4bbb3-109">Definition</span></span>

```XML
          <xs:complexType name="HeaderFooter_Type">
          
          <xs:all>
    <xs:element name="HeaderMargin"  type="HeaderMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterMargin"  type="FooterMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderLeft"  type="HeaderLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderCenter"  type="HeaderCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderRight"  type="HeaderRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterLeft"  type="FooterLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterCenter"  type="FooterCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterRight"  type="FooterRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooterFont"  type="HeaderFooterFont_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="HeaderFooterColor"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4bbb3-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4bbb3-110">Elements and attributes</span></span>

<span data-ttu-id="4bbb3-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="4bbb3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4bbb3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4bbb3-112">Child elements</span></span>

|<span data-ttu-id="4bbb3-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-113">**Element**</span></span>|<span data-ttu-id="4bbb3-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-114">**Type**</span></span>|<span data-ttu-id="4bbb3-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4bbb3-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="4bbb3-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="4bbb3-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="4bbb3-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="4bbb3-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="4bbb3-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="4bbb3-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="4bbb3-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="4bbb3-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4bbb3-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="4bbb3-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4bbb3-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="4bbb3-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4bbb3-134">Attributs</span><span class="sxs-lookup"><span data-stu-id="4bbb3-134">Attributes</span></span>

|<span data-ttu-id="4bbb3-135">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-135">**Attribute**</span></span>|<span data-ttu-id="4bbb3-136">**Type**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-136">**Type**</span></span>|<span data-ttu-id="4bbb3-137">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-137">**Required**</span></span>|<span data-ttu-id="4bbb3-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-138">**Description**</span></span>|<span data-ttu-id="4bbb3-139">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4bbb3-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4bbb3-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="4bbb3-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="4bbb3-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="4bbb3-141">xsd:string</span></span>  <br/> |<span data-ttu-id="4bbb3-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="4bbb3-142">optional</span></span>  <br/> ||<span data-ttu-id="4bbb3-143">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4bbb3-143">Values of the xsd:string type.</span></span>  <br/> |
   

