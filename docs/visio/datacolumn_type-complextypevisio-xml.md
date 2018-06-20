---
title: Type complexe DataColumn_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788402"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="1f504-102">Type complexe DataColumn_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1f504-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1f504-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1f504-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f504-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1f504-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1f504-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1f504-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1f504-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1f504-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1f504-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1f504-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1f504-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="1f504-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1f504-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1f504-109">Definition</span></span>

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1f504-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1f504-110">Elements and attributes</span></span>

<span data-ttu-id="1f504-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1f504-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1f504-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1f504-112">Child elements</span></span>

<span data-ttu-id="1f504-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1f504-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f504-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1f504-114">Attributes</span></span>

|<span data-ttu-id="1f504-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1f504-115">**Attribute**</span></span>|<span data-ttu-id="1f504-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="1f504-116">**Type**</span></span>|<span data-ttu-id="1f504-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1f504-117">**Required**</span></span>|<span data-ttu-id="1f504-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="1f504-118">**Description**</span></span>|<span data-ttu-id="1f504-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1f504-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1f504-120">Calendrier</span><span class="sxs-lookup"><span data-stu-id="1f504-120">Calendar</span></span>  <br/> |<span data-ttu-id="1f504-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1f504-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1f504-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-122">optional</span></span>  <br/> ||<span data-ttu-id="1f504-123">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1f504-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1f504-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="1f504-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="1f504-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1f504-125">xsd:string</span></span>  <br/> |<span data-ttu-id="1f504-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1f504-126">required</span></span>  <br/> ||<span data-ttu-id="1f504-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1f504-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1f504-128">Monnaie</span><span class="sxs-lookup"><span data-stu-id="1f504-128">Currency</span></span>  <br/> |<span data-ttu-id="1f504-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1f504-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1f504-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-130">optional</span></span>  <br/> ||<span data-ttu-id="1f504-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1f504-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1f504-132">Type de données</span><span class="sxs-lookup"><span data-stu-id="1f504-132">DataType</span></span>  <br/> |<span data-ttu-id="1f504-133">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1f504-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1f504-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-134">optional</span></span>  <br/> ||<span data-ttu-id="1f504-135">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1f504-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1f504-136">Degré</span><span class="sxs-lookup"><span data-stu-id="1f504-136">Degree</span></span>  <br/> |<span data-ttu-id="1f504-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f504-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f504-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-138">optional</span></span>  <br/> ||<span data-ttu-id="1f504-139">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f504-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f504-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="1f504-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="1f504-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f504-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f504-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-142">optional</span></span>  <br/> ||<span data-ttu-id="1f504-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f504-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f504-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="1f504-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="1f504-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f504-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f504-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-146">optional</span></span>  <br/> ||<span data-ttu-id="1f504-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f504-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f504-148">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="1f504-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="1f504-149">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="1f504-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1f504-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-150">optional</span></span>  <br/> ||<span data-ttu-id="1f504-151">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="1f504-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1f504-152">Étiquette</span><span class="sxs-lookup"><span data-stu-id="1f504-152">Label</span></span>  <br/> |<span data-ttu-id="1f504-153">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1f504-153">xsd:string</span></span>  <br/> |<span data-ttu-id="1f504-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1f504-154">required</span></span>  <br/> ||<span data-ttu-id="1f504-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1f504-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1f504-156">ID de langue</span><span class="sxs-lookup"><span data-stu-id="1f504-156">LangID</span></span>  <br/> |<span data-ttu-id="1f504-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f504-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f504-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-158">optional</span></span>  <br/> ||<span data-ttu-id="1f504-159">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f504-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f504-160">Mappées</span><span class="sxs-lookup"><span data-stu-id="1f504-160">Mapped</span></span>  <br/> |<span data-ttu-id="1f504-161">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="1f504-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1f504-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-162">optional</span></span>  <br/> ||<span data-ttu-id="1f504-163">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="1f504-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1f504-164">Nom</span><span class="sxs-lookup"><span data-stu-id="1f504-164">Name</span></span>  <br/> |<span data-ttu-id="1f504-165">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1f504-165">xsd:string</span></span>  <br/> |<span data-ttu-id="1f504-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1f504-166">required</span></span>  <br/> ||<span data-ttu-id="1f504-167">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1f504-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1f504-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="1f504-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="1f504-169">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1f504-169">xsd:string</span></span>  <br/> |<span data-ttu-id="1f504-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-170">optional</span></span>  <br/> ||<span data-ttu-id="1f504-171">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1f504-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1f504-172">Type_d</span><span class="sxs-lookup"><span data-stu-id="1f504-172">UnitType</span></span>  <br/> |<span data-ttu-id="1f504-173">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1f504-173">xsd:string</span></span>  <br/> |<span data-ttu-id="1f504-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f504-174">optional</span></span>  <br/> ||<span data-ttu-id="1f504-175">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1f504-175">Values of the xsd:string type.</span></span>  <br/> |
   

