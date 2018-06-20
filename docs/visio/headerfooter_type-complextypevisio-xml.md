---
title: Type complexe HeaderFooter_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 9c567542061ec419de9c4347209059b0486bdf88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788747"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="a3a78-102">Type complexe HeaderFooter_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a3a78-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a3a78-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a3a78-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3a78-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a3a78-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a3a78-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a3a78-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a3a78-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a3a78-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a3a78-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a3a78-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a3a78-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="a3a78-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3a78-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a3a78-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a3a78-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a3a78-110">Elements and attributes</span></span>

<span data-ttu-id="a3a78-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a3a78-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a3a78-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a3a78-112">Child elements</span></span>

|<span data-ttu-id="a3a78-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a3a78-113">**Element**</span></span>|<span data-ttu-id="a3a78-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a3a78-114">**Type**</span></span>|<span data-ttu-id="a3a78-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3a78-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3a78-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="a3a78-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="a3a78-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="a3a78-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="a3a78-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="a3a78-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="a3a78-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="a3a78-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="a3a78-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3a78-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="a3a78-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3a78-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="a3a78-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a3a78-134">Attributs</span><span class="sxs-lookup"><span data-stu-id="a3a78-134">Attributes</span></span>

|<span data-ttu-id="a3a78-135">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a3a78-135">**Attribute**</span></span>|<span data-ttu-id="a3a78-136">**Type**</span><span class="sxs-lookup"><span data-stu-id="a3a78-136">**Type**</span></span>|<span data-ttu-id="a3a78-137">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a3a78-137">**Required**</span></span>|<span data-ttu-id="a3a78-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3a78-138">**Description**</span></span>|<span data-ttu-id="a3a78-139">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a3a78-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3a78-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="a3a78-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="a3a78-141">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a3a78-141">xsd:string</span></span>  <br/> |<span data-ttu-id="a3a78-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="a3a78-142">optional</span></span>  <br/> ||<span data-ttu-id="a3a78-143">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a3a78-143">Values of the xsd:string type.</span></span>  <br/> |
   

