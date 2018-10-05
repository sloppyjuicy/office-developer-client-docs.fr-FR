---
title: Type complexe Connect_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 158fad1f3ec18bbc9565229338f4710c145c17e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383912"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="59a6d-102">Type complexe Connect_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="59a6d-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="59a6d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="59a6d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59a6d-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="59a6d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="59a6d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="59a6d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="59a6d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="59a6d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="59a6d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="59a6d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="59a6d-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="59a6d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59a6d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="59a6d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="59a6d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="59a6d-110">Elements and attributes</span></span>

<span data-ttu-id="59a6d-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="59a6d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="59a6d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="59a6d-112">Child elements</span></span>

<span data-ttu-id="59a6d-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="59a6d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59a6d-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="59a6d-114">Attributes</span></span>

|<span data-ttu-id="59a6d-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="59a6d-115">**Attribute**</span></span>|<span data-ttu-id="59a6d-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="59a6d-116">**Type**</span></span>|<span data-ttu-id="59a6d-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="59a6d-117">**Required**</span></span>|<span data-ttu-id="59a6d-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="59a6d-118">**Description**</span></span>|<span data-ttu-id="59a6d-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="59a6d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="59a6d-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="59a6d-120">FromCell</span></span>  <br/> |<span data-ttu-id="59a6d-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="59a6d-121">xsd:string</span></span>  <br/> |<span data-ttu-id="59a6d-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="59a6d-122">optional</span></span>  <br/> ||<span data-ttu-id="59a6d-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="59a6d-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59a6d-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="59a6d-124">FromPart</span></span>  <br/> |<span data-ttu-id="59a6d-125">XSD : int</span><span class="sxs-lookup"><span data-stu-id="59a6d-125">xsd:int</span></span>  <br/> |<span data-ttu-id="59a6d-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="59a6d-126">optional</span></span>  <br/> ||<span data-ttu-id="59a6d-127">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="59a6d-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="59a6d-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="59a6d-128">FromSheet</span></span>  <br/> |<span data-ttu-id="59a6d-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="59a6d-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59a6d-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="59a6d-130">required</span></span>  <br/> ||<span data-ttu-id="59a6d-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="59a6d-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="59a6d-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="59a6d-132">ToCell</span></span>  <br/> |<span data-ttu-id="59a6d-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="59a6d-133">xsd:string</span></span>  <br/> |<span data-ttu-id="59a6d-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="59a6d-134">optional</span></span>  <br/> ||<span data-ttu-id="59a6d-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="59a6d-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59a6d-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="59a6d-136">ToPart</span></span>  <br/> |<span data-ttu-id="59a6d-137">XSD : int</span><span class="sxs-lookup"><span data-stu-id="59a6d-137">xsd:int</span></span>  <br/> |<span data-ttu-id="59a6d-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="59a6d-138">optional</span></span>  <br/> ||<span data-ttu-id="59a6d-139">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="59a6d-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="59a6d-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="59a6d-140">ToSheet</span></span>  <br/> |<span data-ttu-id="59a6d-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="59a6d-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59a6d-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="59a6d-142">required</span></span>  <br/> ||<span data-ttu-id="59a6d-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="59a6d-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

