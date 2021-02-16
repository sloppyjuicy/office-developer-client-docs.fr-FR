---
title: RuleSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 5d3d29ee7ae48c344afcdce3faf5e26d5f564501
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541623"
---
# <a name="ruleset_type-complextype-visio-xml"></a><span data-ttu-id="11445-102">RuleSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="11445-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="11445-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="11445-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11445-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11445-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="11445-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="11445-105">**Schema file**</span></span> <br/> |<span data-ttu-id="11445-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="11445-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="11445-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="11445-107">**Extension base**</span></span> <br/> |<span data-ttu-id="11445-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="11445-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11445-109">Définition</span><span class="sxs-lookup"><span data-stu-id="11445-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSet_Type">
          
          <xs:sequence>
    <xs:element name="RuleSetFlags"  type="RuleSetFlags_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rule"  type="Rule_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11445-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="11445-110">Elements and attributes</span></span>

<span data-ttu-id="11445-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="11445-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="11445-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="11445-112">Child elements</span></span>

|<span data-ttu-id="11445-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="11445-113">**Element**</span></span>|<span data-ttu-id="11445-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="11445-114">**Type**</span></span>|<span data-ttu-id="11445-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="11445-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11445-116">Règle</span><span class="sxs-lookup"><span data-stu-id="11445-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="11445-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="11445-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="11445-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="11445-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="11445-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="11445-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="11445-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="11445-120">Attributes</span></span>

|<span data-ttu-id="11445-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="11445-121">**Attribute**</span></span>|<span data-ttu-id="11445-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="11445-122">**Type**</span></span>|<span data-ttu-id="11445-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="11445-123">**Required**</span></span>|<span data-ttu-id="11445-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="11445-124">**Description**</span></span>|<span data-ttu-id="11445-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="11445-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="11445-126">Description</span><span class="sxs-lookup"><span data-stu-id="11445-126">Description</span></span>  <br/> |<span data-ttu-id="11445-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="11445-127">xsd:string</span></span>  <br/> |<span data-ttu-id="11445-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="11445-128">optional</span></span>  <br/> ||<span data-ttu-id="11445-129">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="11445-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="11445-130">Activé</span><span class="sxs-lookup"><span data-stu-id="11445-130">Enabled</span></span>  <br/> |<span data-ttu-id="11445-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="11445-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="11445-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="11445-132">optional</span></span>  <br/> ||<span data-ttu-id="11445-133">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="11445-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="11445-134">ID</span><span class="sxs-lookup"><span data-stu-id="11445-134">ID</span></span>  <br/> |<span data-ttu-id="11445-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="11445-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="11445-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="11445-136">required</span></span>  <br/> ||<span data-ttu-id="11445-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="11445-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="11445-138">Nom</span><span class="sxs-lookup"><span data-stu-id="11445-138">Name</span></span>  <br/> |<span data-ttu-id="11445-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="11445-139">xsd:string</span></span>  <br/> |<span data-ttu-id="11445-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="11445-140">optional</span></span>  <br/> ||<span data-ttu-id="11445-141">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="11445-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="11445-142">NameU</span><span class="sxs-lookup"><span data-stu-id="11445-142">NameU</span></span>  <br/> |<span data-ttu-id="11445-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="11445-143">xsd:string</span></span>  <br/> |<span data-ttu-id="11445-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="11445-144">required</span></span>  <br/> ||<span data-ttu-id="11445-145">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="11445-145">Values of the xsd:string type.</span></span>  <br/> |
   

