---
title: Connect_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9dee421915cb3e69ef5223280a425e785d29e4ec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538738"
---
# <a name="connect_type-complextype-visio-xml"></a><span data-ttu-id="b28d9-102">Connect_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b28d9-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b28d9-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="b28d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b28d9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b28d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b28d9-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b28d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b28d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b28d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b28d9-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="b28d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b28d9-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="b28d9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b28d9-109">Définition</span><span class="sxs-lookup"><span data-stu-id="b28d9-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b28d9-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b28d9-110">Elements and attributes</span></span>

<span data-ttu-id="b28d9-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="b28d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b28d9-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b28d9-112">Child elements</span></span>

<span data-ttu-id="b28d9-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b28d9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b28d9-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="b28d9-114">Attributes</span></span>

|<span data-ttu-id="b28d9-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b28d9-115">**Attribute**</span></span>|<span data-ttu-id="b28d9-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="b28d9-116">**Type**</span></span>|<span data-ttu-id="b28d9-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b28d9-117">**Required**</span></span>|<span data-ttu-id="b28d9-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b28d9-118">**Description**</span></span>|<span data-ttu-id="b28d9-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b28d9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b28d9-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="b28d9-120">FromCell</span></span>  <br/> |<span data-ttu-id="b28d9-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b28d9-121">xsd:string</span></span>  <br/> |<span data-ttu-id="b28d9-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="b28d9-122">optional</span></span>  <br/> ||<span data-ttu-id="b28d9-123">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b28d9-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b28d9-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="b28d9-124">FromPart</span></span>  <br/> |<span data-ttu-id="b28d9-125">xsd:int</span><span class="sxs-lookup"><span data-stu-id="b28d9-125">xsd:int</span></span>  <br/> |<span data-ttu-id="b28d9-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="b28d9-126">optional</span></span>  <br/> ||<span data-ttu-id="b28d9-127">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="b28d9-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="b28d9-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="b28d9-128">FromSheet</span></span>  <br/> |<span data-ttu-id="b28d9-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b28d9-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b28d9-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b28d9-130">required</span></span>  <br/> ||<span data-ttu-id="b28d9-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b28d9-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b28d9-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="b28d9-132">ToCell</span></span>  <br/> |<span data-ttu-id="b28d9-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b28d9-133">xsd:string</span></span>  <br/> |<span data-ttu-id="b28d9-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="b28d9-134">optional</span></span>  <br/> ||<span data-ttu-id="b28d9-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b28d9-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b28d9-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="b28d9-136">ToPart</span></span>  <br/> |<span data-ttu-id="b28d9-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="b28d9-137">xsd:int</span></span>  <br/> |<span data-ttu-id="b28d9-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="b28d9-138">optional</span></span>  <br/> ||<span data-ttu-id="b28d9-139">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="b28d9-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="b28d9-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="b28d9-140">ToSheet</span></span>  <br/> |<span data-ttu-id="b28d9-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b28d9-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b28d9-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b28d9-142">required</span></span>  <br/> ||<span data-ttu-id="b28d9-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b28d9-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

