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
# <a name="mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="9cbe2-102">MasterShortcut_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9cbe2-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9cbe2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9cbe2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9cbe2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9cbe2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9cbe2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9cbe2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9cbe2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9cbe2-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="9cbe2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9cbe2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9cbe2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9cbe2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9cbe2-110">Elements and attributes</span></span>

<span data-ttu-id="9cbe2-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9cbe2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9cbe2-112">Child elements</span></span>

|<span data-ttu-id="9cbe2-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-113">**Element**</span></span>|<span data-ttu-id="9cbe2-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-114">**Type**</span></span>|<span data-ttu-id="9cbe2-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9cbe2-116">Icon</span><span class="sxs-lookup"><span data-stu-id="9cbe2-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9cbe2-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="9cbe2-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9cbe2-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9cbe2-118">Attributes</span></span>

|<span data-ttu-id="9cbe2-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-119">**Attribute**</span></span>|<span data-ttu-id="9cbe2-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-120">**Type**</span></span>|<span data-ttu-id="9cbe2-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-121">**Required**</span></span>|<span data-ttu-id="9cbe2-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-122">**Description**</span></span>|<span data-ttu-id="9cbe2-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9cbe2-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9cbe2-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="9cbe2-124">AlignName</span></span>  <br/> |<span data-ttu-id="9cbe2-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9cbe2-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9cbe2-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-126">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-127">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="9cbe2-128">IconSize</span></span>  <br/> |<span data-ttu-id="9cbe2-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9cbe2-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9cbe2-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-130">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-132">ID</span><span class="sxs-lookup"><span data-stu-id="9cbe2-132">ID</span></span>  <br/> |<span data-ttu-id="9cbe2-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9cbe2-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9cbe2-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9cbe2-134">required</span></span>  <br/> ||<span data-ttu-id="9cbe2-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="9cbe2-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="9cbe2-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9cbe2-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9cbe2-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-138">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-139">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="9cbe2-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="9cbe2-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9cbe2-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9cbe2-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-142">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-143">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="9cbe2-144">MasterType</span></span>  <br/> |<span data-ttu-id="9cbe2-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9cbe2-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9cbe2-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-146">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-147">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-148">Nom</span><span class="sxs-lookup"><span data-stu-id="9cbe2-148">Name</span></span>  <br/> |<span data-ttu-id="9cbe2-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9cbe2-149">xsd:string</span></span>  <br/> |<span data-ttu-id="9cbe2-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-150">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-151">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-152">NameU</span><span class="sxs-lookup"><span data-stu-id="9cbe2-152">NameU</span></span>  <br/> |<span data-ttu-id="9cbe2-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9cbe2-153">xsd:string</span></span>  <br/> |<span data-ttu-id="9cbe2-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-154">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-155">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="9cbe2-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="9cbe2-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9cbe2-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9cbe2-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-158">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-159">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-160">Invite</span><span class="sxs-lookup"><span data-stu-id="9cbe2-160">Prompt</span></span>  <br/> |<span data-ttu-id="9cbe2-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9cbe2-161">xsd:string</span></span>  <br/> |<span data-ttu-id="9cbe2-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-162">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-163">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="9cbe2-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="9cbe2-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9cbe2-165">xsd:string</span></span>  <br/> |<span data-ttu-id="9cbe2-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-166">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-167">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9cbe2-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="9cbe2-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="9cbe2-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9cbe2-169">xsd:string</span></span>  <br/> |<span data-ttu-id="9cbe2-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="9cbe2-170">optional</span></span>  <br/> ||<span data-ttu-id="9cbe2-171">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-171">Values of the xsd:string type.</span></span>  <br/> |
   

