---
title: Élément PublishSettings (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Spécifie les paramètres utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541357"
---
# <a name="publishsettings-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="d010d-103">Élément PublishSettings (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d010d-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="d010d-104">Spécifie les paramètres utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d010d-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d010d-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="d010d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d010d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="d010d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d010d-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="d010d-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d010d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d010d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d010d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d010d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d010d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d010d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d010d-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="d010d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d010d-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="d010d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d010d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="d010d-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d010d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d010d-114">Elements and attributes</span></span>

<span data-ttu-id="d010d-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="d010d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d010d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d010d-116">Parent elements</span></span>

|<span data-ttu-id="d010d-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d010d-117">**Element**</span></span>|<span data-ttu-id="d010d-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d010d-118">**Type**</span></span>|<span data-ttu-id="d010d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="d010d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d010d-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="d010d-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="d010d-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="d010d-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d010d-122">Spécifie les propriétés d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="d010d-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d010d-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d010d-123">Child elements</span></span>

|<span data-ttu-id="d010d-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d010d-124">**Element**</span></span>|<span data-ttu-id="d010d-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d010d-125">**Type**</span></span>|<span data-ttu-id="d010d-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="d010d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d010d-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="d010d-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d010d-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="d010d-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d010d-129">Spécifie si une page de dessin est consultable dans le navigateur à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="d010d-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="d010d-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="d010d-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d010d-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="d010d-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d010d-132">Spécifie si un recordset est actualisable à l’aide Visio Services.</span><span class="sxs-lookup"><span data-stu-id="d010d-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d010d-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="d010d-133">Attributes</span></span>

<span data-ttu-id="d010d-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d010d-134">None.</span></span>
  

