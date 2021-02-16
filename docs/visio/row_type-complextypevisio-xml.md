---
title: Row_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: d728363e6a3e7cd7fca2b95d91469f0d50ae1c39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538157"
---
# <a name="row_type-complextype-visio-xml"></a><span data-ttu-id="6c461-102">Row_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6c461-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6c461-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6c461-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c461-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c461-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6c461-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6c461-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6c461-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6c461-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6c461-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6c461-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6c461-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="6c461-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c461-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6c461-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6c461-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6c461-110">Elements and attributes</span></span>

<span data-ttu-id="6c461-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="6c461-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6c461-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6c461-112">Child elements</span></span>

|<span data-ttu-id="6c461-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6c461-113">**Element**</span></span>|<span data-ttu-id="6c461-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="6c461-114">**Type**</span></span>|<span data-ttu-id="6c461-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c461-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6c461-116">Cell</span><span class="sxs-lookup"><span data-stu-id="6c461-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="6c461-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6c461-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6c461-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="6c461-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="6c461-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="6c461-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6c461-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="6c461-120">Attributes</span></span>

|<span data-ttu-id="6c461-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6c461-121">**Attribute**</span></span>|<span data-ttu-id="6c461-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="6c461-122">**Type**</span></span>|<span data-ttu-id="6c461-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="6c461-123">**Required**</span></span>|<span data-ttu-id="6c461-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c461-124">**Description**</span></span>|<span data-ttu-id="6c461-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="6c461-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6c461-126">Del</span><span class="sxs-lookup"><span data-stu-id="6c461-126">Del</span></span>  <br/> |<span data-ttu-id="6c461-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6c461-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6c461-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c461-128">optional</span></span>  <br/> ||<span data-ttu-id="6c461-129">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6c461-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6c461-130">IX</span><span class="sxs-lookup"><span data-stu-id="6c461-130">IX</span></span>  <br/> |<span data-ttu-id="6c461-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6c461-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6c461-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c461-132">optional</span></span>  <br/> ||<span data-ttu-id="6c461-133">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6c461-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6c461-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="6c461-134">LocalName</span></span>  <br/> |<span data-ttu-id="6c461-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6c461-135">xsd:string</span></span>  <br/> |<span data-ttu-id="6c461-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c461-136">optional</span></span>  <br/> ||<span data-ttu-id="6c461-137">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6c461-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c461-138">N</span><span class="sxs-lookup"><span data-stu-id="6c461-138">N</span></span>  <br/> |<span data-ttu-id="6c461-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6c461-139">xsd:string</span></span>  <br/> |<span data-ttu-id="6c461-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c461-140">optional</span></span>  <br/> ||<span data-ttu-id="6c461-141">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6c461-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c461-142">T</span><span class="sxs-lookup"><span data-stu-id="6c461-142">T</span></span>  <br/> |<span data-ttu-id="6c461-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6c461-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6c461-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c461-144">optional</span></span>  <br/> ||<span data-ttu-id="6c461-145">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6c461-145">Values of the xsd:string type.</span></span>  <br/> |
   

