---
title: Élément de ligne (section contrôles) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Contient les cellules d'une poignée de contrôle particulière définie pour une forme.
ms.openlocfilehash: aa690bf70078a711dffca3f01b6e7acc05507bdd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358421"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="55b11-103">Élément de ligne (section contrôles) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="55b11-103">Row element (Controls Section) ('Visio XML')</span></span>

<span data-ttu-id="55b11-104">Contient les cellules d'une poignée de contrôle particulière définie pour une forme.</span><span class="sxs-lookup"><span data-stu-id="55b11-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55b11-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="55b11-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55b11-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="55b11-106">**Element type**</span></span> <br/> |[<span data-ttu-id="55b11-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="55b11-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="55b11-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="55b11-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="55b11-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="55b11-109">**Schema file**</span></span> <br/> |<span data-ttu-id="55b11-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="55b11-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="55b11-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="55b11-111">**Document parts**</span></span> <br/> |<span data-ttu-id="55b11-112">Master #. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="55b11-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="55b11-113">Définition</span><span class="sxs-lookup"><span data-stu-id="55b11-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="55b11-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="55b11-114">Elements and attributes</span></span>

<span data-ttu-id="55b11-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="55b11-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="55b11-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="55b11-116">Parent elements</span></span>

|<span data-ttu-id="55b11-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="55b11-117">**Element**</span></span>|<span data-ttu-id="55b11-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="55b11-118">**Type**</span></span>|<span data-ttu-id="55b11-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="55b11-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55b11-120">Section</span><span class="sxs-lookup"><span data-stu-id="55b11-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55b11-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="55b11-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="55b11-122">Contient les cellules d'une poignée de contrôle particulière définie pour une forme.</span><span class="sxs-lookup"><span data-stu-id="55b11-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55b11-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="55b11-123">Child elements</span></span>

|<span data-ttu-id="55b11-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="55b11-124">**Element**</span></span>|<span data-ttu-id="55b11-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="55b11-125">**Type**</span></span>|<span data-ttu-id="55b11-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="55b11-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55b11-127">Cell</span><span class="sxs-lookup"><span data-stu-id="55b11-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="55b11-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="55b11-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="55b11-129">Contient une propriété pour une poignée de contrôle spécifique définie pour une forme.</span><span class="sxs-lookup"><span data-stu-id="55b11-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="55b11-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="55b11-130">Attributes</span></span>

|<span data-ttu-id="55b11-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="55b11-131">**Attribute**</span></span>|<span data-ttu-id="55b11-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="55b11-132">**Type**</span></span>|<span data-ttu-id="55b11-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="55b11-133">**Required**</span></span>|<span data-ttu-id="55b11-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="55b11-134">**Description**</span></span>|<span data-ttu-id="55b11-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="55b11-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="55b11-136">Suppr</span><span class="sxs-lookup"><span data-stu-id="55b11-136">Del</span></span>  <br/> |<span data-ttu-id="55b11-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="55b11-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="55b11-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="55b11-138">optional</span></span>  <br/> |<span data-ttu-id="55b11-139">Indique si une ligne qui serait normalement héritée d'une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="55b11-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="55b11-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="55b11-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="55b11-141">IX</span><span class="sxs-lookup"><span data-stu-id="55b11-141">IX</span></span>  <br/> |<span data-ttu-id="55b11-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="55b11-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="55b11-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="55b11-143">optional</span></span>  <br/> |<span data-ttu-id="55b11-144">Spécifie l'identificateur de base 1 de la ligne.</span><span class="sxs-lookup"><span data-stu-id="55b11-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="55b11-145">Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L'attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs.</span><span class="sxs-lookup"><span data-stu-id="55b11-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="55b11-146">Une ligne ne peut avoir qu'un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="55b11-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="55b11-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="55b11-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="55b11-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="55b11-148">LocalName</span></span>  <br/> |<span data-ttu-id="55b11-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="55b11-149">xsd:string</span></span>  <br/> |<span data-ttu-id="55b11-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="55b11-150">optional</span></span>  <br/> |<span data-ttu-id="55b11-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="55b11-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="55b11-152">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="55b11-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="55b11-153">N</span><span class="sxs-lookup"><span data-stu-id="55b11-153">N</span></span>  <br/> |<span data-ttu-id="55b11-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="55b11-154">xsd:string</span></span>  <br/> |<span data-ttu-id="55b11-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="55b11-155">optional</span></span>  <br/> |<span data-ttu-id="55b11-156">Spécifie le nom unique indépendant de la langue de la ligne. L'attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, hyperLink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="55b11-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="55b11-157">Une ligne ne peut avoir qu'un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="55b11-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="55b11-158">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="55b11-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="55b11-159">T</span><span class="sxs-lookup"><span data-stu-id="55b11-159">T</span></span>  <br/> |<span data-ttu-id="55b11-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="55b11-160">xsd:string</span></span>  <br/> |<span data-ttu-id="55b11-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="55b11-161">optional</span></span>  <br/> |<span data-ttu-id="55b11-162">Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="55b11-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="55b11-163">L'attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="55b11-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="55b11-164">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="55b11-164">Values of the xsd:string type.</span></span>  <br/> |
   

