---
title: Type complexe FaceName_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382441"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="e0bd1-102">Type complexe FaceName_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e0bd1-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e0bd1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e0bd1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0bd1-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e0bd1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e0bd1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e0bd1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e0bd1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e0bd1-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="e0bd1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0bd1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e0bd1-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0bd1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e0bd1-110">Elements and attributes</span></span>

<span data-ttu-id="e0bd1-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e0bd1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e0bd1-112">Child elements</span></span>

<span data-ttu-id="e0bd1-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0bd1-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="e0bd1-114">Attributes</span></span>

|<span data-ttu-id="e0bd1-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-115">**Attribute**</span></span>|<span data-ttu-id="e0bd1-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-116">**Type**</span></span>|<span data-ttu-id="e0bd1-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-117">**Required**</span></span>|<span data-ttu-id="e0bd1-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-118">**Description**</span></span>|<span data-ttu-id="e0bd1-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e0bd1-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0bd1-120">Jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="e0bd1-120">CharSets</span></span>  <br/> |<span data-ttu-id="e0bd1-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0bd1-121">xsd:string</span></span>  <br/> |<span data-ttu-id="e0bd1-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0bd1-122">optional</span></span>  <br/> ||<span data-ttu-id="e0bd1-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0bd1-124">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="e0bd1-124">Flags</span></span>  <br/> |<span data-ttu-id="e0bd1-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0bd1-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0bd1-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0bd1-126">optional</span></span>  <br/> ||<span data-ttu-id="e0bd1-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0bd1-128">NameU</span><span class="sxs-lookup"><span data-stu-id="e0bd1-128">NameU</span></span>  <br/> |<span data-ttu-id="e0bd1-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0bd1-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e0bd1-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e0bd1-130">required</span></span>  <br/> ||<span data-ttu-id="e0bd1-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0bd1-132">Panos</span><span class="sxs-lookup"><span data-stu-id="e0bd1-132">Panos</span></span>  <br/> |<span data-ttu-id="e0bd1-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0bd1-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e0bd1-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0bd1-134">optional</span></span>  <br/> ||<span data-ttu-id="e0bd1-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0bd1-136">Panose</span><span class="sxs-lookup"><span data-stu-id="e0bd1-136">Panose</span></span>  <br/> |<span data-ttu-id="e0bd1-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0bd1-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e0bd1-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0bd1-138">optional</span></span>  <br/> ||<span data-ttu-id="e0bd1-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0bd1-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="e0bd1-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="e0bd1-141">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0bd1-141">xsd:string</span></span>  <br/> |<span data-ttu-id="e0bd1-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0bd1-142">optional</span></span>  <br/> ||<span data-ttu-id="e0bd1-143">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-143">Values of the xsd:string type.</span></span>  <br/> |
   

