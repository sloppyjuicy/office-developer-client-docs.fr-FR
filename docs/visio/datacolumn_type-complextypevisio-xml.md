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
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="eeff5-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="eeff5-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="eeff5-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="eeff5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eeff5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eeff5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eeff5-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="eeff5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eeff5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="eeff5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eeff5-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="eeff5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eeff5-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="eeff5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eeff5-109">Définition</span><span class="sxs-lookup"><span data-stu-id="eeff5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="eeff5-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="eeff5-110">Elements and attributes</span></span>

<span data-ttu-id="eeff5-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="eeff5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eeff5-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eeff5-112">Child elements</span></span>

<span data-ttu-id="eeff5-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eeff5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eeff5-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="eeff5-114">Attributes</span></span>

|<span data-ttu-id="eeff5-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="eeff5-115">**Attribute**</span></span>|<span data-ttu-id="eeff5-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="eeff5-116">**Type**</span></span>|<span data-ttu-id="eeff5-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="eeff5-117">**Required**</span></span>|<span data-ttu-id="eeff5-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="eeff5-118">**Description**</span></span>|<span data-ttu-id="eeff5-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="eeff5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eeff5-120">Calendrier</span><span class="sxs-lookup"><span data-stu-id="eeff5-120">Calendar</span></span>  <br/> |<span data-ttu-id="eeff5-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="eeff5-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="eeff5-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-122">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-123">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="eeff5-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="eeff5-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="eeff5-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="eeff5-125">xsd:string</span></span>  <br/> |<span data-ttu-id="eeff5-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="eeff5-126">required</span></span>  <br/> ||<span data-ttu-id="eeff5-127">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="eeff5-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-128">Monétaire</span><span class="sxs-lookup"><span data-stu-id="eeff5-128">Currency</span></span>  <br/> |<span data-ttu-id="eeff5-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="eeff5-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="eeff5-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-130">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="eeff5-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-132">DataType</span><span class="sxs-lookup"><span data-stu-id="eeff5-132">DataType</span></span>  <br/> |<span data-ttu-id="eeff5-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="eeff5-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="eeff5-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-134">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-135">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="eeff5-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-136">Degree</span><span class="sxs-lookup"><span data-stu-id="eeff5-136">Degree</span></span>  <br/> |<span data-ttu-id="eeff5-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eeff5-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eeff5-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-138">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-139">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eeff5-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="eeff5-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="eeff5-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eeff5-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eeff5-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-142">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eeff5-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="eeff5-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="eeff5-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eeff5-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eeff5-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-146">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eeff5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="eeff5-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="eeff5-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="eeff5-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="eeff5-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-150">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-151">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="eeff5-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-152">Étiquette</span><span class="sxs-lookup"><span data-stu-id="eeff5-152">Label</span></span>  <br/> |<span data-ttu-id="eeff5-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="eeff5-153">xsd:string</span></span>  <br/> |<span data-ttu-id="eeff5-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="eeff5-154">required</span></span>  <br/> ||<span data-ttu-id="eeff5-155">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="eeff5-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-156">LangID</span><span class="sxs-lookup"><span data-stu-id="eeff5-156">LangID</span></span>  <br/> |<span data-ttu-id="eeff5-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eeff5-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eeff5-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-158">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-159">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eeff5-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-160">Mappée</span><span class="sxs-lookup"><span data-stu-id="eeff5-160">Mapped</span></span>  <br/> |<span data-ttu-id="eeff5-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="eeff5-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="eeff5-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-162">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-163">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="eeff5-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-164">Nom</span><span class="sxs-lookup"><span data-stu-id="eeff5-164">Name</span></span>  <br/> |<span data-ttu-id="eeff5-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="eeff5-165">xsd:string</span></span>  <br/> |<span data-ttu-id="eeff5-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="eeff5-166">required</span></span>  <br/> ||<span data-ttu-id="eeff5-167">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="eeff5-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="eeff5-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="eeff5-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="eeff5-169">xsd:string</span></span>  <br/> |<span data-ttu-id="eeff5-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-170">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-171">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="eeff5-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="eeff5-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="eeff5-172">UnitType</span></span>  <br/> |<span data-ttu-id="eeff5-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="eeff5-173">xsd:string</span></span>  <br/> |<span data-ttu-id="eeff5-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="eeff5-174">optional</span></span>  <br/> ||<span data-ttu-id="eeff5-175">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="eeff5-175">Values of the xsd:string type.</span></span>  <br/> |
   

