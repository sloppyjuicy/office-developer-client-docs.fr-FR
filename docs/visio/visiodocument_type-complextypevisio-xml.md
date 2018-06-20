---
title: Type complexe VisioDocument_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: f56ec2f09ebd14683952c70b62f84cffb97f2e7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790029"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="1c890-102">Type complexe VisioDocument_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1c890-102">VisioDocument_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1c890-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1c890-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c890-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1c890-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1c890-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1c890-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1c890-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1c890-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1c890-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1c890-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1c890-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="1c890-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c890-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1c890-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1c890-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1c890-110">Elements and attributes</span></span>

<span data-ttu-id="1c890-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1c890-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1c890-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1c890-112">Child elements</span></span>

|<span data-ttu-id="1c890-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1c890-113">**Element**</span></span>|<span data-ttu-id="1c890-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="1c890-114">**Type**</span></span>|<span data-ttu-id="1c890-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c890-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c890-116">Couleurs</span><span class="sxs-lookup"><span data-stu-id="1c890-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c890-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="1c890-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c890-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="1c890-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c890-122">EventList</span><span class="sxs-lookup"><span data-stu-id="1c890-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c890-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="1c890-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c890-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="1c890-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c890-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="1c890-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c890-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="1c890-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c890-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="1c890-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1c890-132">Attributs</span><span class="sxs-lookup"><span data-stu-id="1c890-132">Attributes</span></span>

<span data-ttu-id="1c890-133">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1c890-133">None.</span></span>
  

