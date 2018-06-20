---
title: Type complexe FaceName_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 554a8144fd38c34d59aa2fd0ae25d171c20cd8ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788589"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="4f358-102">Type complexe FaceName_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="4f358-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4f358-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="4f358-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f358-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4f358-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4f358-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4f358-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4f358-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4f358-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4f358-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="4f358-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4f358-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="4f358-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f358-109">Définition</span><span class="sxs-lookup"><span data-stu-id="4f358-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4f358-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4f358-110">Elements and attributes</span></span>

<span data-ttu-id="4f358-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4f358-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4f358-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4f358-112">Child elements</span></span>

<span data-ttu-id="4f358-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4f358-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f358-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="4f358-114">Attributes</span></span>

|<span data-ttu-id="4f358-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4f358-115">**Attribute**</span></span>|<span data-ttu-id="4f358-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="4f358-116">**Type**</span></span>|<span data-ttu-id="4f358-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4f358-117">**Required**</span></span>|<span data-ttu-id="4f358-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="4f358-118">**Description**</span></span>|<span data-ttu-id="4f358-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4f358-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f358-120">Jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="4f358-120">CharSets</span></span>  <br/> |<span data-ttu-id="4f358-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4f358-121">xsd:string</span></span>  <br/> |<span data-ttu-id="4f358-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="4f358-122">optional</span></span>  <br/> ||<span data-ttu-id="4f358-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4f358-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f358-124">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="4f358-124">Flags</span></span>  <br/> |<span data-ttu-id="4f358-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4f358-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4f358-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="4f358-126">optional</span></span>  <br/> ||<span data-ttu-id="4f358-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4f358-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4f358-128">NameU</span><span class="sxs-lookup"><span data-stu-id="4f358-128">NameU</span></span>  <br/> |<span data-ttu-id="4f358-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4f358-129">xsd:string</span></span>  <br/> |<span data-ttu-id="4f358-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4f358-130">required</span></span>  <br/> ||<span data-ttu-id="4f358-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4f358-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f358-132">Panos</span><span class="sxs-lookup"><span data-stu-id="4f358-132">Panos</span></span>  <br/> |<span data-ttu-id="4f358-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4f358-133">xsd:string</span></span>  <br/> |<span data-ttu-id="4f358-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="4f358-134">optional</span></span>  <br/> ||<span data-ttu-id="4f358-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4f358-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f358-136">Panose</span><span class="sxs-lookup"><span data-stu-id="4f358-136">Panose</span></span>  <br/> |<span data-ttu-id="4f358-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4f358-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4f358-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="4f358-138">optional</span></span>  <br/> ||<span data-ttu-id="4f358-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4f358-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f358-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="4f358-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="4f358-141">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4f358-141">xsd:string</span></span>  <br/> |<span data-ttu-id="4f358-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="4f358-142">optional</span></span>  <br/> ||<span data-ttu-id="4f358-143">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4f358-143">Values of the xsd:string type.</span></span>  <br/> |
   

