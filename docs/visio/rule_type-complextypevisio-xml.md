---
title: Type complexe Rule_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 380c59d659c820f0c5452ce37fa3616e1408a86c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789568"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="48b30-102">Type complexe Rule_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="48b30-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="48b30-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="48b30-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48b30-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="48b30-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="48b30-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="48b30-105">**Schema file**</span></span> <br/> |<span data-ttu-id="48b30-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="48b30-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="48b30-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="48b30-107">**Extension base**</span></span> <br/> |<span data-ttu-id="48b30-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="48b30-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48b30-109">Définition</span><span class="sxs-lookup"><span data-stu-id="48b30-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="48b30-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="48b30-110">Elements and attributes</span></span>

<span data-ttu-id="48b30-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="48b30-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="48b30-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="48b30-112">Child elements</span></span>

|<span data-ttu-id="48b30-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="48b30-113">**Element**</span></span>|<span data-ttu-id="48b30-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="48b30-114">**Type**</span></span>|<span data-ttu-id="48b30-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="48b30-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48b30-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="48b30-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48b30-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="48b30-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48b30-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="48b30-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48b30-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="48b30-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="48b30-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="48b30-120">Attributes</span></span>

|<span data-ttu-id="48b30-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="48b30-121">**Attribute**</span></span>|<span data-ttu-id="48b30-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="48b30-122">**Type**</span></span>|<span data-ttu-id="48b30-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="48b30-123">**Required**</span></span>|<span data-ttu-id="48b30-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="48b30-124">**Description**</span></span>|<span data-ttu-id="48b30-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="48b30-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48b30-126">Category</span><span class="sxs-lookup"><span data-stu-id="48b30-126">Category</span></span>  <br/> |<span data-ttu-id="48b30-127">XSD : String</span><span class="sxs-lookup"><span data-stu-id="48b30-127">xsd:string</span></span>  <br/> |<span data-ttu-id="48b30-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="48b30-128">optional</span></span>  <br/> ||<span data-ttu-id="48b30-129">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="48b30-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="48b30-130">Description</span><span class="sxs-lookup"><span data-stu-id="48b30-130">Description</span></span>  <br/> |<span data-ttu-id="48b30-131">XSD : String</span><span class="sxs-lookup"><span data-stu-id="48b30-131">xsd:string</span></span>  <br/> |<span data-ttu-id="48b30-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="48b30-132">optional</span></span>  <br/> ||<span data-ttu-id="48b30-133">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="48b30-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="48b30-134">ID</span><span class="sxs-lookup"><span data-stu-id="48b30-134">ID</span></span>  <br/> |<span data-ttu-id="48b30-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="48b30-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="48b30-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="48b30-136">required</span></span>  <br/> ||<span data-ttu-id="48b30-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="48b30-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="48b30-138">Ignoré</span><span class="sxs-lookup"><span data-stu-id="48b30-138">Ignored</span></span>  <br/> |<span data-ttu-id="48b30-139">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="48b30-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="48b30-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="48b30-140">optional</span></span>  <br/> ||<span data-ttu-id="48b30-141">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="48b30-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="48b30-142">NameU</span><span class="sxs-lookup"><span data-stu-id="48b30-142">NameU</span></span>  <br/> |<span data-ttu-id="48b30-143">XSD : String</span><span class="sxs-lookup"><span data-stu-id="48b30-143">xsd:string</span></span>  <br/> |<span data-ttu-id="48b30-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="48b30-144">required</span></span>  <br/> ||<span data-ttu-id="48b30-145">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="48b30-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="48b30-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="48b30-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="48b30-147">XSD : int</span><span class="sxs-lookup"><span data-stu-id="48b30-147">xsd:int</span></span>  <br/> |<span data-ttu-id="48b30-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="48b30-148">optional</span></span>  <br/> ||<span data-ttu-id="48b30-149">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="48b30-149">Values of the xsd:int type.</span></span>  <br/> |
   

