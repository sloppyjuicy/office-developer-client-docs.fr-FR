---
title: Type complexe SectionDef_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 1d13cf54861435aea2ce0b3aade955575d538891
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395076"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="1724f-102">Type complexe SectionDef_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1724f-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1724f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1724f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1724f-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1724f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1724f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1724f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1724f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1724f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1724f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1724f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1724f-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="1724f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1724f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1724f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1724f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1724f-110">Elements and attributes</span></span>

<span data-ttu-id="1724f-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1724f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1724f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1724f-112">Child elements</span></span>

|<span data-ttu-id="1724f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1724f-113">**Element**</span></span>|<span data-ttu-id="1724f-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="1724f-114">**Type**</span></span>|<span data-ttu-id="1724f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="1724f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1724f-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="1724f-116">CellDef</span></span> <br/> |[<span data-ttu-id="1724f-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="1724f-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="1724f-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="1724f-118">RowDef</span></span> <br/> |[<span data-ttu-id="1724f-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="1724f-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1724f-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="1724f-120">Attributes</span></span>

|<span data-ttu-id="1724f-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1724f-121">**Attribute**</span></span>|<span data-ttu-id="1724f-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="1724f-122">**Type**</span></span>|<span data-ttu-id="1724f-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1724f-123">**Required**</span></span>|<span data-ttu-id="1724f-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="1724f-124">**Description**</span></span>|<span data-ttu-id="1724f-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1724f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1724f-126">N</span><span class="sxs-lookup"><span data-stu-id="1724f-126">N</span></span>  <br/> |<span data-ttu-id="1724f-127">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1724f-127">xsd:string</span></span>  <br/> |<span data-ttu-id="1724f-128">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1724f-128">required</span></span>  <br/> ||<span data-ttu-id="1724f-129">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1724f-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1724f-130">S</span><span class="sxs-lookup"><span data-stu-id="1724f-130">S</span></span>  <br/> |<span data-ttu-id="1724f-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="1724f-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1724f-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="1724f-132">optional</span></span>  <br/> ||<span data-ttu-id="1724f-133">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="1724f-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1724f-134">T</span><span class="sxs-lookup"><span data-stu-id="1724f-134">T</span></span>  <br/> |<span data-ttu-id="1724f-135">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1724f-135">xsd:string</span></span>  <br/> |<span data-ttu-id="1724f-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="1724f-136">optional</span></span>  <br/> ||<span data-ttu-id="1724f-137">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1724f-137">Values of the xsd:string type.</span></span>  <br/> |
   

