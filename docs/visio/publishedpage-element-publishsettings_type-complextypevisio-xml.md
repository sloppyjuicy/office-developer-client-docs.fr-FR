---
title: Élément PublishedPage (complexType PublishSettings_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Indique si une page de dessin est affichable dans le navigateur à l'aide de Visio Services dans Microsoft SharePoint Server 2013.
ms.openlocfilehash: 313cabbdd59930df67c807ee3c89df1a6e8c17a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326795"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="65583-103">Élément PublishedPage (complexType PublishSettings_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="65583-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="65583-104">Indique si une page de dessin est affichable dans le navigateur à l'aide de Visio Services dans Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="65583-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65583-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="65583-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65583-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="65583-106">**Element type**</span></span> <br/> |[<span data-ttu-id="65583-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="65583-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="65583-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65583-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="65583-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="65583-109">**Schema file**</span></span> <br/> |<span data-ttu-id="65583-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="65583-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="65583-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="65583-111">**Document parts**</span></span> <br/> |<span data-ttu-id="65583-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="65583-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65583-113">Définition</span><span class="sxs-lookup"><span data-stu-id="65583-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65583-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="65583-114">Elements and attributes</span></span>

<span data-ttu-id="65583-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="65583-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="65583-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="65583-116">Parent elements</span></span>

|<span data-ttu-id="65583-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="65583-117">**Element**</span></span>|<span data-ttu-id="65583-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="65583-118">**Type**</span></span>|<span data-ttu-id="65583-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="65583-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65583-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="65583-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65583-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="65583-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65583-122">Spécifie les paramètres qui sont utilisés lorsque le diagramme est ouvert à l'aide de Visio Services.</span><span class="sxs-lookup"><span data-stu-id="65583-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65583-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="65583-123">Child elements</span></span>

<span data-ttu-id="65583-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="65583-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65583-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="65583-125">Attributes</span></span>

|<span data-ttu-id="65583-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="65583-126">**Attribute**</span></span>|<span data-ttu-id="65583-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="65583-127">**Type**</span></span>|<span data-ttu-id="65583-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="65583-128">**Required**</span></span>|<span data-ttu-id="65583-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="65583-129">**Description**</span></span>|<span data-ttu-id="65583-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="65583-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65583-131">ID</span><span class="sxs-lookup"><span data-stu-id="65583-131">ID</span></span>  <br/> |<span data-ttu-id="65583-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65583-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65583-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="65583-133">required</span></span>  <br/> |<span data-ttu-id="65583-134">Identificateur d'une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="65583-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="65583-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="65583-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

