---
title: ComplexType Page_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334397"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="10bf6-102">ComplexType Page_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="10bf6-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="10bf6-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="10bf6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10bf6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="10bf6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="10bf6-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="10bf6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="10bf6-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="10bf6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="10bf6-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="10bf6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="10bf6-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="10bf6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10bf6-109">Définition</span><span class="sxs-lookup"><span data-stu-id="10bf6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="10bf6-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="10bf6-110">Elements and attributes</span></span>

<span data-ttu-id="10bf6-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="10bf6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="10bf6-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="10bf6-112">Child elements</span></span>

|<span data-ttu-id="10bf6-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="10bf6-113">**Element**</span></span>|<span data-ttu-id="10bf6-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="10bf6-114">**Type**</span></span>|<span data-ttu-id="10bf6-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="10bf6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10bf6-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="10bf6-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10bf6-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="10bf6-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="10bf6-118">Ver</span><span class="sxs-lookup"><span data-stu-id="10bf6-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10bf6-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="10bf6-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="10bf6-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="10bf6-120">Attributes</span></span>

|<span data-ttu-id="10bf6-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="10bf6-121">**Attribute**</span></span>|<span data-ttu-id="10bf6-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="10bf6-122">**Type**</span></span>|<span data-ttu-id="10bf6-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="10bf6-123">**Required**</span></span>|<span data-ttu-id="10bf6-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="10bf6-124">**Description**</span></span>|<span data-ttu-id="10bf6-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="10bf6-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10bf6-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="10bf6-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="10bf6-127">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10bf6-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10bf6-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-128">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-129">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="10bf6-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-130">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="10bf6-130">Background</span></span>  <br/> |<span data-ttu-id="10bf6-131">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="10bf6-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="10bf6-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-132">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-133">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="10bf6-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="10bf6-134">BackPage</span></span>  <br/> |<span data-ttu-id="10bf6-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10bf6-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10bf6-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-136">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="10bf6-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-138">ID</span><span class="sxs-lookup"><span data-stu-id="10bf6-138">ID</span></span>  <br/> |<span data-ttu-id="10bf6-139">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10bf6-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10bf6-140">obligatoire</span><span class="sxs-lookup"><span data-stu-id="10bf6-140">required</span></span>  <br/> ||<span data-ttu-id="10bf6-141">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="10bf6-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="10bf6-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="10bf6-143">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="10bf6-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="10bf6-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-144">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-145">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="10bf6-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="10bf6-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="10bf6-147">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="10bf6-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="10bf6-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-148">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-149">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="10bf6-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-150">Nom</span><span class="sxs-lookup"><span data-stu-id="10bf6-150">Name</span></span>  <br/> |<span data-ttu-id="10bf6-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="10bf6-151">xsd:string</span></span>  <br/> |<span data-ttu-id="10bf6-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-152">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-153">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="10bf6-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-154">NameU</span><span class="sxs-lookup"><span data-stu-id="10bf6-154">NameU</span></span>  <br/> |<span data-ttu-id="10bf6-155">xsd: String</span><span class="sxs-lookup"><span data-stu-id="10bf6-155">xsd:string</span></span>  <br/> |<span data-ttu-id="10bf6-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-156">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-157">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="10bf6-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="10bf6-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="10bf6-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10bf6-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10bf6-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-160">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-161">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="10bf6-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="10bf6-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="10bf6-163">xsd: double</span><span class="sxs-lookup"><span data-stu-id="10bf6-163">xsd:double</span></span>  <br/> |<span data-ttu-id="10bf6-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-164">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-165">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="10bf6-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="10bf6-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="10bf6-167">xsd: double</span><span class="sxs-lookup"><span data-stu-id="10bf6-167">xsd:double</span></span>  <br/> |<span data-ttu-id="10bf6-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-168">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-169">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="10bf6-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="10bf6-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="10bf6-170">ViewScale</span></span>  <br/> |<span data-ttu-id="10bf6-171">xsd: double</span><span class="sxs-lookup"><span data-stu-id="10bf6-171">xsd:double</span></span>  <br/> |<span data-ttu-id="10bf6-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="10bf6-172">optional</span></span>  <br/> ||<span data-ttu-id="10bf6-173">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="10bf6-173">Values of the xsd:double type.</span></span>  <br/> |
   

