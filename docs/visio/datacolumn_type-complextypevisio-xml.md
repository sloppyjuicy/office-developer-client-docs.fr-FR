---
title: ComplexType DataColumn_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344701"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="4fca6-102">ComplexType DataColumn_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4fca6-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4fca6-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="4fca6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fca6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4fca6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4fca6-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4fca6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4fca6-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="4fca6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4fca6-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="4fca6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4fca6-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="4fca6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4fca6-109">Définition</span><span class="sxs-lookup"><span data-stu-id="4fca6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4fca6-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4fca6-110">Elements and attributes</span></span>

<span data-ttu-id="4fca6-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="4fca6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4fca6-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4fca6-112">Child elements</span></span>

<span data-ttu-id="4fca6-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4fca6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fca6-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="4fca6-114">Attributes</span></span>

|<span data-ttu-id="4fca6-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4fca6-115">**Attribute**</span></span>|<span data-ttu-id="4fca6-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="4fca6-116">**Type**</span></span>|<span data-ttu-id="4fca6-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4fca6-117">**Required**</span></span>|<span data-ttu-id="4fca6-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="4fca6-118">**Description**</span></span>|<span data-ttu-id="4fca6-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4fca6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4fca6-120">Calendrier</span><span class="sxs-lookup"><span data-stu-id="4fca6-120">Calendar</span></span>  <br/> |<span data-ttu-id="4fca6-121">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4fca6-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4fca6-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-122">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-123">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4fca6-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="4fca6-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="4fca6-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="4fca6-125">xsd:string</span></span>  <br/> |<span data-ttu-id="4fca6-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4fca6-126">required</span></span>  <br/> ||<span data-ttu-id="4fca6-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4fca6-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-128">Devise</span><span class="sxs-lookup"><span data-stu-id="4fca6-128">Currency</span></span>  <br/> |<span data-ttu-id="4fca6-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4fca6-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4fca6-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-130">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-131">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4fca6-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-132">DataType</span><span class="sxs-lookup"><span data-stu-id="4fca6-132">DataType</span></span>  <br/> |<span data-ttu-id="4fca6-133">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4fca6-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4fca6-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-134">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-135">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4fca6-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-136">Degree</span><span class="sxs-lookup"><span data-stu-id="4fca6-136">Degree</span></span>  <br/> |<span data-ttu-id="4fca6-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4fca6-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4fca6-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-138">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-139">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4fca6-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="4fca6-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="4fca6-141">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4fca6-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4fca6-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-142">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-143">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4fca6-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="4fca6-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="4fca6-145">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4fca6-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4fca6-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-146">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4fca6-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-148">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="4fca6-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="4fca6-149">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="4fca6-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4fca6-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-150">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-151">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4fca6-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-152">Étiquette</span><span class="sxs-lookup"><span data-stu-id="4fca6-152">Label</span></span>  <br/> |<span data-ttu-id="4fca6-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="4fca6-153">xsd:string</span></span>  <br/> |<span data-ttu-id="4fca6-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4fca6-154">required</span></span>  <br/> ||<span data-ttu-id="4fca6-155">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4fca6-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-156">ID</span><span class="sxs-lookup"><span data-stu-id="4fca6-156">LangID</span></span>  <br/> |<span data-ttu-id="4fca6-157">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4fca6-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4fca6-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-158">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-159">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4fca6-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-160">Mappé</span><span class="sxs-lookup"><span data-stu-id="4fca6-160">Mapped</span></span>  <br/> |<span data-ttu-id="4fca6-161">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="4fca6-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4fca6-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-162">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-163">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4fca6-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-164">Nom</span><span class="sxs-lookup"><span data-stu-id="4fca6-164">Name</span></span>  <br/> |<span data-ttu-id="4fca6-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="4fca6-165">xsd:string</span></span>  <br/> |<span data-ttu-id="4fca6-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4fca6-166">required</span></span>  <br/> ||<span data-ttu-id="4fca6-167">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4fca6-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="4fca6-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="4fca6-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="4fca6-169">xsd:string</span></span>  <br/> |<span data-ttu-id="4fca6-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-170">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-171">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4fca6-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4fca6-172">Type_d'unité</span><span class="sxs-lookup"><span data-stu-id="4fca6-172">UnitType</span></span>  <br/> |<span data-ttu-id="4fca6-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="4fca6-173">xsd:string</span></span>  <br/> |<span data-ttu-id="4fca6-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="4fca6-174">optional</span></span>  <br/> ||<span data-ttu-id="4fca6-175">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4fca6-175">Values of the xsd:string type.</span></span>  <br/> |
   

