---
title: Élément RefBy (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Spécifie une référence à une page du dessin.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538290"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="7ddc2-103">Élément RefBy (Trigger_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7ddc2-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7ddc2-104">Spécifie une référence à une page du dessin.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ddc2-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="7ddc2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ddc2-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7ddc2-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="7ddc2-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7ddc2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7ddc2-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7ddc2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7ddc2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7ddc2-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="7ddc2-112">Définition</span><span class="sxs-lookup"><span data-stu-id="7ddc2-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7ddc2-113">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7ddc2-113">Elements and attributes</span></span>

<span data-ttu-id="7ddc2-114">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7ddc2-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7ddc2-115">Parent elements</span></span>

|<span data-ttu-id="7ddc2-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-116">**Element**</span></span>|<span data-ttu-id="7ddc2-117">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-117">**Type**</span></span>|<span data-ttu-id="7ddc2-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7ddc2-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="7ddc2-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="7ddc2-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="7ddc2-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7ddc2-121">Fournit des instructions à Microsoft Visio pour recalculer une relation entre les composants de document dans un fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="7ddc2-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7ddc2-122">Child elements</span></span>

<span data-ttu-id="7ddc2-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ddc2-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="7ddc2-124">Attributes</span></span>

|<span data-ttu-id="7ddc2-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-125">**Attribute**</span></span>|<span data-ttu-id="7ddc2-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-126">**Type**</span></span>|<span data-ttu-id="7ddc2-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-127">**Required**</span></span>|<span data-ttu-id="7ddc2-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-128">**Description**</span></span>|<span data-ttu-id="7ddc2-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7ddc2-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7ddc2-130">ID</span><span class="sxs-lookup"><span data-stu-id="7ddc2-130">ID</span></span>  <br/> |<span data-ttu-id="7ddc2-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7ddc2-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7ddc2-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ddc2-132">required</span></span>  <br/> |<span data-ttu-id="7ddc2-133">Spécifie l’attribut ID d’une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="7ddc2-134">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7ddc2-135">T</span><span class="sxs-lookup"><span data-stu-id="7ddc2-135">T</span></span>  <br/> |<span data-ttu-id="7ddc2-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7ddc2-136">xsd:string</span></span>  <br/> |<span data-ttu-id="7ddc2-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ddc2-137">required</span></span>  <br/> |<span data-ttu-id="7ddc2-138">Spécifie le type de référence.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="7ddc2-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7ddc2-139">Values of the xsd:string type.</span></span>  <br/> |
   

