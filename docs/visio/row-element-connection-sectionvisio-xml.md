---
title: Élément Row (connection section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Contient les coordonnées x ou y, la direction horizontale et verticale, et le type d’un point de connexion unique sur une forme.
ms.openlocfilehash: eb32030e89d3ac77adfdc64e2d20a5fb954dbb53
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541763"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="0eb01-103">Élément Row (connection section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0eb01-103">Row element (Connection Section) (Visio XML)</span></span>

<span data-ttu-id="0eb01-104">Contient les coordonnées x ou y, la direction horizontale et verticale, et le type d’un point de connexion unique sur une forme.</span><span class="sxs-lookup"><span data-stu-id="0eb01-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0eb01-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="0eb01-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0eb01-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0eb01-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0eb01-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="0eb01-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0eb01-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0eb01-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0eb01-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0eb01-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0eb01-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0eb01-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0eb01-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="0eb01-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0eb01-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="0eb01-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0eb01-113">Définition</span><span class="sxs-lookup"><span data-stu-id="0eb01-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0eb01-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0eb01-114">Elements and attributes</span></span>

<span data-ttu-id="0eb01-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="0eb01-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0eb01-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0eb01-116">Parent elements</span></span>

|<span data-ttu-id="0eb01-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0eb01-117">**Element**</span></span>|<span data-ttu-id="0eb01-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="0eb01-118">**Type**</span></span>|<span data-ttu-id="0eb01-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="0eb01-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0eb01-120">Section</span><span class="sxs-lookup"><span data-stu-id="0eb01-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0eb01-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0eb01-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0eb01-122">Contient les coordonnées x ou y, la direction horizontale et verticale, et le type d’un point de connexion unique sur une forme.</span><span class="sxs-lookup"><span data-stu-id="0eb01-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0eb01-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0eb01-123">Child elements</span></span>

|<span data-ttu-id="0eb01-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0eb01-124">**Element**</span></span>|<span data-ttu-id="0eb01-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="0eb01-125">**Type**</span></span>|<span data-ttu-id="0eb01-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="0eb01-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0eb01-127">Cell</span><span class="sxs-lookup"><span data-stu-id="0eb01-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="0eb01-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0eb01-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0eb01-129">Spécifie une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="0eb01-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0eb01-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="0eb01-130">Attributes</span></span>

|<span data-ttu-id="0eb01-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0eb01-131">**Attribute**</span></span>|<span data-ttu-id="0eb01-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="0eb01-132">**Type**</span></span>|<span data-ttu-id="0eb01-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0eb01-133">**Required**</span></span>|<span data-ttu-id="0eb01-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="0eb01-134">**Description**</span></span>|<span data-ttu-id="0eb01-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0eb01-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0eb01-136">Del</span><span class="sxs-lookup"><span data-stu-id="0eb01-136">Del</span></span>  <br/> |<span data-ttu-id="0eb01-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0eb01-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0eb01-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="0eb01-138">optional</span></span>  <br/> |<span data-ttu-id="0eb01-139">Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="0eb01-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="0eb01-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0eb01-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0eb01-141">IX</span><span class="sxs-lookup"><span data-stu-id="0eb01-141">IX</span></span>  <br/> |<span data-ttu-id="0eb01-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0eb01-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0eb01-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="0eb01-143">optional</span></span>  <br/> |<span data-ttu-id="0eb01-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="0eb01-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="0eb01-145">Il doit être unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="0eb01-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="0eb01-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="0eb01-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0eb01-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0eb01-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0eb01-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="0eb01-148">LocalName</span></span>  <br/> |<span data-ttu-id="0eb01-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0eb01-149">xsd:string</span></span>  <br/> |<span data-ttu-id="0eb01-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="0eb01-150">optional</span></span>  <br/> |<span data-ttu-id="0eb01-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="0eb01-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="0eb01-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0eb01-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0eb01-153">N</span><span class="sxs-lookup"><span data-stu-id="0eb01-153">N</span></span>  <br/> |<span data-ttu-id="0eb01-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0eb01-154">xsd:string</span></span>  <br/> |<span data-ttu-id="0eb01-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="0eb01-155">optional</span></span>  <br/> |<span data-ttu-id="0eb01-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="0eb01-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="0eb01-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="0eb01-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0eb01-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0eb01-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0eb01-159">T</span><span class="sxs-lookup"><span data-stu-id="0eb01-159">T</span></span>  <br/> |<span data-ttu-id="0eb01-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0eb01-160">xsd:string</span></span>  <br/> |<span data-ttu-id="0eb01-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="0eb01-161">optional</span></span>  <br/> |<span data-ttu-id="0eb01-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="0eb01-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="0eb01-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="0eb01-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="0eb01-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0eb01-164">Values of the xsd:string type.</span></span>  <br/> |
   

