---
title: Élément RefBy (Trigger_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Spécifie une référence à une page dans le dessin.
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789406"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="22de7-103">Élément RefBy (Trigger_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="22de7-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="22de7-104">Spécifie une référence à une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="22de7-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22de7-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="22de7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22de7-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="22de7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="22de7-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="22de7-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="22de7-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="22de7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="22de7-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="22de7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="22de7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="22de7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="22de7-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="22de7-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="22de7-112">Définition</span><span class="sxs-lookup"><span data-stu-id="22de7-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="22de7-113">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="22de7-113">Elements and attributes</span></span>

<span data-ttu-id="22de7-114">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="22de7-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="22de7-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="22de7-115">Parent elements</span></span>

|<span data-ttu-id="22de7-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="22de7-116">**Element**</span></span>|<span data-ttu-id="22de7-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="22de7-117">**Type**</span></span>|<span data-ttu-id="22de7-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="22de7-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="22de7-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="22de7-119">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="22de7-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="22de7-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22de7-121">Fournit des instructions pour Microsoft Visio recalcule une relation entre les parties de document dans un fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="22de7-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="22de7-122">Trigger</span><span class="sxs-lookup"><span data-stu-id="22de7-122">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="22de7-123">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="22de7-123">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22de7-124">Fournit des instructions pour Microsoft Visio recalcule une relation entre les parties de document dans un fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="22de7-124">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="22de7-125">Trigger</span><span class="sxs-lookup"><span data-stu-id="22de7-125">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="22de7-126">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="22de7-126">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22de7-127">Fournit des instructions pour Microsoft Visio recalcule une relation entre les parties de document dans un fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="22de7-127">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="22de7-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="22de7-128">Child elements</span></span>

<span data-ttu-id="22de7-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="22de7-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22de7-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="22de7-130">Attributes</span></span>

|<span data-ttu-id="22de7-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="22de7-131">**Attribute**</span></span>|<span data-ttu-id="22de7-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="22de7-132">**Type**</span></span>|<span data-ttu-id="22de7-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="22de7-133">**Required**</span></span>|<span data-ttu-id="22de7-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="22de7-134">**Description**</span></span>|<span data-ttu-id="22de7-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="22de7-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="22de7-136">ID</span><span class="sxs-lookup"><span data-stu-id="22de7-136">ID</span></span>  <br/> |<span data-ttu-id="22de7-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="22de7-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="22de7-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22de7-138">required</span></span>  <br/> |<span data-ttu-id="22de7-139">Spécifie l’attribut ID d’une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="22de7-139">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="22de7-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="22de7-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="22de7-141">T</span><span class="sxs-lookup"><span data-stu-id="22de7-141">T</span></span>  <br/> |<span data-ttu-id="22de7-142">XSD : String</span><span class="sxs-lookup"><span data-stu-id="22de7-142">xsd:string</span></span>  <br/> |<span data-ttu-id="22de7-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22de7-143">required</span></span>  <br/> |<span data-ttu-id="22de7-144">Spécifie le type de référence.</span><span class="sxs-lookup"><span data-stu-id="22de7-144">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="22de7-145">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="22de7-145">Values of the xsd:string type.</span></span>  <br/> |
   

