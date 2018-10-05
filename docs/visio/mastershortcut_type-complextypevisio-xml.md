---
title: Type complexe MasterShortcut_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396483"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="fe797-102">Type complexe MasterShortcut_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="fe797-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fe797-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="fe797-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe797-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="fe797-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fe797-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fe797-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fe797-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fe797-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fe797-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="fe797-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fe797-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="fe797-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fe797-109">Définition</span><span class="sxs-lookup"><span data-stu-id="fe797-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fe797-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fe797-110">Elements and attributes</span></span>

<span data-ttu-id="fe797-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="fe797-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fe797-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fe797-112">Child elements</span></span>

|<span data-ttu-id="fe797-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fe797-113">**Element**</span></span>|<span data-ttu-id="fe797-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="fe797-114">**Type**</span></span>|<span data-ttu-id="fe797-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe797-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fe797-116">Icône</span><span class="sxs-lookup"><span data-stu-id="fe797-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fe797-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="fe797-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fe797-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="fe797-118">Attributes</span></span>

|<span data-ttu-id="fe797-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fe797-119">**Attribute**</span></span>|<span data-ttu-id="fe797-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="fe797-120">**Type**</span></span>|<span data-ttu-id="fe797-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fe797-121">**Required**</span></span>|<span data-ttu-id="fe797-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe797-122">**Description**</span></span>|<span data-ttu-id="fe797-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fe797-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fe797-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="fe797-124">AlignName</span></span>  <br/> |<span data-ttu-id="fe797-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fe797-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fe797-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-126">optional</span></span>  <br/> ||<span data-ttu-id="fe797-127">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fe797-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fe797-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="fe797-128">IconSize</span></span>  <br/> |<span data-ttu-id="fe797-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fe797-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fe797-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-130">optional</span></span>  <br/> ||<span data-ttu-id="fe797-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fe797-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fe797-132">ID</span><span class="sxs-lookup"><span data-stu-id="fe797-132">ID</span></span>  <br/> |<span data-ttu-id="fe797-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fe797-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fe797-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fe797-134">required</span></span>  <br/> ||<span data-ttu-id="fe797-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fe797-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fe797-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="fe797-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="fe797-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="fe797-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fe797-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-138">optional</span></span>  <br/> ||<span data-ttu-id="fe797-139">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="fe797-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fe797-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="fe797-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="fe797-141">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="fe797-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fe797-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-142">optional</span></span>  <br/> ||<span data-ttu-id="fe797-143">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="fe797-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fe797-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="fe797-144">MasterType</span></span>  <br/> |<span data-ttu-id="fe797-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fe797-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fe797-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-146">optional</span></span>  <br/> ||<span data-ttu-id="fe797-147">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fe797-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fe797-148">Nom</span><span class="sxs-lookup"><span data-stu-id="fe797-148">Name</span></span>  <br/> |<span data-ttu-id="fe797-149">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fe797-149">xsd:string</span></span>  <br/> |<span data-ttu-id="fe797-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-150">optional</span></span>  <br/> ||<span data-ttu-id="fe797-151">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fe797-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe797-152">NameU</span><span class="sxs-lookup"><span data-stu-id="fe797-152">NameU</span></span>  <br/> |<span data-ttu-id="fe797-153">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fe797-153">xsd:string</span></span>  <br/> |<span data-ttu-id="fe797-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-154">optional</span></span>  <br/> ||<span data-ttu-id="fe797-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fe797-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe797-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="fe797-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="fe797-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fe797-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fe797-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-158">optional</span></span>  <br/> ||<span data-ttu-id="fe797-159">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fe797-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fe797-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="fe797-160">Prompt</span></span>  <br/> |<span data-ttu-id="fe797-161">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fe797-161">xsd:string</span></span>  <br/> |<span data-ttu-id="fe797-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-162">optional</span></span>  <br/> ||<span data-ttu-id="fe797-163">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fe797-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe797-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="fe797-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="fe797-165">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fe797-165">xsd:string</span></span>  <br/> |<span data-ttu-id="fe797-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-166">optional</span></span>  <br/> ||<span data-ttu-id="fe797-167">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fe797-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe797-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="fe797-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="fe797-169">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fe797-169">xsd:string</span></span>  <br/> |<span data-ttu-id="fe797-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="fe797-170">optional</span></span>  <br/> ||<span data-ttu-id="fe797-171">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fe797-171">Values of the xsd:string type.</span></span>  <br/> |
   

