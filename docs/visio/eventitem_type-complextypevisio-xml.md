---
title: EventItem_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: f0fd618cc2a86d3695d0d6f6c446f118475ffc1f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541791"
---
# <a name="eventitem_type-complextype-visio-xml"></a><span data-ttu-id="6c614-102">EventItem_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6c614-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6c614-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6c614-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c614-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c614-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6c614-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6c614-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6c614-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6c614-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6c614-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6c614-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6c614-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="6c614-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c614-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6c614-109">Definition</span></span>

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6c614-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6c614-110">Elements and attributes</span></span>

<span data-ttu-id="6c614-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="6c614-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6c614-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6c614-112">Child elements</span></span>

<span data-ttu-id="6c614-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6c614-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c614-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="6c614-114">Attributes</span></span>

|<span data-ttu-id="6c614-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6c614-115">**Attribute**</span></span>|<span data-ttu-id="6c614-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="6c614-116">**Type**</span></span>|<span data-ttu-id="6c614-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="6c614-117">**Required**</span></span>|<span data-ttu-id="6c614-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c614-118">**Description**</span></span>|<span data-ttu-id="6c614-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="6c614-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6c614-120">Action</span><span class="sxs-lookup"><span data-stu-id="6c614-120">Action</span></span>  <br/> |<span data-ttu-id="6c614-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6c614-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6c614-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c614-122">required</span></span>  <br/> ||<span data-ttu-id="6c614-123">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6c614-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6c614-124">Activé</span><span class="sxs-lookup"><span data-stu-id="6c614-124">Enabled</span></span>  <br/> |<span data-ttu-id="6c614-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6c614-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6c614-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c614-126">optional</span></span>  <br/> ||<span data-ttu-id="6c614-127">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6c614-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6c614-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="6c614-128">EventCode</span></span>  <br/> |<span data-ttu-id="6c614-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6c614-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6c614-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c614-130">required</span></span>  <br/> ||<span data-ttu-id="6c614-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6c614-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6c614-132">ID</span><span class="sxs-lookup"><span data-stu-id="6c614-132">ID</span></span>  <br/> |<span data-ttu-id="6c614-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6c614-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6c614-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c614-134">required</span></span>  <br/> ||<span data-ttu-id="6c614-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6c614-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6c614-136">Target</span><span class="sxs-lookup"><span data-stu-id="6c614-136">Target</span></span>  <br/> |<span data-ttu-id="6c614-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6c614-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6c614-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c614-138">required</span></span>  <br/> ||<span data-ttu-id="6c614-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6c614-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c614-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="6c614-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="6c614-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6c614-141">xsd:string</span></span>  <br/> |<span data-ttu-id="6c614-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c614-142">required</span></span>  <br/> ||<span data-ttu-id="6c614-143">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6c614-143">Values of the xsd:string type.</span></span>  <br/> |
   

