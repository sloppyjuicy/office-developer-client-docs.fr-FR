---
title: ComplexType Cell_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327117"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="a9748-102">ComplexType Cell_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a9748-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a9748-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a9748-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9748-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a9748-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a9748-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a9748-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a9748-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a9748-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a9748-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a9748-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a9748-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="a9748-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a9748-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a9748-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a9748-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a9748-110">Elements and attributes</span></span>

<span data-ttu-id="a9748-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a9748-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a9748-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a9748-112">Child elements</span></span>

|<span data-ttu-id="a9748-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a9748-113">**Element**</span></span>|<span data-ttu-id="a9748-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a9748-114">**Type**</span></span>|<span data-ttu-id="a9748-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a9748-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a9748-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="a9748-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9748-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a9748-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a9748-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="a9748-118">Attributes</span></span>

|<span data-ttu-id="a9748-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a9748-119">**Attribute**</span></span>|<span data-ttu-id="a9748-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="a9748-120">**Type**</span></span>|<span data-ttu-id="a9748-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a9748-121">**Required**</span></span>|<span data-ttu-id="a9748-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="a9748-122">**Description**</span></span>|<span data-ttu-id="a9748-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a9748-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a9748-124">E</span><span class="sxs-lookup"><span data-stu-id="a9748-124">E</span></span>  <br/> |<span data-ttu-id="a9748-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a9748-125">xsd:string</span></span>  <br/> |<span data-ttu-id="a9748-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="a9748-126">optional</span></span>  <br/> ||<span data-ttu-id="a9748-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a9748-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a9748-128">F</span><span class="sxs-lookup"><span data-stu-id="a9748-128">F</span></span>  <br/> |<span data-ttu-id="a9748-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a9748-129">xsd:string</span></span>  <br/> |<span data-ttu-id="a9748-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="a9748-130">optional</span></span>  <br/> ||<span data-ttu-id="a9748-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a9748-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a9748-132">N</span><span class="sxs-lookup"><span data-stu-id="a9748-132">N</span></span>  <br/> |<span data-ttu-id="a9748-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a9748-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a9748-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a9748-134">required</span></span>  <br/> ||<span data-ttu-id="a9748-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a9748-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a9748-136">U</span><span class="sxs-lookup"><span data-stu-id="a9748-136">U</span></span>  <br/> |<span data-ttu-id="a9748-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a9748-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a9748-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="a9748-138">optional</span></span>  <br/> ||<span data-ttu-id="a9748-139">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a9748-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a9748-140">V</span><span class="sxs-lookup"><span data-stu-id="a9748-140">V</span></span>  <br/> |<span data-ttu-id="a9748-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a9748-141">xsd:string</span></span>  <br/> |<span data-ttu-id="a9748-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="a9748-142">optional</span></span>  <br/> ||<span data-ttu-id="a9748-143">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a9748-143">Values of the xsd:string type.</span></span>  <br/> |
   

