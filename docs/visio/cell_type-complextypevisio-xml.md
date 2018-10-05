---
title: Type complexe Cell_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389462"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="f24ad-102">Type complexe Cell_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="f24ad-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f24ad-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f24ad-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f24ad-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="f24ad-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f24ad-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f24ad-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f24ad-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f24ad-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f24ad-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f24ad-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f24ad-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="f24ad-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f24ad-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f24ad-109">Definition</span></span>

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f24ad-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f24ad-110">Elements and attributes</span></span>

<span data-ttu-id="f24ad-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="f24ad-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f24ad-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f24ad-112">Child elements</span></span>

|<span data-ttu-id="f24ad-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f24ad-113">**Element**</span></span>|<span data-ttu-id="f24ad-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="f24ad-114">**Type**</span></span>|<span data-ttu-id="f24ad-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f24ad-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f24ad-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="f24ad-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f24ad-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="f24ad-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f24ad-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="f24ad-118">Attributes</span></span>

|<span data-ttu-id="f24ad-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f24ad-119">**Attribute**</span></span>|<span data-ttu-id="f24ad-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="f24ad-120">**Type**</span></span>|<span data-ttu-id="f24ad-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f24ad-121">**Required**</span></span>|<span data-ttu-id="f24ad-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="f24ad-122">**Description**</span></span>|<span data-ttu-id="f24ad-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f24ad-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f24ad-124">E</span><span class="sxs-lookup"><span data-stu-id="f24ad-124">E</span></span>  <br/> |<span data-ttu-id="f24ad-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f24ad-125">xsd:string</span></span>  <br/> |<span data-ttu-id="f24ad-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="f24ad-126">optional</span></span>  <br/> ||<span data-ttu-id="f24ad-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f24ad-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f24ad-128">F</span><span class="sxs-lookup"><span data-stu-id="f24ad-128">F</span></span>  <br/> |<span data-ttu-id="f24ad-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f24ad-129">xsd:string</span></span>  <br/> |<span data-ttu-id="f24ad-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="f24ad-130">optional</span></span>  <br/> ||<span data-ttu-id="f24ad-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f24ad-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f24ad-132">N</span><span class="sxs-lookup"><span data-stu-id="f24ad-132">N</span></span>  <br/> |<span data-ttu-id="f24ad-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f24ad-133">xsd:string</span></span>  <br/> |<span data-ttu-id="f24ad-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f24ad-134">required</span></span>  <br/> ||<span data-ttu-id="f24ad-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f24ad-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f24ad-136">U</span><span class="sxs-lookup"><span data-stu-id="f24ad-136">U</span></span>  <br/> |<span data-ttu-id="f24ad-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f24ad-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f24ad-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="f24ad-138">optional</span></span>  <br/> ||<span data-ttu-id="f24ad-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f24ad-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f24ad-140">V</span><span class="sxs-lookup"><span data-stu-id="f24ad-140">V</span></span>  <br/> |<span data-ttu-id="f24ad-141">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f24ad-141">xsd:string</span></span>  <br/> |<span data-ttu-id="f24ad-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="f24ad-142">optional</span></span>  <br/> ||<span data-ttu-id="f24ad-143">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f24ad-143">Values of the xsd:string type.</span></span>  <br/> |
   

