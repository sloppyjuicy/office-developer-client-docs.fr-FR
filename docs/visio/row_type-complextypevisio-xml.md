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
# <a name="row_type-complextype-visio-xml"></a><span data-ttu-id="dedcf-102">Row_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dedcf-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dedcf-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="dedcf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dedcf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dedcf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dedcf-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="dedcf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dedcf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dedcf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dedcf-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="dedcf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dedcf-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="dedcf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dedcf-109">Définition</span><span class="sxs-lookup"><span data-stu-id="dedcf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dedcf-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="dedcf-110">Elements and attributes</span></span>

<span data-ttu-id="dedcf-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="dedcf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dedcf-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dedcf-112">Child elements</span></span>

|<span data-ttu-id="dedcf-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="dedcf-113">**Element**</span></span>|<span data-ttu-id="dedcf-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="dedcf-114">**Type**</span></span>|<span data-ttu-id="dedcf-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="dedcf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dedcf-116">Cell</span><span class="sxs-lookup"><span data-stu-id="dedcf-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="dedcf-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="dedcf-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="dedcf-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="dedcf-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="dedcf-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="dedcf-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="dedcf-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="dedcf-120">Attributes</span></span>

|<span data-ttu-id="dedcf-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dedcf-121">**Attribute**</span></span>|<span data-ttu-id="dedcf-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="dedcf-122">**Type**</span></span>|<span data-ttu-id="dedcf-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="dedcf-123">**Required**</span></span>|<span data-ttu-id="dedcf-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="dedcf-124">**Description**</span></span>|<span data-ttu-id="dedcf-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="dedcf-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dedcf-126">Del</span><span class="sxs-lookup"><span data-stu-id="dedcf-126">Del</span></span>  <br/> |<span data-ttu-id="dedcf-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="dedcf-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dedcf-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="dedcf-128">optional</span></span>  <br/> ||<span data-ttu-id="dedcf-129">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="dedcf-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dedcf-130">IX</span><span class="sxs-lookup"><span data-stu-id="dedcf-130">IX</span></span>  <br/> |<span data-ttu-id="dedcf-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dedcf-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dedcf-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="dedcf-132">optional</span></span>  <br/> ||<span data-ttu-id="dedcf-133">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dedcf-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dedcf-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="dedcf-134">LocalName</span></span>  <br/> |<span data-ttu-id="dedcf-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dedcf-135">xsd:string</span></span>  <br/> |<span data-ttu-id="dedcf-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="dedcf-136">optional</span></span>  <br/> ||<span data-ttu-id="dedcf-137">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dedcf-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dedcf-138">N</span><span class="sxs-lookup"><span data-stu-id="dedcf-138">N</span></span>  <br/> |<span data-ttu-id="dedcf-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dedcf-139">xsd:string</span></span>  <br/> |<span data-ttu-id="dedcf-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="dedcf-140">optional</span></span>  <br/> ||<span data-ttu-id="dedcf-141">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dedcf-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dedcf-142">T</span><span class="sxs-lookup"><span data-stu-id="dedcf-142">T</span></span>  <br/> |<span data-ttu-id="dedcf-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dedcf-143">xsd:string</span></span>  <br/> |<span data-ttu-id="dedcf-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="dedcf-144">optional</span></span>  <br/> ||<span data-ttu-id="dedcf-145">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dedcf-145">Values of the xsd:string type.</span></span>  <br/> |
   

