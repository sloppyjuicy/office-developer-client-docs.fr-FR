---
title: ComplexType MasterShortcut_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341691"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="35582-102">ComplexType MasterShortcut_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="35582-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="35582-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="35582-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35582-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="35582-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="35582-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="35582-105">**Schema file**</span></span> <br/> |<span data-ttu-id="35582-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="35582-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="35582-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="35582-107">**Extension base**</span></span> <br/> |<span data-ttu-id="35582-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="35582-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="35582-109">Définition</span><span class="sxs-lookup"><span data-stu-id="35582-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="35582-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="35582-110">Elements and attributes</span></span>

<span data-ttu-id="35582-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="35582-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="35582-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="35582-112">Child elements</span></span>

|<span data-ttu-id="35582-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="35582-113">**Element**</span></span>|<span data-ttu-id="35582-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="35582-114">**Type**</span></span>|<span data-ttu-id="35582-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="35582-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="35582-116">Icon</span><span class="sxs-lookup"><span data-stu-id="35582-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35582-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="35582-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="35582-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="35582-118">Attributes</span></span>

|<span data-ttu-id="35582-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="35582-119">**Attribute**</span></span>|<span data-ttu-id="35582-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="35582-120">**Type**</span></span>|<span data-ttu-id="35582-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="35582-121">**Required**</span></span>|<span data-ttu-id="35582-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="35582-122">**Description**</span></span>|<span data-ttu-id="35582-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="35582-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="35582-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="35582-124">AlignName</span></span>  <br/> |<span data-ttu-id="35582-125">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="35582-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="35582-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-126">optional</span></span>  <br/> ||<span data-ttu-id="35582-127">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="35582-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="35582-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="35582-128">IconSize</span></span>  <br/> |<span data-ttu-id="35582-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="35582-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="35582-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-130">optional</span></span>  <br/> ||<span data-ttu-id="35582-131">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="35582-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="35582-132">ID</span><span class="sxs-lookup"><span data-stu-id="35582-132">ID</span></span>  <br/> |<span data-ttu-id="35582-133">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="35582-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="35582-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="35582-134">required</span></span>  <br/> ||<span data-ttu-id="35582-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="35582-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="35582-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="35582-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="35582-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="35582-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="35582-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-138">optional</span></span>  <br/> ||<span data-ttu-id="35582-139">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="35582-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="35582-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="35582-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="35582-141">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="35582-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="35582-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-142">optional</span></span>  <br/> ||<span data-ttu-id="35582-143">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="35582-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="35582-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="35582-144">MasterType</span></span>  <br/> |<span data-ttu-id="35582-145">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="35582-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="35582-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-146">optional</span></span>  <br/> ||<span data-ttu-id="35582-147">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="35582-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="35582-148">Nom</span><span class="sxs-lookup"><span data-stu-id="35582-148">Name</span></span>  <br/> |<span data-ttu-id="35582-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="35582-149">xsd:string</span></span>  <br/> |<span data-ttu-id="35582-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-150">optional</span></span>  <br/> ||<span data-ttu-id="35582-151">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="35582-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35582-152">NameU</span><span class="sxs-lookup"><span data-stu-id="35582-152">NameU</span></span>  <br/> |<span data-ttu-id="35582-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="35582-153">xsd:string</span></span>  <br/> |<span data-ttu-id="35582-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-154">optional</span></span>  <br/> ||<span data-ttu-id="35582-155">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="35582-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35582-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="35582-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="35582-157">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="35582-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="35582-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-158">optional</span></span>  <br/> ||<span data-ttu-id="35582-159">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="35582-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="35582-160">Invite</span><span class="sxs-lookup"><span data-stu-id="35582-160">Prompt</span></span>  <br/> |<span data-ttu-id="35582-161">xsd: String</span><span class="sxs-lookup"><span data-stu-id="35582-161">xsd:string</span></span>  <br/> |<span data-ttu-id="35582-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-162">optional</span></span>  <br/> ||<span data-ttu-id="35582-163">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="35582-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35582-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="35582-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="35582-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="35582-165">xsd:string</span></span>  <br/> |<span data-ttu-id="35582-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-166">optional</span></span>  <br/> ||<span data-ttu-id="35582-167">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="35582-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35582-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="35582-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="35582-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="35582-169">xsd:string</span></span>  <br/> |<span data-ttu-id="35582-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="35582-170">optional</span></span>  <br/> ||<span data-ttu-id="35582-171">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="35582-171">Values of the xsd:string type.</span></span>  <br/> |
   

