---
title: Type complexe Page_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: b3a4916f3de20d9350b6673a6000d56f3030b66e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789196"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="a2295-102">Type complexe Page_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a2295-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a2295-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a2295-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2295-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a2295-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a2295-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a2295-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a2295-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a2295-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a2295-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a2295-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a2295-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="a2295-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2295-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a2295-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a2295-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a2295-110">Elements and attributes</span></span>

<span data-ttu-id="a2295-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a2295-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a2295-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a2295-112">Child elements</span></span>

|<span data-ttu-id="a2295-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a2295-113">**Element**</span></span>|<span data-ttu-id="a2295-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a2295-114">**Type**</span></span>|<span data-ttu-id="a2295-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2295-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a2295-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="a2295-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2295-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a2295-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a2295-118">Rel</span><span class="sxs-lookup"><span data-stu-id="a2295-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2295-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="a2295-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a2295-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="a2295-120">Attributes</span></span>

|<span data-ttu-id="a2295-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a2295-121">**Attribute**</span></span>|<span data-ttu-id="a2295-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="a2295-122">**Type**</span></span>|<span data-ttu-id="a2295-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a2295-123">**Required**</span></span>|<span data-ttu-id="a2295-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2295-124">**Description**</span></span>|<span data-ttu-id="a2295-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a2295-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2295-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="a2295-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="a2295-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2295-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2295-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-128">optional</span></span>  <br/> ||<span data-ttu-id="a2295-129">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2295-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2295-130">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="a2295-130">Background</span></span>  <br/> |<span data-ttu-id="a2295-131">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="a2295-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a2295-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-132">optional</span></span>  <br/> ||<span data-ttu-id="a2295-133">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="a2295-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a2295-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="a2295-134">BackPage</span></span>  <br/> |<span data-ttu-id="a2295-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2295-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2295-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-136">optional</span></span>  <br/> ||<span data-ttu-id="a2295-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2295-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2295-138">ID</span><span class="sxs-lookup"><span data-stu-id="a2295-138">ID</span></span>  <br/> |<span data-ttu-id="a2295-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2295-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2295-140">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2295-140">required</span></span>  <br/> ||<span data-ttu-id="a2295-141">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2295-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2295-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a2295-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="a2295-143">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="a2295-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a2295-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-144">optional</span></span>  <br/> ||<span data-ttu-id="a2295-145">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="a2295-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a2295-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a2295-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a2295-147">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="a2295-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a2295-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-148">optional</span></span>  <br/> ||<span data-ttu-id="a2295-149">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="a2295-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a2295-150">Nom</span><span class="sxs-lookup"><span data-stu-id="a2295-150">Name</span></span>  <br/> |<span data-ttu-id="a2295-151">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a2295-151">xsd:string</span></span>  <br/> |<span data-ttu-id="a2295-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-152">optional</span></span>  <br/> ||<span data-ttu-id="a2295-153">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a2295-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a2295-154">NameU</span><span class="sxs-lookup"><span data-stu-id="a2295-154">NameU</span></span>  <br/> |<span data-ttu-id="a2295-155">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a2295-155">xsd:string</span></span>  <br/> |<span data-ttu-id="a2295-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-156">optional</span></span>  <br/> ||<span data-ttu-id="a2295-157">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a2295-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a2295-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="a2295-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="a2295-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2295-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2295-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-160">optional</span></span>  <br/> ||<span data-ttu-id="a2295-161">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2295-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2295-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="a2295-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="a2295-163">XSD : double</span><span class="sxs-lookup"><span data-stu-id="a2295-163">xsd:double</span></span>  <br/> |<span data-ttu-id="a2295-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-164">optional</span></span>  <br/> ||<span data-ttu-id="a2295-165">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="a2295-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a2295-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="a2295-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="a2295-167">XSD : double</span><span class="sxs-lookup"><span data-stu-id="a2295-167">xsd:double</span></span>  <br/> |<span data-ttu-id="a2295-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-168">optional</span></span>  <br/> ||<span data-ttu-id="a2295-169">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="a2295-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a2295-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="a2295-170">ViewScale</span></span>  <br/> |<span data-ttu-id="a2295-171">XSD : double</span><span class="sxs-lookup"><span data-stu-id="a2295-171">xsd:double</span></span>  <br/> |<span data-ttu-id="a2295-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="a2295-172">optional</span></span>  <br/> ||<span data-ttu-id="a2295-173">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="a2295-173">Values of the xsd:double type.</span></span>  <br/> |
   

