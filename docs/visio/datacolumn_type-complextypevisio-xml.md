---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541210"
---
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="fe0f2-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fe0f2-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fe0f2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="fe0f2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe0f2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fe0f2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fe0f2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fe0f2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fe0f2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fe0f2-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="fe0f2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fe0f2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="fe0f2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fe0f2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fe0f2-110">Elements and attributes</span></span>

<span data-ttu-id="fe0f2-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fe0f2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fe0f2-112">Child elements</span></span>

<span data-ttu-id="fe0f2-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe0f2-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="fe0f2-114">Attributes</span></span>

|<span data-ttu-id="fe0f2-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-115">**Attribute**</span></span>|<span data-ttu-id="fe0f2-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-116">**Type**</span></span>|<span data-ttu-id="fe0f2-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-117">**Required**</span></span>|<span data-ttu-id="fe0f2-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-118">**Description**</span></span>|<span data-ttu-id="fe0f2-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fe0f2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fe0f2-120">Calendrier</span><span class="sxs-lookup"><span data-stu-id="fe0f2-120">Calendar</span></span>  <br/> |<span data-ttu-id="fe0f2-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fe0f2-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fe0f2-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-122">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-123">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="fe0f2-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="fe0f2-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fe0f2-125">xsd:string</span></span>  <br/> |<span data-ttu-id="fe0f2-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fe0f2-126">required</span></span>  <br/> ||<span data-ttu-id="fe0f2-127">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-128">Devise</span><span class="sxs-lookup"><span data-stu-id="fe0f2-128">Currency</span></span>  <br/> |<span data-ttu-id="fe0f2-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fe0f2-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fe0f2-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-130">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-132">DataType</span><span class="sxs-lookup"><span data-stu-id="fe0f2-132">DataType</span></span>  <br/> |<span data-ttu-id="fe0f2-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fe0f2-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fe0f2-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-134">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-135">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-136">Degree</span><span class="sxs-lookup"><span data-stu-id="fe0f2-136">Degree</span></span>  <br/> |<span data-ttu-id="fe0f2-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fe0f2-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fe0f2-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-138">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-139">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="fe0f2-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="fe0f2-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fe0f2-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fe0f2-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-142">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="fe0f2-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="fe0f2-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fe0f2-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fe0f2-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-146">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-148">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="fe0f2-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="fe0f2-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="fe0f2-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fe0f2-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-150">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-151">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-152">Étiquette</span><span class="sxs-lookup"><span data-stu-id="fe0f2-152">Label</span></span>  <br/> |<span data-ttu-id="fe0f2-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fe0f2-153">xsd:string</span></span>  <br/> |<span data-ttu-id="fe0f2-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fe0f2-154">required</span></span>  <br/> ||<span data-ttu-id="fe0f2-155">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-156">LangID</span><span class="sxs-lookup"><span data-stu-id="fe0f2-156">LangID</span></span>  <br/> |<span data-ttu-id="fe0f2-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fe0f2-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fe0f2-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-158">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-159">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-160">Mappée</span><span class="sxs-lookup"><span data-stu-id="fe0f2-160">Mapped</span></span>  <br/> |<span data-ttu-id="fe0f2-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="fe0f2-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fe0f2-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-162">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-163">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-164">Nom</span><span class="sxs-lookup"><span data-stu-id="fe0f2-164">Name</span></span>  <br/> |<span data-ttu-id="fe0f2-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fe0f2-165">xsd:string</span></span>  <br/> |<span data-ttu-id="fe0f2-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fe0f2-166">required</span></span>  <br/> ||<span data-ttu-id="fe0f2-167">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="fe0f2-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="fe0f2-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fe0f2-169">xsd:string</span></span>  <br/> |<span data-ttu-id="fe0f2-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-170">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-171">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe0f2-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="fe0f2-172">UnitType</span></span>  <br/> |<span data-ttu-id="fe0f2-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fe0f2-173">xsd:string</span></span>  <br/> |<span data-ttu-id="fe0f2-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe0f2-174">optional</span></span>  <br/> ||<span data-ttu-id="fe0f2-175">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-175">Values of the xsd:string type.</span></span>  <br/> |
   

