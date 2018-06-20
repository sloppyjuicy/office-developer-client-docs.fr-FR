---
title: Type complexe MasterShortcut_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: df1e10ff11470cd87fc16efbaba6ad968df6d1b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789082"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="c25e7-102">Type complexe MasterShortcut_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c25e7-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c25e7-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c25e7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c25e7-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c25e7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c25e7-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c25e7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c25e7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c25e7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c25e7-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c25e7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c25e7-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="c25e7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c25e7-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c25e7-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
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
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c25e7-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c25e7-110">Elements and attributes</span></span>

<span data-ttu-id="c25e7-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c25e7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c25e7-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c25e7-112">Child elements</span></span>

|<span data-ttu-id="c25e7-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c25e7-113">**Element**</span></span>|<span data-ttu-id="c25e7-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c25e7-114">**Type**</span></span>|<span data-ttu-id="c25e7-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c25e7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c25e7-116">Icône</span><span class="sxs-lookup"><span data-stu-id="c25e7-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c25e7-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="c25e7-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c25e7-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c25e7-118">Attributes</span></span>

|<span data-ttu-id="c25e7-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c25e7-119">**Attribute**</span></span>|<span data-ttu-id="c25e7-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="c25e7-120">**Type**</span></span>|<span data-ttu-id="c25e7-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c25e7-121">**Required**</span></span>|<span data-ttu-id="c25e7-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="c25e7-122">**Description**</span></span>|<span data-ttu-id="c25e7-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c25e7-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c25e7-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="c25e7-124">AlignName</span></span>  <br/> |<span data-ttu-id="c25e7-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c25e7-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c25e7-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-126">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-127">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c25e7-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="c25e7-128">IconSize</span></span>  <br/> |<span data-ttu-id="c25e7-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c25e7-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c25e7-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-130">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c25e7-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-132">ID</span><span class="sxs-lookup"><span data-stu-id="c25e7-132">ID</span></span>  <br/> |<span data-ttu-id="c25e7-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c25e7-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c25e7-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c25e7-134">required</span></span>  <br/> ||<span data-ttu-id="c25e7-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c25e7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="c25e7-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="c25e7-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="c25e7-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c25e7-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-138">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-139">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="c25e7-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c25e7-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c25e7-141">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="c25e7-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c25e7-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-142">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-143">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="c25e7-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="c25e7-144">MasterType</span></span>  <br/> |<span data-ttu-id="c25e7-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c25e7-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c25e7-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-146">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-147">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c25e7-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-148">Nom</span><span class="sxs-lookup"><span data-stu-id="c25e7-148">Name</span></span>  <br/> |<span data-ttu-id="c25e7-149">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c25e7-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c25e7-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-150">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-151">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c25e7-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-152">NameU</span><span class="sxs-lookup"><span data-stu-id="c25e7-152">NameU</span></span>  <br/> |<span data-ttu-id="c25e7-153">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c25e7-153">xsd:string</span></span>  <br/> |<span data-ttu-id="c25e7-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-154">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c25e7-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="c25e7-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="c25e7-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c25e7-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c25e7-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-158">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-159">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c25e7-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="c25e7-160">Prompt</span></span>  <br/> |<span data-ttu-id="c25e7-161">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c25e7-161">xsd:string</span></span>  <br/> |<span data-ttu-id="c25e7-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-162">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-163">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c25e7-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="c25e7-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="c25e7-165">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c25e7-165">xsd:string</span></span>  <br/> |<span data-ttu-id="c25e7-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-166">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-167">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c25e7-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c25e7-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="c25e7-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="c25e7-169">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c25e7-169">xsd:string</span></span>  <br/> |<span data-ttu-id="c25e7-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="c25e7-170">optional</span></span>  <br/> ||<span data-ttu-id="c25e7-171">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c25e7-171">Values of the xsd:string type.</span></span>  <br/> |
   

