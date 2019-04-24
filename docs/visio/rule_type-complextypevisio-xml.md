---
title: ComplexType Rule_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283421"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="95d66-102">ComplexType Rule_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="95d66-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="95d66-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="95d66-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95d66-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95d66-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="95d66-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="95d66-105">**Schema file**</span></span> <br/> |<span data-ttu-id="95d66-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="95d66-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="95d66-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="95d66-107">**Extension base**</span></span> <br/> |<span data-ttu-id="95d66-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="95d66-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95d66-109">Définition</span><span class="sxs-lookup"><span data-stu-id="95d66-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="95d66-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="95d66-110">Elements and attributes</span></span>

<span data-ttu-id="95d66-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="95d66-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="95d66-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="95d66-112">Child elements</span></span>

|<span data-ttu-id="95d66-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="95d66-113">**Element**</span></span>|<span data-ttu-id="95d66-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="95d66-114">**Type**</span></span>|<span data-ttu-id="95d66-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="95d66-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95d66-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="95d66-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95d66-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="95d66-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="95d66-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="95d66-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95d66-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="95d66-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="95d66-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="95d66-120">Attributes</span></span>

|<span data-ttu-id="95d66-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="95d66-121">**Attribute**</span></span>|<span data-ttu-id="95d66-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="95d66-122">**Type**</span></span>|<span data-ttu-id="95d66-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="95d66-123">**Required**</span></span>|<span data-ttu-id="95d66-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="95d66-124">**Description**</span></span>|<span data-ttu-id="95d66-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="95d66-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95d66-126">Catégorie</span><span class="sxs-lookup"><span data-stu-id="95d66-126">Category</span></span>  <br/> |<span data-ttu-id="95d66-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="95d66-127">xsd:string</span></span>  <br/> |<span data-ttu-id="95d66-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="95d66-128">optional</span></span>  <br/> ||<span data-ttu-id="95d66-129">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="95d66-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95d66-130">Description</span><span class="sxs-lookup"><span data-stu-id="95d66-130">Description</span></span>  <br/> |<span data-ttu-id="95d66-131">xsd: String</span><span class="sxs-lookup"><span data-stu-id="95d66-131">xsd:string</span></span>  <br/> |<span data-ttu-id="95d66-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="95d66-132">optional</span></span>  <br/> ||<span data-ttu-id="95d66-133">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="95d66-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95d66-134">ID</span><span class="sxs-lookup"><span data-stu-id="95d66-134">ID</span></span>  <br/> |<span data-ttu-id="95d66-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="95d66-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="95d66-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="95d66-136">required</span></span>  <br/> ||<span data-ttu-id="95d66-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="95d66-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="95d66-138">Ignoré</span><span class="sxs-lookup"><span data-stu-id="95d66-138">Ignored</span></span>  <br/> |<span data-ttu-id="95d66-139">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="95d66-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="95d66-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="95d66-140">optional</span></span>  <br/> ||<span data-ttu-id="95d66-141">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="95d66-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="95d66-142">NameU</span><span class="sxs-lookup"><span data-stu-id="95d66-142">NameU</span></span>  <br/> |<span data-ttu-id="95d66-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="95d66-143">xsd:string</span></span>  <br/> |<span data-ttu-id="95d66-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="95d66-144">required</span></span>  <br/> ||<span data-ttu-id="95d66-145">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="95d66-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95d66-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="95d66-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="95d66-147">xsd: int</span><span class="sxs-lookup"><span data-stu-id="95d66-147">xsd:int</span></span>  <br/> |<span data-ttu-id="95d66-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="95d66-148">optional</span></span>  <br/> ||<span data-ttu-id="95d66-149">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="95d66-149">Values of the xsd:int type.</span></span>  <br/> |
   

