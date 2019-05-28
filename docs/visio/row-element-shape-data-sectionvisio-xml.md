---
title: Élément de ligne (section données de forme) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Spécifie une entrée de données de forme pour l’Association de données à une forme.
ms.openlocfilehash: 7857ad8a28e11d6ed3ba34145ffc0606f306120f
ms.sourcegitcommit: 9716521f7bcd531f93be9855ae7835be20cdd0e2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2019
ms.locfileid: "32283485"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="0e336-103">Élément de ligne (section données de forme) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0e336-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="0e336-104">Spécifie une entrée de données de forme pour l’Association de données à une forme.</span><span class="sxs-lookup"><span data-stu-id="0e336-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e336-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="0e336-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e336-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0e336-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0e336-107">Forme type_de_données</span><span class="sxs-lookup"><span data-stu-id="0e336-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0e336-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0e336-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0e336-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0e336-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0e336-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0e336-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0e336-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="0e336-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0e336-112">Master #. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="0e336-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e336-113">Définition</span><span class="sxs-lookup"><span data-stu-id="0e336-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0e336-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0e336-114">Elements and attributes</span></span>

<span data-ttu-id="0e336-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="0e336-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0e336-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0e336-116">Parent elements</span></span>

|<span data-ttu-id="0e336-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0e336-117">**Element**</span></span>|<span data-ttu-id="0e336-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="0e336-118">**Type**</span></span>|<span data-ttu-id="0e336-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e336-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0e336-120">Section</span><span class="sxs-lookup"><span data-stu-id="0e336-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e336-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0e336-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0e336-122">Spécifie une entrée de données de forme pour l’Association de données à une forme.</span><span class="sxs-lookup"><span data-stu-id="0e336-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0e336-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0e336-123">Child elements</span></span>

|<span data-ttu-id="0e336-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0e336-124">**Element**</span></span>|<span data-ttu-id="0e336-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="0e336-125">**Type**</span></span>|<span data-ttu-id="0e336-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e336-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0e336-127">Cell</span><span class="sxs-lookup"><span data-stu-id="0e336-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0e336-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0e336-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0e336-129">Spécifie une propriété des données de forme.</span><span class="sxs-lookup"><span data-stu-id="0e336-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0e336-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="0e336-130">Attributes</span></span>

|<span data-ttu-id="0e336-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0e336-131">**Attribute**</span></span>|<span data-ttu-id="0e336-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="0e336-132">**Type**</span></span>|<span data-ttu-id="0e336-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0e336-133">**Required**</span></span>|<span data-ttu-id="0e336-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e336-134">**Description**</span></span>|<span data-ttu-id="0e336-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0e336-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0e336-136">Suppr</span><span class="sxs-lookup"><span data-stu-id="0e336-136">Del</span></span>  <br/> |<span data-ttu-id="0e336-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="0e336-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0e336-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="0e336-138">optional</span></span>  <br/> |<span data-ttu-id="0e336-139">Indique si une ligne qui serait normalement héritée d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="0e336-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="0e336-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0e336-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0e336-141">IX</span><span class="sxs-lookup"><span data-stu-id="0e336-141">IX</span></span>  <br/> |<span data-ttu-id="0e336-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0e336-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e336-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="0e336-143">optional</span></span>  <br/> |<span data-ttu-id="0e336-144">Spécifie l’identificateur de base 1 de la ligne.</span><span class="sxs-lookup"><span data-stu-id="0e336-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="0e336-145">Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs.</span><span class="sxs-lookup"><span data-stu-id="0e336-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="0e336-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="0e336-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0e336-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0e336-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e336-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="0e336-148">LocalName</span></span>  <br/> |<span data-ttu-id="0e336-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e336-149">xsd:string</span></span>  <br/> |<span data-ttu-id="0e336-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="0e336-150">optional</span></span>  <br/> |<span data-ttu-id="0e336-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="0e336-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="0e336-152">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0e336-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e336-153">N</span><span class="sxs-lookup"><span data-stu-id="0e336-153">N</span></span>  <br/> |<span data-ttu-id="0e336-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e336-154">xsd:string</span></span>  <br/> |<span data-ttu-id="0e336-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="0e336-155">optional</span></span>  <br/> |<span data-ttu-id="0e336-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, HYPERLINK et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="0e336-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="0e336-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="0e336-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0e336-158">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0e336-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e336-159">T</span><span class="sxs-lookup"><span data-stu-id="0e336-159">T</span></span>  <br/> |<span data-ttu-id="0e336-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0e336-160">xsd:string</span></span>  <br/> |<span data-ttu-id="0e336-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="0e336-161">optional</span></span>  <br/> |<span data-ttu-id="0e336-162">Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="0e336-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="0e336-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="0e336-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="0e336-164">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0e336-164">Values of the xsd:string type.</span></span>  <br/> |
   

