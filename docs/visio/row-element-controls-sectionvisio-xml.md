---
title: Row, élément (section Controls) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Contient les cellules d’un handle de contrôle particulier défini pour une forme.
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541742"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="c0c13-103">Row, élément (section Controls) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c0c13-103">Row element (Controls Section) (Visio XML)</span></span>

<span data-ttu-id="c0c13-104">Contient les cellules d’un handle de contrôle particulier défini pour une forme.</span><span class="sxs-lookup"><span data-stu-id="c0c13-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0c13-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="c0c13-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0c13-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c0c13-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c0c13-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="c0c13-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c0c13-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c0c13-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c0c13-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c0c13-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c0c13-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c0c13-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c0c13-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="c0c13-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c0c13-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="c0c13-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c0c13-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c0c13-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c0c13-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c0c13-114">Elements and attributes</span></span>

<span data-ttu-id="c0c13-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c0c13-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c0c13-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c0c13-116">Parent elements</span></span>

|<span data-ttu-id="c0c13-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c0c13-117">**Element**</span></span>|<span data-ttu-id="c0c13-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c0c13-118">**Type**</span></span>|<span data-ttu-id="c0c13-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0c13-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c0c13-120">Section</span><span class="sxs-lookup"><span data-stu-id="c0c13-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c0c13-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c0c13-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c0c13-122">Contient les cellules d’un handle de contrôle particulier défini pour une forme.</span><span class="sxs-lookup"><span data-stu-id="c0c13-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c0c13-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c0c13-123">Child elements</span></span>

|<span data-ttu-id="c0c13-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c0c13-124">**Element**</span></span>|<span data-ttu-id="c0c13-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c0c13-125">**Type**</span></span>|<span data-ttu-id="c0c13-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0c13-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c0c13-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c0c13-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="c0c13-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c0c13-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c0c13-129">Contient une propriété pour un handle de contrôle particulier défini pour une forme.</span><span class="sxs-lookup"><span data-stu-id="c0c13-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c0c13-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="c0c13-130">Attributes</span></span>

|<span data-ttu-id="c0c13-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c0c13-131">**Attribute**</span></span>|<span data-ttu-id="c0c13-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="c0c13-132">**Type**</span></span>|<span data-ttu-id="c0c13-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c0c13-133">**Required**</span></span>|<span data-ttu-id="c0c13-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0c13-134">**Description**</span></span>|<span data-ttu-id="c0c13-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c0c13-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c0c13-136">Del</span><span class="sxs-lookup"><span data-stu-id="c0c13-136">Del</span></span>  <br/> |<span data-ttu-id="c0c13-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c0c13-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c0c13-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="c0c13-138">optional</span></span>  <br/> |<span data-ttu-id="c0c13-139">Spécifie si une ligne qui sinon serait héritée d’une forme de forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="c0c13-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c0c13-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c0c13-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c0c13-141">IX</span><span class="sxs-lookup"><span data-stu-id="c0c13-141">IX</span></span>  <br/> |<span data-ttu-id="c0c13-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c0c13-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c0c13-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="c0c13-143">optional</span></span>  <br/> |<span data-ttu-id="c0c13-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="c0c13-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c0c13-145">Il doit être unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="c0c13-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c0c13-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="c0c13-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c0c13-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c0c13-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c0c13-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c0c13-148">LocalName</span></span>  <br/> |<span data-ttu-id="c0c13-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c0c13-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c0c13-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="c0c13-150">optional</span></span>  <br/> |<span data-ttu-id="c0c13-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="c0c13-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c0c13-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c0c13-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c0c13-153">N</span><span class="sxs-lookup"><span data-stu-id="c0c13-153">N</span></span>  <br/> |<span data-ttu-id="c0c13-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c0c13-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c0c13-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="c0c13-155">optional</span></span>  <br/> |<span data-ttu-id="c0c13-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="c0c13-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c0c13-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="c0c13-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c0c13-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c0c13-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c0c13-159">T</span><span class="sxs-lookup"><span data-stu-id="c0c13-159">T</span></span>  <br/> |<span data-ttu-id="c0c13-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c0c13-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c0c13-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="c0c13-161">optional</span></span>  <br/> |<span data-ttu-id="c0c13-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="c0c13-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c0c13-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="c0c13-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c0c13-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c0c13-164">Values of the xsd:string type.</span></span>  <br/> |
   

