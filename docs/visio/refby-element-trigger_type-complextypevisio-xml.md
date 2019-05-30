---
title: Élément RefBy (complexType Trigger_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Cette énumération spécifie une référence à une page dans le dessin.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538290"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="b824d-103">Élément RefBy (complexType Trigger_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="b824d-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b824d-104">Cette énumération spécifie une référence à une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="b824d-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b824d-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="b824d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b824d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="b824d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b824d-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="b824d-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b824d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b824d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b824d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b824d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b824d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b824d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b824d-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="b824d-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="b824d-112">Définition</span><span class="sxs-lookup"><span data-stu-id="b824d-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b824d-113">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b824d-113">Elements and attributes</span></span>

<span data-ttu-id="b824d-114">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="b824d-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b824d-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b824d-115">Parent elements</span></span>

|<span data-ttu-id="b824d-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b824d-116">**Element**</span></span>|<span data-ttu-id="b824d-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="b824d-117">**Type**</span></span>|<span data-ttu-id="b824d-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b824d-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b824d-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="b824d-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="b824d-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="b824d-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b824d-121">Fournit des instructions à Microsoft Visio pour recalculer une relation entre des parties de document dans un fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="b824d-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="b824d-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b824d-122">Child elements</span></span>

<span data-ttu-id="b824d-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b824d-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b824d-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="b824d-124">Attributes</span></span>

|<span data-ttu-id="b824d-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b824d-125">**Attribute**</span></span>|<span data-ttu-id="b824d-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="b824d-126">**Type**</span></span>|<span data-ttu-id="b824d-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b824d-127">**Required**</span></span>|<span data-ttu-id="b824d-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="b824d-128">**Description**</span></span>|<span data-ttu-id="b824d-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b824d-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b824d-130">ID</span><span class="sxs-lookup"><span data-stu-id="b824d-130">ID</span></span>  <br/> |<span data-ttu-id="b824d-131">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b824d-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b824d-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b824d-132">required</span></span>  <br/> |<span data-ttu-id="b824d-133">Spécifie l’attribut ID d’une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="b824d-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="b824d-134">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b824d-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b824d-135">T</span><span class="sxs-lookup"><span data-stu-id="b824d-135">T</span></span>  <br/> |<span data-ttu-id="b824d-136">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b824d-136">xsd:string</span></span>  <br/> |<span data-ttu-id="b824d-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b824d-137">required</span></span>  <br/> |<span data-ttu-id="b824d-138">Spécifie le type de référence.</span><span class="sxs-lookup"><span data-stu-id="b824d-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="b824d-139">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b824d-139">Values of the xsd:string type.</span></span>  <br/> |
   

