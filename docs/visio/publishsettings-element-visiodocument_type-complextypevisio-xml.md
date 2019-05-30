---
title: Élément PublishSettings (complexType VisioDocument_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541357"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ef8ae-103">Élément PublishSettings (complexType VisioDocument_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ef8ae-104">Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef8ae-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="ef8ae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef8ae-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ef8ae-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ef8ae-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ef8ae-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ef8ae-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ef8ae-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ef8ae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ef8ae-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ef8ae-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="ef8ae-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef8ae-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ef8ae-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef8ae-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ef8ae-114">Elements and attributes</span></span>

<span data-ttu-id="ef8ae-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ef8ae-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ef8ae-116">Parent elements</span></span>

|<span data-ttu-id="ef8ae-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-117">**Element**</span></span>|<span data-ttu-id="ef8ae-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-118">**Type**</span></span>|<span data-ttu-id="ef8ae-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef8ae-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ef8ae-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ef8ae-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ef8ae-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef8ae-122">Spécifie les propriétés d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef8ae-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef8ae-123">Child elements</span></span>

|<span data-ttu-id="ef8ae-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-124">**Element**</span></span>|<span data-ttu-id="ef8ae-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-125">**Type**</span></span>|<span data-ttu-id="ef8ae-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef8ae-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="ef8ae-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef8ae-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="ef8ae-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef8ae-129">Indique si une page de dessin est affichable dans le navigateur à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="ef8ae-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="ef8ae-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef8ae-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="ef8ae-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef8ae-132">Indique si un objet Recordset est actualisable à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ef8ae-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef8ae-133">Attributes</span></span>

<span data-ttu-id="ef8ae-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-134">None.</span></span>
  

