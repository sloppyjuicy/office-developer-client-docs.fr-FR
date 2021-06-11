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
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="f1846-103">Élément RefBy (Trigger_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f1846-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f1846-104">Spécifie une référence à une page du dessin.</span><span class="sxs-lookup"><span data-stu-id="f1846-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1846-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="f1846-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1846-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="f1846-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f1846-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="f1846-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f1846-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f1846-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f1846-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f1846-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f1846-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f1846-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f1846-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="f1846-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="f1846-112">Définition</span><span class="sxs-lookup"><span data-stu-id="f1846-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1846-113">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f1846-113">Elements and attributes</span></span>

<span data-ttu-id="f1846-114">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="f1846-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f1846-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f1846-115">Parent elements</span></span>

|<span data-ttu-id="f1846-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f1846-116">**Element**</span></span>|<span data-ttu-id="f1846-117">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f1846-117">**Type**</span></span>|<span data-ttu-id="f1846-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1846-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1846-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="f1846-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="f1846-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="f1846-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1846-121">Fournit des instructions à Microsoft Visio pour recalculer une relation entre les composants de document dans Visio fichier.</span><span class="sxs-lookup"><span data-stu-id="f1846-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="f1846-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f1846-122">Child elements</span></span>

<span data-ttu-id="f1846-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f1846-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1846-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="f1846-124">Attributes</span></span>

|<span data-ttu-id="f1846-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f1846-125">**Attribute**</span></span>|<span data-ttu-id="f1846-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="f1846-126">**Type**</span></span>|<span data-ttu-id="f1846-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f1846-127">**Required**</span></span>|<span data-ttu-id="f1846-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1846-128">**Description**</span></span>|<span data-ttu-id="f1846-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f1846-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f1846-130">ID</span><span class="sxs-lookup"><span data-stu-id="f1846-130">ID</span></span>  <br/> |<span data-ttu-id="f1846-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f1846-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f1846-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f1846-132">required</span></span>  <br/> |<span data-ttu-id="f1846-133">Spécifie l’attribut ID d’une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="f1846-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="f1846-134">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f1846-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f1846-135">T</span><span class="sxs-lookup"><span data-stu-id="f1846-135">T</span></span>  <br/> |<span data-ttu-id="f1846-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f1846-136">xsd:string</span></span>  <br/> |<span data-ttu-id="f1846-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f1846-137">required</span></span>  <br/> |<span data-ttu-id="f1846-138">Spécifie le type de référence.</span><span class="sxs-lookup"><span data-stu-id="f1846-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="f1846-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f1846-139">Values of the xsd:string type.</span></span>  <br/> |
   

