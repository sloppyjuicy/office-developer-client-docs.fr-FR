---
title: Élément PublishedPage (PublishSettings_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Indique si une page de dessin est visible dans le navigateur à l’aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 5cdbb03aaac3393c16c6ed0169842153374f668e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789374"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="ef49c-103">Élément PublishedPage (PublishSettings_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ef49c-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ef49c-104">Indique si une page de dessin est visible dans le navigateur à l’aide de Visio Services dans Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef49c-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef49c-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="ef49c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef49c-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ef49c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ef49c-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="ef49c-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ef49c-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ef49c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ef49c-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ef49c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ef49c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ef49c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ef49c-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ef49c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ef49c-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="ef49c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef49c-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ef49c-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef49c-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ef49c-114">Elements and attributes</span></span>

<span data-ttu-id="ef49c-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ef49c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ef49c-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ef49c-116">Parent elements</span></span>

|<span data-ttu-id="ef49c-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ef49c-117">**Element**</span></span>|<span data-ttu-id="ef49c-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ef49c-118">**Type**</span></span>|<span data-ttu-id="ef49c-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef49c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef49c-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="ef49c-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef49c-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ef49c-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef49c-122">Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l’aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="ef49c-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef49c-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef49c-123">Child elements</span></span>

<span data-ttu-id="ef49c-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ef49c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef49c-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef49c-125">Attributes</span></span>

|<span data-ttu-id="ef49c-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ef49c-126">**Attribute**</span></span>|<span data-ttu-id="ef49c-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="ef49c-127">**Type**</span></span>|<span data-ttu-id="ef49c-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ef49c-128">**Required**</span></span>|<span data-ttu-id="ef49c-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef49c-129">**Description**</span></span>|<span data-ttu-id="ef49c-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ef49c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ef49c-131">ID</span><span class="sxs-lookup"><span data-stu-id="ef49c-131">ID</span></span>  <br/> |<span data-ttu-id="ef49c-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ef49c-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ef49c-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ef49c-133">required</span></span>  <br/> |<span data-ttu-id="ef49c-134">L’identificateur d’une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="ef49c-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="ef49c-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ef49c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

