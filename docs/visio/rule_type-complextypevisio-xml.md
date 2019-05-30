---
title: ComplexType Rule_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: a1c3111458b90cd5e1b181a3b1776f64d8ec476b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541714"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="e5ca8-102">ComplexType Rule_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e5ca8-102">Rule_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e5ca8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e5ca8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5ca8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e5ca8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e5ca8-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e5ca8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e5ca8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e5ca8-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="e5ca8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5ca8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e5ca8-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e5ca8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e5ca8-110">Elements and attributes</span></span>

<span data-ttu-id="e5ca8-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="e5ca8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e5ca8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e5ca8-112">Child elements</span></span>

|<span data-ttu-id="e5ca8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-113">**Element**</span></span>|<span data-ttu-id="e5ca8-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-114">**Type**</span></span>|<span data-ttu-id="e5ca8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5ca8-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="e5ca8-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e5ca8-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="e5ca8-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e5ca8-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="e5ca8-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e5ca8-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="e5ca8-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e5ca8-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="e5ca8-120">Attributes</span></span>

|<span data-ttu-id="e5ca8-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-121">**Attribute**</span></span>|<span data-ttu-id="e5ca8-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-122">**Type**</span></span>|<span data-ttu-id="e5ca8-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-123">**Required**</span></span>|<span data-ttu-id="e5ca8-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-124">**Description**</span></span>|<span data-ttu-id="e5ca8-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e5ca8-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e5ca8-126">Catégorie</span><span class="sxs-lookup"><span data-stu-id="e5ca8-126">Category</span></span>  <br/> |<span data-ttu-id="e5ca8-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5ca8-127">xsd:string</span></span>  <br/> |<span data-ttu-id="e5ca8-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5ca8-128">optional</span></span>  <br/> ||<span data-ttu-id="e5ca8-129">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5ca8-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5ca8-130">Description</span><span class="sxs-lookup"><span data-stu-id="e5ca8-130">Description</span></span>  <br/> |<span data-ttu-id="e5ca8-131">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5ca8-131">xsd:string</span></span>  <br/> |<span data-ttu-id="e5ca8-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5ca8-132">optional</span></span>  <br/> ||<span data-ttu-id="e5ca8-133">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5ca8-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5ca8-134">ID</span><span class="sxs-lookup"><span data-stu-id="e5ca8-134">ID</span></span>  <br/> |<span data-ttu-id="e5ca8-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e5ca8-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e5ca8-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5ca8-136">required</span></span>  <br/> ||<span data-ttu-id="e5ca8-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e5ca8-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e5ca8-138">Ignoré</span><span class="sxs-lookup"><span data-stu-id="e5ca8-138">Ignored</span></span>  <br/> |<span data-ttu-id="e5ca8-139">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="e5ca8-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e5ca8-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5ca8-140">optional</span></span>  <br/> ||<span data-ttu-id="e5ca8-141">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e5ca8-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e5ca8-142">NameU</span><span class="sxs-lookup"><span data-stu-id="e5ca8-142">NameU</span></span>  <br/> |<span data-ttu-id="e5ca8-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5ca8-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e5ca8-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5ca8-144">required</span></span>  <br/> ||<span data-ttu-id="e5ca8-145">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5ca8-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5ca8-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="e5ca8-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="e5ca8-147">xsd: int</span><span class="sxs-lookup"><span data-stu-id="e5ca8-147">xsd:int</span></span>  <br/> |<span data-ttu-id="e5ca8-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5ca8-148">optional</span></span>  <br/> ||<span data-ttu-id="e5ca8-149">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="e5ca8-149">Values of the xsd:int type.</span></span>  <br/> |
   

