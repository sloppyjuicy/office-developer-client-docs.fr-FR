---
title: VisioDocument_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: 8c0a5976139aee2f3aee41b3709ce5fd1ac5c00d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538472"
---
# <a name="visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="391d8-102">VisioDocument_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="391d8-102">VisioDocument_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="391d8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="391d8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="391d8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="391d8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="391d8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="391d8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="391d8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="391d8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="391d8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="391d8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="391d8-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="391d8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="391d8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="391d8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="391d8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="391d8-110">Elements and attributes</span></span>

<span data-ttu-id="391d8-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="391d8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="391d8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="391d8-112">Child elements</span></span>

|<span data-ttu-id="391d8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="391d8-113">**Element**</span></span>|<span data-ttu-id="391d8-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="391d8-114">**Type**</span></span>|<span data-ttu-id="391d8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="391d8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="391d8-116">Colors</span><span class="sxs-lookup"><span data-stu-id="391d8-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="391d8-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="391d8-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="391d8-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="391d8-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="391d8-122">EventList</span><span class="sxs-lookup"><span data-stu-id="391d8-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="391d8-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="391d8-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="391d8-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="391d8-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="391d8-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="391d8-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="391d8-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="391d8-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="391d8-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="391d8-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="391d8-132">Attributs</span><span class="sxs-lookup"><span data-stu-id="391d8-132">Attributes</span></span>

<span data-ttu-id="391d8-133">Aucun.</span><span class="sxs-lookup"><span data-stu-id="391d8-133">None.</span></span>
  

