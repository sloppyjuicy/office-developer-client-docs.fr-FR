---
title: Cell_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: 4e0cedaab755dab669d79ff52742b8ac2b9f9725
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542302"
---
# <a name="cell_type-complextype-visio-xml"></a><span data-ttu-id="9b24f-102">Cell_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9b24f-102">Cell_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9b24f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9b24f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b24f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9b24f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9b24f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9b24f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9b24f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9b24f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9b24f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9b24f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9b24f-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="9b24f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9b24f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9b24f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9b24f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9b24f-110">Elements and attributes</span></span>

<span data-ttu-id="9b24f-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="9b24f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9b24f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9b24f-112">Child elements</span></span>

|<span data-ttu-id="9b24f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9b24f-113">**Element**</span></span>|<span data-ttu-id="9b24f-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9b24f-114">**Type**</span></span>|<span data-ttu-id="9b24f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b24f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9b24f-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="9b24f-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9b24f-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="9b24f-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9b24f-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9b24f-118">Attributes</span></span>

|<span data-ttu-id="9b24f-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9b24f-119">**Attribute**</span></span>|<span data-ttu-id="9b24f-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="9b24f-120">**Type**</span></span>|<span data-ttu-id="9b24f-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9b24f-121">**Required**</span></span>|<span data-ttu-id="9b24f-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b24f-122">**Description**</span></span>|<span data-ttu-id="9b24f-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9b24f-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9b24f-124">E</span><span class="sxs-lookup"><span data-stu-id="9b24f-124">E</span></span>  <br/> |<span data-ttu-id="9b24f-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9b24f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9b24f-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="9b24f-126">optional</span></span>  <br/> ||<span data-ttu-id="9b24f-127">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9b24f-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9b24f-128">F</span><span class="sxs-lookup"><span data-stu-id="9b24f-128">F</span></span>  <br/> |<span data-ttu-id="9b24f-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9b24f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9b24f-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="9b24f-130">optional</span></span>  <br/> ||<span data-ttu-id="9b24f-131">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9b24f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9b24f-132">N</span><span class="sxs-lookup"><span data-stu-id="9b24f-132">N</span></span>  <br/> |<span data-ttu-id="9b24f-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9b24f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="9b24f-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9b24f-134">required</span></span>  <br/> ||<span data-ttu-id="9b24f-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9b24f-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9b24f-136">U</span><span class="sxs-lookup"><span data-stu-id="9b24f-136">U</span></span>  <br/> |<span data-ttu-id="9b24f-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9b24f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9b24f-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="9b24f-138">optional</span></span>  <br/> ||<span data-ttu-id="9b24f-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9b24f-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9b24f-140">V</span><span class="sxs-lookup"><span data-stu-id="9b24f-140">V</span></span>  <br/> |<span data-ttu-id="9b24f-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9b24f-141">xsd:string</span></span>  <br/> |<span data-ttu-id="9b24f-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="9b24f-142">optional</span></span>  <br/> ||<span data-ttu-id="9b24f-143">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9b24f-143">Values of the xsd:string type.</span></span>  <br/> |
   

