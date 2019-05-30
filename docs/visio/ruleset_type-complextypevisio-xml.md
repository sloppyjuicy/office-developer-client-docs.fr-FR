---
title: ComplexType RuleSet_Type (Visio XML)
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
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="69ffb-102">ComplexType RuleSet_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="69ffb-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="69ffb-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="69ffb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69ffb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="69ffb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="69ffb-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="69ffb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="69ffb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="69ffb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="69ffb-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="69ffb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="69ffb-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="69ffb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69ffb-109">Définition</span><span class="sxs-lookup"><span data-stu-id="69ffb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="69ffb-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="69ffb-110">Elements and attributes</span></span>

<span data-ttu-id="69ffb-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="69ffb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="69ffb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="69ffb-112">Child elements</span></span>

|<span data-ttu-id="69ffb-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="69ffb-113">**Element**</span></span>|<span data-ttu-id="69ffb-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="69ffb-114">**Type**</span></span>|<span data-ttu-id="69ffb-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="69ffb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69ffb-116">Règle</span><span class="sxs-lookup"><span data-stu-id="69ffb-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69ffb-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="69ffb-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69ffb-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="69ffb-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69ffb-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="69ffb-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="69ffb-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="69ffb-120">Attributes</span></span>

|<span data-ttu-id="69ffb-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="69ffb-121">**Attribute**</span></span>|<span data-ttu-id="69ffb-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="69ffb-122">**Type**</span></span>|<span data-ttu-id="69ffb-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="69ffb-123">**Required**</span></span>|<span data-ttu-id="69ffb-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="69ffb-124">**Description**</span></span>|<span data-ttu-id="69ffb-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="69ffb-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="69ffb-126">Description</span><span class="sxs-lookup"><span data-stu-id="69ffb-126">Description</span></span>  <br/> |<span data-ttu-id="69ffb-127">xsd: String</span><span class="sxs-lookup"><span data-stu-id="69ffb-127">xsd:string</span></span>  <br/> |<span data-ttu-id="69ffb-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="69ffb-128">optional</span></span>  <br/> ||<span data-ttu-id="69ffb-129">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="69ffb-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="69ffb-130">Activé</span><span class="sxs-lookup"><span data-stu-id="69ffb-130">Enabled</span></span>  <br/> |<span data-ttu-id="69ffb-131">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="69ffb-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="69ffb-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="69ffb-132">optional</span></span>  <br/> ||<span data-ttu-id="69ffb-133">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="69ffb-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="69ffb-134">ID</span><span class="sxs-lookup"><span data-stu-id="69ffb-134">ID</span></span>  <br/> |<span data-ttu-id="69ffb-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69ffb-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69ffb-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="69ffb-136">required</span></span>  <br/> ||<span data-ttu-id="69ffb-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="69ffb-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69ffb-138">Nom</span><span class="sxs-lookup"><span data-stu-id="69ffb-138">Name</span></span>  <br/> |<span data-ttu-id="69ffb-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="69ffb-139">xsd:string</span></span>  <br/> |<span data-ttu-id="69ffb-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="69ffb-140">optional</span></span>  <br/> ||<span data-ttu-id="69ffb-141">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="69ffb-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="69ffb-142">NameU</span><span class="sxs-lookup"><span data-stu-id="69ffb-142">NameU</span></span>  <br/> |<span data-ttu-id="69ffb-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="69ffb-143">xsd:string</span></span>  <br/> |<span data-ttu-id="69ffb-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="69ffb-144">required</span></span>  <br/> ||<span data-ttu-id="69ffb-145">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="69ffb-145">Values of the xsd:string type.</span></span>  <br/> |
   

