---
title: SectionDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 96812d1911d249ebce02aeab20b0a77ef518fbff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542078"
---
# <a name="sectiondef_type-complextype-visio-xml"></a><span data-ttu-id="d0e51-102">SectionDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d0e51-102">SectionDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d0e51-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="d0e51-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0e51-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0e51-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d0e51-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d0e51-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d0e51-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d0e51-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d0e51-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="d0e51-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d0e51-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="d0e51-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0e51-109">Définition</span><span class="sxs-lookup"><span data-stu-id="d0e51-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0e51-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d0e51-110">Elements and attributes</span></span>

<span data-ttu-id="d0e51-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="d0e51-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d0e51-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d0e51-112">Child elements</span></span>

|<span data-ttu-id="d0e51-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d0e51-113">**Element**</span></span>|<span data-ttu-id="d0e51-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d0e51-114">**Type**</span></span>|<span data-ttu-id="d0e51-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0e51-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0e51-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="d0e51-116">CellDef</span></span> <br/> |[<span data-ttu-id="d0e51-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="d0e51-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="d0e51-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="d0e51-118">RowDef</span></span> <br/> |[<span data-ttu-id="d0e51-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="d0e51-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d0e51-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="d0e51-120">Attributes</span></span>

|<span data-ttu-id="d0e51-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d0e51-121">**Attribute**</span></span>|<span data-ttu-id="d0e51-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="d0e51-122">**Type**</span></span>|<span data-ttu-id="d0e51-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d0e51-123">**Required**</span></span>|<span data-ttu-id="d0e51-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0e51-124">**Description**</span></span>|<span data-ttu-id="d0e51-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d0e51-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0e51-126">N</span><span class="sxs-lookup"><span data-stu-id="d0e51-126">N</span></span>  <br/> |<span data-ttu-id="d0e51-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d0e51-127">xsd:string</span></span>  <br/> |<span data-ttu-id="d0e51-128">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d0e51-128">required</span></span>  <br/> ||<span data-ttu-id="d0e51-129">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d0e51-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0e51-130">S</span><span class="sxs-lookup"><span data-stu-id="d0e51-130">S</span></span>  <br/> |<span data-ttu-id="d0e51-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d0e51-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d0e51-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="d0e51-132">optional</span></span>  <br/> ||<span data-ttu-id="d0e51-133">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="d0e51-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d0e51-134">T</span><span class="sxs-lookup"><span data-stu-id="d0e51-134">T</span></span>  <br/> |<span data-ttu-id="d0e51-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d0e51-135">xsd:string</span></span>  <br/> |<span data-ttu-id="d0e51-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="d0e51-136">optional</span></span>  <br/> ||<span data-ttu-id="d0e51-137">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d0e51-137">Values of the xsd:string type.</span></span>  <br/> |
   

