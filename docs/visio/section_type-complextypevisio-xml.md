---
title: Type complexe Section_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 8eb9362f84849ad22a20662b327ae33cd795cc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789602"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="cefb7-102">Type complexe Section_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="cefb7-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cefb7-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="cefb7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cefb7-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="cefb7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cefb7-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="cefb7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cefb7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cefb7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cefb7-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="cefb7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cefb7-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="cefb7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cefb7-109">Définition</span><span class="sxs-lookup"><span data-stu-id="cefb7-109">Definition</span></span>

```XML
          <xs:complexType name="Section_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="Row_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cefb7-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="cefb7-110">Elements and attributes</span></span>

<span data-ttu-id="cefb7-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="cefb7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cefb7-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cefb7-112">Child elements</span></span>

|<span data-ttu-id="cefb7-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="cefb7-113">**Element**</span></span>|<span data-ttu-id="cefb7-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="cefb7-114">**Type**</span></span>|<span data-ttu-id="cefb7-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="cefb7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cefb7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="cefb7-116">Cell</span></span>](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[<span data-ttu-id="cefb7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="cefb7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cefb7-118">Row</span><span class="sxs-lookup"><span data-stu-id="cefb7-118">Row</span></span>](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="cefb7-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="cefb7-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cefb7-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="cefb7-120">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="cefb7-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="cefb7-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cefb7-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="cefb7-122">Attributes</span></span>

|<span data-ttu-id="cefb7-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cefb7-123">**Attribute**</span></span>|<span data-ttu-id="cefb7-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="cefb7-124">**Type**</span></span>|<span data-ttu-id="cefb7-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="cefb7-125">**Required**</span></span>|<span data-ttu-id="cefb7-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="cefb7-126">**Description**</span></span>|<span data-ttu-id="cefb7-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="cefb7-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cefb7-128">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="cefb7-128">Del</span></span>  <br/> |<span data-ttu-id="cefb7-129">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="cefb7-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cefb7-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="cefb7-130">optional</span></span>  <br/> ||<span data-ttu-id="cefb7-131">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="cefb7-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cefb7-132">IX</span><span class="sxs-lookup"><span data-stu-id="cefb7-132">IX</span></span>  <br/> |<span data-ttu-id="cefb7-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cefb7-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cefb7-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="cefb7-134">optional</span></span>  <br/> ||<span data-ttu-id="cefb7-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cefb7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cefb7-136">N</span><span class="sxs-lookup"><span data-stu-id="cefb7-136">N</span></span>  <br/> |<span data-ttu-id="cefb7-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="cefb7-137">xsd:string</span></span>  <br/> |<span data-ttu-id="cefb7-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cefb7-138">required</span></span>  <br/> ||<span data-ttu-id="cefb7-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="cefb7-139">Values of the xsd:string type.</span></span>  <br/> |
   

