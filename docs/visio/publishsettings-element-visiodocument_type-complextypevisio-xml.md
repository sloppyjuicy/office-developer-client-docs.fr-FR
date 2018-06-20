---
title: Élément PublishSettings (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: f2554facc47de23104f65b26ae19cfc71821bd37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789377"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="11404-103">Élément PublishSettings (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="11404-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="11404-104">Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="11404-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11404-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="11404-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11404-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="11404-106">**Element type**</span></span> <br/> |[<span data-ttu-id="11404-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="11404-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="11404-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="11404-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="11404-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="11404-109">**Schema file**</span></span> <br/> |<span data-ttu-id="11404-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="11404-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="11404-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="11404-111">**Document parts**</span></span> <br/> |<span data-ttu-id="11404-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="11404-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11404-113">Définition</span><span class="sxs-lookup"><span data-stu-id="11404-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11404-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="11404-114">Elements and attributes</span></span>

<span data-ttu-id="11404-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="11404-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="11404-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="11404-116">Parent elements</span></span>

|<span data-ttu-id="11404-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="11404-117">**Element**</span></span>|<span data-ttu-id="11404-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="11404-118">**Type**</span></span>|<span data-ttu-id="11404-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="11404-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11404-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="11404-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="11404-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="11404-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="11404-122">Spécifie les propriétés d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="11404-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="11404-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="11404-123">Child elements</span></span>

|<span data-ttu-id="11404-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="11404-124">**Element**</span></span>|<span data-ttu-id="11404-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="11404-125">**Type**</span></span>|<span data-ttu-id="11404-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="11404-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11404-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="11404-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="11404-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="11404-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="11404-129">Indique si une page de dessin est visible dans le navigateur à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="11404-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="11404-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="11404-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="11404-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="11404-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="11404-132">Indique si un objet recordset actualisable à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="11404-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="11404-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="11404-133">Attributes</span></span>

<span data-ttu-id="11404-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="11404-134">None.</span></span>
  

