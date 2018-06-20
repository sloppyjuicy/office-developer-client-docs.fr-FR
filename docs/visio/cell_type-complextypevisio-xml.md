---
title: Type complexe Cell_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: b17a251844a00ce01ad572dc63d971329214a23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788226"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="5e706-102">Type complexe Cell_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="5e706-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5e706-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="5e706-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e706-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="5e706-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5e706-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5e706-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5e706-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5e706-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5e706-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="5e706-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5e706-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="5e706-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5e706-109">Définition</span><span class="sxs-lookup"><span data-stu-id="5e706-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5e706-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5e706-110">Elements and attributes</span></span>

<span data-ttu-id="5e706-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="5e706-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5e706-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5e706-112">Child elements</span></span>

|<span data-ttu-id="5e706-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5e706-113">**Element**</span></span>|<span data-ttu-id="5e706-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="5e706-114">**Type**</span></span>|<span data-ttu-id="5e706-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="5e706-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5e706-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="5e706-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5e706-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="5e706-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5e706-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="5e706-118">Attributes</span></span>

|<span data-ttu-id="5e706-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5e706-119">**Attribute**</span></span>|<span data-ttu-id="5e706-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="5e706-120">**Type**</span></span>|<span data-ttu-id="5e706-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="5e706-121">**Required**</span></span>|<span data-ttu-id="5e706-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="5e706-122">**Description**</span></span>|<span data-ttu-id="5e706-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="5e706-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5e706-124">E</span><span class="sxs-lookup"><span data-stu-id="5e706-124">E</span></span>  <br/> |<span data-ttu-id="5e706-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5e706-125">xsd:string</span></span>  <br/> |<span data-ttu-id="5e706-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="5e706-126">optional</span></span>  <br/> ||<span data-ttu-id="5e706-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5e706-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e706-128">F</span><span class="sxs-lookup"><span data-stu-id="5e706-128">F</span></span>  <br/> |<span data-ttu-id="5e706-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5e706-129">xsd:string</span></span>  <br/> |<span data-ttu-id="5e706-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="5e706-130">optional</span></span>  <br/> ||<span data-ttu-id="5e706-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5e706-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e706-132">N</span><span class="sxs-lookup"><span data-stu-id="5e706-132">N</span></span>  <br/> |<span data-ttu-id="5e706-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5e706-133">xsd:string</span></span>  <br/> |<span data-ttu-id="5e706-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="5e706-134">required</span></span>  <br/> ||<span data-ttu-id="5e706-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5e706-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e706-136">U</span><span class="sxs-lookup"><span data-stu-id="5e706-136">U</span></span>  <br/> |<span data-ttu-id="5e706-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5e706-137">xsd:string</span></span>  <br/> |<span data-ttu-id="5e706-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="5e706-138">optional</span></span>  <br/> ||<span data-ttu-id="5e706-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5e706-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e706-140">V</span><span class="sxs-lookup"><span data-stu-id="5e706-140">V</span></span>  <br/> |<span data-ttu-id="5e706-141">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5e706-141">xsd:string</span></span>  <br/> |<span data-ttu-id="5e706-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="5e706-142">optional</span></span>  <br/> ||<span data-ttu-id="5e706-143">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5e706-143">Values of the xsd:string type.</span></span>  <br/> |
   

