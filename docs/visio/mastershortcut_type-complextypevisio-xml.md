---
title: MasterShortcut_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: ed8dd8ef985c814e41017526144bd7ec8cb63424
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538059"
---
# <a name="mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="2e96e-102">MasterShortcut_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2e96e-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2e96e-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="2e96e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e96e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2e96e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2e96e-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2e96e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2e96e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2e96e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2e96e-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="2e96e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2e96e-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="2e96e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2e96e-109">Définition</span><span class="sxs-lookup"><span data-stu-id="2e96e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2e96e-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2e96e-110">Elements and attributes</span></span>

<span data-ttu-id="2e96e-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="2e96e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2e96e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2e96e-112">Child elements</span></span>

|<span data-ttu-id="2e96e-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2e96e-113">**Element**</span></span>|<span data-ttu-id="2e96e-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="2e96e-114">**Type**</span></span>|<span data-ttu-id="2e96e-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e96e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2e96e-116">Icon</span><span class="sxs-lookup"><span data-stu-id="2e96e-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2e96e-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="2e96e-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2e96e-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="2e96e-118">Attributes</span></span>

|<span data-ttu-id="2e96e-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2e96e-119">**Attribute**</span></span>|<span data-ttu-id="2e96e-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="2e96e-120">**Type**</span></span>|<span data-ttu-id="2e96e-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2e96e-121">**Required**</span></span>|<span data-ttu-id="2e96e-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e96e-122">**Description**</span></span>|<span data-ttu-id="2e96e-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2e96e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2e96e-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="2e96e-124">AlignName</span></span>  <br/> |<span data-ttu-id="2e96e-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2e96e-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2e96e-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-126">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-127">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2e96e-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="2e96e-128">IconSize</span></span>  <br/> |<span data-ttu-id="2e96e-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2e96e-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2e96e-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-130">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2e96e-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-132">ID</span><span class="sxs-lookup"><span data-stu-id="2e96e-132">ID</span></span>  <br/> |<span data-ttu-id="2e96e-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2e96e-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2e96e-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2e96e-134">required</span></span>  <br/> ||<span data-ttu-id="2e96e-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2e96e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="2e96e-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="2e96e-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2e96e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2e96e-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-138">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-139">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2e96e-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="2e96e-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="2e96e-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2e96e-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2e96e-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-142">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-143">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2e96e-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="2e96e-144">MasterType</span></span>  <br/> |<span data-ttu-id="2e96e-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2e96e-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2e96e-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-146">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-147">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2e96e-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-148">Nom</span><span class="sxs-lookup"><span data-stu-id="2e96e-148">Name</span></span>  <br/> |<span data-ttu-id="2e96e-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2e96e-149">xsd:string</span></span>  <br/> |<span data-ttu-id="2e96e-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-150">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-151">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e96e-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-152">NameU</span><span class="sxs-lookup"><span data-stu-id="2e96e-152">NameU</span></span>  <br/> |<span data-ttu-id="2e96e-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2e96e-153">xsd:string</span></span>  <br/> |<span data-ttu-id="2e96e-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-154">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-155">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e96e-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="2e96e-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="2e96e-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2e96e-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2e96e-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-158">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-159">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2e96e-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-160">Invite</span><span class="sxs-lookup"><span data-stu-id="2e96e-160">Prompt</span></span>  <br/> |<span data-ttu-id="2e96e-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2e96e-161">xsd:string</span></span>  <br/> |<span data-ttu-id="2e96e-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-162">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-163">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e96e-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="2e96e-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="2e96e-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2e96e-165">xsd:string</span></span>  <br/> |<span data-ttu-id="2e96e-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-166">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-167">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e96e-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e96e-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="2e96e-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="2e96e-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2e96e-169">xsd:string</span></span>  <br/> |<span data-ttu-id="2e96e-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="2e96e-170">optional</span></span>  <br/> ||<span data-ttu-id="2e96e-171">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e96e-171">Values of the xsd:string type.</span></span>  <br/> |
   

