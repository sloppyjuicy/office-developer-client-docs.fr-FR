---
title: Row, élément (Shape Data Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Spécifie une entrée de données de forme pour associer des données à une forme.
ms.openlocfilehash: 4c5644aa2088dcaf3be81ea9aeaa549c911a31f6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538269"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="61152-103">Row, élément (Shape Data Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="61152-103">Row element (Shape Data Section) (Visio XML)</span></span>

<span data-ttu-id="61152-104">Spécifie une entrée de données de forme pour associer des données à une forme.</span><span class="sxs-lookup"><span data-stu-id="61152-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61152-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="61152-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61152-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="61152-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61152-107">Forme Data_Type</span><span class="sxs-lookup"><span data-stu-id="61152-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61152-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="61152-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61152-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="61152-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61152-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="61152-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61152-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="61152-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61152-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="61152-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61152-113">Définition</span><span class="sxs-lookup"><span data-stu-id="61152-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61152-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="61152-114">Elements and attributes</span></span>

<span data-ttu-id="61152-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="61152-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61152-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="61152-116">Parent elements</span></span>

|<span data-ttu-id="61152-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="61152-117">**Element**</span></span>|<span data-ttu-id="61152-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="61152-118">**Type**</span></span>|<span data-ttu-id="61152-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="61152-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61152-120">Section</span><span class="sxs-lookup"><span data-stu-id="61152-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61152-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="61152-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61152-122">Spécifie une entrée de données de forme pour associer des données à une forme.</span><span class="sxs-lookup"><span data-stu-id="61152-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61152-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="61152-123">Child elements</span></span>

|<span data-ttu-id="61152-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="61152-124">**Element**</span></span>|<span data-ttu-id="61152-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="61152-125">**Type**</span></span>|<span data-ttu-id="61152-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="61152-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61152-127">Cell</span><span class="sxs-lookup"><span data-stu-id="61152-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="61152-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="61152-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61152-129">Spécifie une propriété des données de forme.</span><span class="sxs-lookup"><span data-stu-id="61152-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="61152-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="61152-130">Attributes</span></span>

|<span data-ttu-id="61152-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="61152-131">**Attribute**</span></span>|<span data-ttu-id="61152-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="61152-132">**Type**</span></span>|<span data-ttu-id="61152-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="61152-133">**Required**</span></span>|<span data-ttu-id="61152-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="61152-134">**Description**</span></span>|<span data-ttu-id="61152-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="61152-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61152-136">Del</span><span class="sxs-lookup"><span data-stu-id="61152-136">Del</span></span>  <br/> |<span data-ttu-id="61152-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="61152-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61152-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="61152-138">optional</span></span>  <br/> |<span data-ttu-id="61152-139">Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="61152-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="61152-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="61152-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61152-141">IX</span><span class="sxs-lookup"><span data-stu-id="61152-141">IX</span></span>  <br/> |<span data-ttu-id="61152-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61152-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61152-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="61152-143">optional</span></span>  <br/> |<span data-ttu-id="61152-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="61152-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="61152-145">Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="61152-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="61152-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="61152-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="61152-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61152-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61152-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="61152-148">LocalName</span></span>  <br/> |<span data-ttu-id="61152-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61152-149">xsd:string</span></span>  <br/> |<span data-ttu-id="61152-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="61152-150">optional</span></span>  <br/> |<span data-ttu-id="61152-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="61152-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="61152-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="61152-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61152-153">N</span><span class="sxs-lookup"><span data-stu-id="61152-153">N</span></span>  <br/> |<span data-ttu-id="61152-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61152-154">xsd:string</span></span>  <br/> |<span data-ttu-id="61152-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="61152-155">optional</span></span>  <br/> |<span data-ttu-id="61152-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="61152-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="61152-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="61152-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="61152-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="61152-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61152-159">T</span><span class="sxs-lookup"><span data-stu-id="61152-159">T</span></span>  <br/> |<span data-ttu-id="61152-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61152-160">xsd:string</span></span>  <br/> |<span data-ttu-id="61152-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="61152-161">optional</span></span>  <br/> |<span data-ttu-id="61152-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="61152-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="61152-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="61152-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="61152-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="61152-164">Values of the xsd:string type.</span></span>  <br/> |
   

