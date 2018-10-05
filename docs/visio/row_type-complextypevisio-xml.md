---
title: Type complexe Row_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: ebd3b666590e6144d2a3cb6e0059b64eb6e8dab5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391576"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="47016-102">Type complexe Row_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="47016-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="47016-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="47016-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47016-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="47016-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47016-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="47016-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47016-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47016-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47016-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="47016-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47016-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="47016-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47016-109">Définition</span><span class="sxs-lookup"><span data-stu-id="47016-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
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
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="47016-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="47016-110">Elements and attributes</span></span>

<span data-ttu-id="47016-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="47016-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47016-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="47016-112">Child elements</span></span>

|<span data-ttu-id="47016-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="47016-113">**Element**</span></span>|<span data-ttu-id="47016-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="47016-114">**Type**</span></span>|<span data-ttu-id="47016-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="47016-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47016-116">Cell</span><span class="sxs-lookup"><span data-stu-id="47016-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="47016-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="47016-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="47016-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="47016-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="47016-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="47016-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="47016-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="47016-120">Attributes</span></span>

|<span data-ttu-id="47016-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="47016-121">**Attribute**</span></span>|<span data-ttu-id="47016-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="47016-122">**Type**</span></span>|<span data-ttu-id="47016-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="47016-123">**Required**</span></span>|<span data-ttu-id="47016-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="47016-124">**Description**</span></span>|<span data-ttu-id="47016-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="47016-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47016-126">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="47016-126">Del</span></span>  <br/> |<span data-ttu-id="47016-127">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="47016-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="47016-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="47016-128">optional</span></span>  <br/> ||<span data-ttu-id="47016-129">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="47016-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="47016-130">IX</span><span class="sxs-lookup"><span data-stu-id="47016-130">IX</span></span>  <br/> |<span data-ttu-id="47016-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47016-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47016-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="47016-132">optional</span></span>  <br/> ||<span data-ttu-id="47016-133">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="47016-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="47016-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="47016-134">LocalName</span></span>  <br/> |<span data-ttu-id="47016-135">XSD : String</span><span class="sxs-lookup"><span data-stu-id="47016-135">xsd:string</span></span>  <br/> |<span data-ttu-id="47016-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="47016-136">optional</span></span>  <br/> ||<span data-ttu-id="47016-137">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="47016-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="47016-138">N</span><span class="sxs-lookup"><span data-stu-id="47016-138">N</span></span>  <br/> |<span data-ttu-id="47016-139">XSD : String</span><span class="sxs-lookup"><span data-stu-id="47016-139">xsd:string</span></span>  <br/> |<span data-ttu-id="47016-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="47016-140">optional</span></span>  <br/> ||<span data-ttu-id="47016-141">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="47016-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="47016-142">T</span><span class="sxs-lookup"><span data-stu-id="47016-142">T</span></span>  <br/> |<span data-ttu-id="47016-143">XSD : String</span><span class="sxs-lookup"><span data-stu-id="47016-143">xsd:string</span></span>  <br/> |<span data-ttu-id="47016-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="47016-144">optional</span></span>  <br/> ||<span data-ttu-id="47016-145">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="47016-145">Values of the xsd:string type.</span></span>  <br/> |
   

