---
title: Type complexe EventItem_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395727"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="177e6-102">Type complexe EventItem_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="177e6-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="177e6-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="177e6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="177e6-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="177e6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="177e6-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="177e6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="177e6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="177e6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="177e6-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="177e6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="177e6-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="177e6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="177e6-109">Définition</span><span class="sxs-lookup"><span data-stu-id="177e6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="177e6-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="177e6-110">Elements and attributes</span></span>

<span data-ttu-id="177e6-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="177e6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="177e6-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="177e6-112">Child elements</span></span>

<span data-ttu-id="177e6-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="177e6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="177e6-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="177e6-114">Attributes</span></span>

|<span data-ttu-id="177e6-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="177e6-115">**Attribute**</span></span>|<span data-ttu-id="177e6-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="177e6-116">**Type**</span></span>|<span data-ttu-id="177e6-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="177e6-117">**Required**</span></span>|<span data-ttu-id="177e6-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="177e6-118">**Description**</span></span>|<span data-ttu-id="177e6-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="177e6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="177e6-120">Opération</span><span class="sxs-lookup"><span data-stu-id="177e6-120">Action</span></span>  <br/> |<span data-ttu-id="177e6-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="177e6-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="177e6-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="177e6-122">required</span></span>  <br/> ||<span data-ttu-id="177e6-123">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="177e6-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="177e6-124">Activé</span><span class="sxs-lookup"><span data-stu-id="177e6-124">Enabled</span></span>  <br/> |<span data-ttu-id="177e6-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="177e6-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="177e6-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="177e6-126">optional</span></span>  <br/> ||<span data-ttu-id="177e6-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="177e6-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="177e6-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="177e6-128">EventCode</span></span>  <br/> |<span data-ttu-id="177e6-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="177e6-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="177e6-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="177e6-130">required</span></span>  <br/> ||<span data-ttu-id="177e6-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="177e6-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="177e6-132">ID</span><span class="sxs-lookup"><span data-stu-id="177e6-132">ID</span></span>  <br/> |<span data-ttu-id="177e6-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="177e6-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="177e6-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="177e6-134">required</span></span>  <br/> ||<span data-ttu-id="177e6-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="177e6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="177e6-136">Cible</span><span class="sxs-lookup"><span data-stu-id="177e6-136">Target</span></span>  <br/> |<span data-ttu-id="177e6-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="177e6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="177e6-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="177e6-138">required</span></span>  <br/> ||<span data-ttu-id="177e6-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="177e6-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="177e6-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="177e6-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="177e6-141">XSD : String</span><span class="sxs-lookup"><span data-stu-id="177e6-141">xsd:string</span></span>  <br/> |<span data-ttu-id="177e6-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="177e6-142">required</span></span>  <br/> ||<span data-ttu-id="177e6-143">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="177e6-143">Values of the xsd:string type.</span></span>  <br/> |
   

