---
title: Élément PublishSettings (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 7e926021180d0f32c5e8754fd856081908f4925d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397211"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="87d79-103">Élément PublishSettings (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="87d79-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="87d79-104">Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services dans Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="87d79-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87d79-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="87d79-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87d79-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="87d79-106">**Element type**</span></span> <br/> |[<span data-ttu-id="87d79-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="87d79-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="87d79-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="87d79-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="87d79-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="87d79-109">**Schema file**</span></span> <br/> |<span data-ttu-id="87d79-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="87d79-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="87d79-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="87d79-111">**Document parts**</span></span> <br/> |<span data-ttu-id="87d79-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="87d79-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87d79-113">Définition</span><span class="sxs-lookup"><span data-stu-id="87d79-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87d79-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="87d79-114">Elements and attributes</span></span>

<span data-ttu-id="87d79-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="87d79-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="87d79-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="87d79-116">Parent elements</span></span>

|<span data-ttu-id="87d79-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="87d79-117">**Element**</span></span>|<span data-ttu-id="87d79-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="87d79-118">**Type**</span></span>|<span data-ttu-id="87d79-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="87d79-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87d79-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="87d79-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="87d79-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="87d79-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87d79-122">Spécifie les propriétés d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="87d79-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87d79-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="87d79-123">Child elements</span></span>

|<span data-ttu-id="87d79-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="87d79-124">**Element**</span></span>|<span data-ttu-id="87d79-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="87d79-125">**Type**</span></span>|<span data-ttu-id="87d79-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="87d79-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87d79-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="87d79-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87d79-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="87d79-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87d79-129">Indique si une page de dessin est visible dans le navigateur à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="87d79-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="87d79-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="87d79-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87d79-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="87d79-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87d79-132">Indique si un objet recordset actualisable à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="87d79-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="87d79-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="87d79-133">Attributes</span></span>

<span data-ttu-id="87d79-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87d79-134">None.</span></span>
  

