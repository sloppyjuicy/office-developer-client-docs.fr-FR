---
title: Type complexe RuleSet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: dfb0d50cd1c39be9b98a880028b5c4b4dc597bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789581"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="ce77a-102">Type complexe RuleSet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ce77a-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ce77a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ce77a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce77a-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ce77a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ce77a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ce77a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ce77a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ce77a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ce77a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ce77a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ce77a-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="ce77a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ce77a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ce77a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ce77a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ce77a-110">Elements and attributes</span></span>

<span data-ttu-id="ce77a-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ce77a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ce77a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ce77a-112">Child elements</span></span>

|<span data-ttu-id="ce77a-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ce77a-113">**Element**</span></span>|<span data-ttu-id="ce77a-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ce77a-114">**Type**</span></span>|<span data-ttu-id="ce77a-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ce77a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce77a-116">Règle</span><span class="sxs-lookup"><span data-stu-id="ce77a-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce77a-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="ce77a-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ce77a-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="ce77a-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce77a-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="ce77a-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ce77a-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="ce77a-120">Attributes</span></span>

|<span data-ttu-id="ce77a-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ce77a-121">**Attribute**</span></span>|<span data-ttu-id="ce77a-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="ce77a-122">**Type**</span></span>|<span data-ttu-id="ce77a-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ce77a-123">**Required**</span></span>|<span data-ttu-id="ce77a-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="ce77a-124">**Description**</span></span>|<span data-ttu-id="ce77a-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ce77a-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ce77a-126">Description</span><span class="sxs-lookup"><span data-stu-id="ce77a-126">Description</span></span>  <br/> |<span data-ttu-id="ce77a-127">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ce77a-127">xsd:string</span></span>  <br/> |<span data-ttu-id="ce77a-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="ce77a-128">optional</span></span>  <br/> ||<span data-ttu-id="ce77a-129">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ce77a-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ce77a-130">Activé</span><span class="sxs-lookup"><span data-stu-id="ce77a-130">Enabled</span></span>  <br/> |<span data-ttu-id="ce77a-131">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="ce77a-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ce77a-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="ce77a-132">optional</span></span>  <br/> ||<span data-ttu-id="ce77a-133">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="ce77a-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ce77a-134">ID</span><span class="sxs-lookup"><span data-stu-id="ce77a-134">ID</span></span>  <br/> |<span data-ttu-id="ce77a-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ce77a-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ce77a-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ce77a-136">required</span></span>  <br/> ||<span data-ttu-id="ce77a-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ce77a-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ce77a-138">Nom</span><span class="sxs-lookup"><span data-stu-id="ce77a-138">Name</span></span>  <br/> |<span data-ttu-id="ce77a-139">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ce77a-139">xsd:string</span></span>  <br/> |<span data-ttu-id="ce77a-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="ce77a-140">optional</span></span>  <br/> ||<span data-ttu-id="ce77a-141">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ce77a-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ce77a-142">NameU</span><span class="sxs-lookup"><span data-stu-id="ce77a-142">NameU</span></span>  <br/> |<span data-ttu-id="ce77a-143">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ce77a-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ce77a-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ce77a-144">required</span></span>  <br/> ||<span data-ttu-id="ce77a-145">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ce77a-145">Values of the xsd:string type.</span></span>  <br/> |
   

