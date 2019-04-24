---
title: ComplexType VisioDocument_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: 3b794f4e7843b89dda2c23216478bc1b72f8753a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285264"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="babeb-102">ComplexType VisioDocument_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="babeb-102">VisioDocument_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="babeb-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="babeb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="babeb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="babeb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="babeb-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="babeb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="babeb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="babeb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="babeb-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="babeb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="babeb-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="babeb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="babeb-109">Définition</span><span class="sxs-lookup"><span data-stu-id="babeb-109">Definition</span></span>

```XML
          <xs:complexType name="VisioDocument_Type">
          
          <xs:sequence>
    <xs:element name="DocumentSettings"  type="DocumentSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Colors"  type="Colors_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FaceNames"  type="FaceNames_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StyleSheets"  type="StyleSheets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DocumentSheet"  type="DocumentSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="EventList"  type="EventList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooter"  type="HeaderFooter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PublishSettings"  type="PublishSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="babeb-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="babeb-110">Elements and attributes</span></span>

<span data-ttu-id="babeb-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="babeb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="babeb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="babeb-112">Child elements</span></span>

|<span data-ttu-id="babeb-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="babeb-113">**Element**</span></span>|<span data-ttu-id="babeb-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="babeb-114">**Type**</span></span>|<span data-ttu-id="babeb-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="babeb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="babeb-116">Colors</span><span class="sxs-lookup"><span data-stu-id="babeb-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="babeb-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="babeb-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="babeb-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="babeb-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="babeb-122">EventList</span><span class="sxs-lookup"><span data-stu-id="babeb-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="babeb-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="babeb-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="babeb-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="babeb-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="babeb-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="babeb-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="babeb-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="babeb-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="babeb-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="babeb-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="babeb-132">Attributs</span><span class="sxs-lookup"><span data-stu-id="babeb-132">Attributes</span></span>

<span data-ttu-id="babeb-133">Aucun.</span><span class="sxs-lookup"><span data-stu-id="babeb-133">None.</span></span>
  

