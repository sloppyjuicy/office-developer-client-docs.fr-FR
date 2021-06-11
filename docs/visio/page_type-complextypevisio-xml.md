---
title: Page_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 3a0153b724539136fe142c2489badcf9895af765
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537982"
---
# <a name="page_type-complextype-visio-xml"></a><span data-ttu-id="9c4c3-102">Page_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9c4c3-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9c4c3-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9c4c3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c4c3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9c4c3-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9c4c3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9c4c3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9c4c3-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9c4c3-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="9c4c3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c4c3-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9c4c3-109">Definition</span></span>

```XML
          <xs:complexType name="Page_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c4c3-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9c4c3-110">Elements and attributes</span></span>

<span data-ttu-id="9c4c3-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9c4c3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9c4c3-112">Child elements</span></span>

|<span data-ttu-id="9c4c3-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-113">**Element**</span></span>|<span data-ttu-id="9c4c3-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-114">**Type**</span></span>|<span data-ttu-id="9c4c3-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c4c3-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="9c4c3-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c4c3-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9c4c3-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c4c3-118">Rel</span><span class="sxs-lookup"><span data-stu-id="9c4c3-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c4c3-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="9c4c3-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9c4c3-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="9c4c3-120">Attributes</span></span>

|<span data-ttu-id="9c4c3-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-121">**Attribute**</span></span>|<span data-ttu-id="9c4c3-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-122">**Type**</span></span>|<span data-ttu-id="9c4c3-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-123">**Required**</span></span>|<span data-ttu-id="9c4c3-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-124">**Description**</span></span>|<span data-ttu-id="9c4c3-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9c4c3-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9c4c3-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="9c4c3-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="9c4c3-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c4c3-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c4c3-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-128">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-129">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-130">Contexte</span><span class="sxs-lookup"><span data-stu-id="9c4c3-130">Background</span></span>  <br/> |<span data-ttu-id="9c4c3-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9c4c3-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9c4c3-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-132">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-133">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="9c4c3-134">BackPage</span></span>  <br/> |<span data-ttu-id="9c4c3-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c4c3-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c4c3-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-136">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-138">ID</span><span class="sxs-lookup"><span data-stu-id="9c4c3-138">ID</span></span>  <br/> |<span data-ttu-id="9c4c3-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c4c3-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c4c3-140">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9c4c3-140">required</span></span>  <br/> ||<span data-ttu-id="9c4c3-141">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="9c4c3-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="9c4c3-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9c4c3-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9c4c3-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-144">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-145">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="9c4c3-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="9c4c3-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9c4c3-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9c4c3-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-148">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-149">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-150">Nom</span><span class="sxs-lookup"><span data-stu-id="9c4c3-150">Name</span></span>  <br/> |<span data-ttu-id="9c4c3-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9c4c3-151">xsd:string</span></span>  <br/> |<span data-ttu-id="9c4c3-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-152">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-153">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-154">NameU</span><span class="sxs-lookup"><span data-stu-id="9c4c3-154">NameU</span></span>  <br/> |<span data-ttu-id="9c4c3-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9c4c3-155">xsd:string</span></span>  <br/> |<span data-ttu-id="9c4c3-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-156">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-157">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="9c4c3-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="9c4c3-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c4c3-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c4c3-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-160">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-161">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="9c4c3-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="9c4c3-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="9c4c3-163">xsd:double</span></span>  <br/> |<span data-ttu-id="9c4c3-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-164">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-165">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="9c4c3-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="9c4c3-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="9c4c3-167">xsd:double</span></span>  <br/> |<span data-ttu-id="9c4c3-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-168">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-169">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="9c4c3-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="9c4c3-170">ViewScale</span></span>  <br/> |<span data-ttu-id="9c4c3-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="9c4c3-171">xsd:double</span></span>  <br/> |<span data-ttu-id="9c4c3-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="9c4c3-172">optional</span></span>  <br/> ||<span data-ttu-id="9c4c3-173">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="9c4c3-173">Values of the xsd:double type.</span></span>  <br/> |
   

