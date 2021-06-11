---
title: Élément de cellule (ligne LineTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite.
ms.openlocfilehash: 4b1628549e659712a1c2e79ae0fbf53d594e18f9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539508"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="ddc53-103">Élément de cellule (ligne LineTo) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ddc53-103">Cell element (LineTo Row) (Visio XML)</span></span>

<span data-ttu-id="ddc53-104">Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="ddc53-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddc53-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="ddc53-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddc53-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ddc53-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ddc53-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ddc53-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ddc53-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ddc53-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ddc53-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ddc53-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ddc53-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ddc53-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ddc53-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="ddc53-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ddc53-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="ddc53-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ddc53-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ddc53-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ddc53-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ddc53-114">Elements and attributes</span></span>

<span data-ttu-id="ddc53-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="ddc53-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ddc53-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ddc53-116">Parent elements</span></span>

|<span data-ttu-id="ddc53-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ddc53-117">**Element**</span></span>|<span data-ttu-id="ddc53-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ddc53-118">**Type**</span></span>|<span data-ttu-id="ddc53-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ddc53-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddc53-120">Élément Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="ddc53-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ddc53-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="ddc53-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ddc53-122">Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="ddc53-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ddc53-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ddc53-123">Child elements</span></span>

|<span data-ttu-id="ddc53-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ddc53-124">**Element**</span></span>|<span data-ttu-id="ddc53-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ddc53-125">**Type**</span></span>|<span data-ttu-id="ddc53-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="ddc53-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddc53-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="ddc53-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ddc53-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="ddc53-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ddc53-129">Spécifie une référence à une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="ddc53-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ddc53-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="ddc53-130">Attributes</span></span>

|<span data-ttu-id="ddc53-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ddc53-131">**Attribute**</span></span>|<span data-ttu-id="ddc53-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="ddc53-132">**Type**</span></span>|<span data-ttu-id="ddc53-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ddc53-133">**Required**</span></span>|<span data-ttu-id="ddc53-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="ddc53-134">**Description**</span></span>|<span data-ttu-id="ddc53-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ddc53-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ddc53-136">E</span><span class="sxs-lookup"><span data-stu-id="ddc53-136">E</span></span>  <br/> |<span data-ttu-id="ddc53-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ddc53-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ddc53-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="ddc53-138">optional</span></span>  <br/> |<span data-ttu-id="ddc53-139">Indique que la formule est évaluée à une erreur.</span><span class="sxs-lookup"><span data-stu-id="ddc53-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="ddc53-140">La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide.</span><span class="sxs-lookup"><span data-stu-id="ddc53-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="ddc53-141">Chaîne de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ddc53-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="ddc53-142">F</span><span class="sxs-lookup"><span data-stu-id="ddc53-142">F</span></span>  <br/> |<span data-ttu-id="ddc53-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ddc53-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ddc53-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="ddc53-144">optional</span></span>  <br/> | <span data-ttu-id="ddc53-145">Représente la formule de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ddc53-145">Represents the element's formula.</span></span> <span data-ttu-id="ddc53-146">Cet attribut peut contenir l’une des chaînes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddc53-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="ddc53-147">'(une formule)' si la formule existe localement</span><span class="sxs-lookup"><span data-stu-id="ddc53-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="ddc53-148">`No Formula` si la formule est supprimée ou bloquée localement</span><span class="sxs-lookup"><span data-stu-id="ddc53-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="ddc53-149">`Inh` si la formule est héritée.</span><span class="sxs-lookup"><span data-stu-id="ddc53-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="ddc53-150">Formule.</span><span class="sxs-lookup"><span data-stu-id="ddc53-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="ddc53-151">N</span><span class="sxs-lookup"><span data-stu-id="ddc53-151">N</span></span>  <br/> |<span data-ttu-id="ddc53-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ddc53-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ddc53-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ddc53-153">required</span></span>  <br/> |<span data-ttu-id="ddc53-154">Représente le nom de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ddc53-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="ddc53-155">Nom de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ddc53-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="ddc53-156">Voir la section Remarques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ddc53-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="ddc53-157">U</span><span class="sxs-lookup"><span data-stu-id="ddc53-157">U</span></span>  <br/> |<span data-ttu-id="ddc53-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ddc53-158">xsd:string</span></span>  <br/> |<span data-ttu-id="ddc53-159">facultatif</span><span class="sxs-lookup"><span data-stu-id="ddc53-159">optional</span></span>  <br/> |<span data-ttu-id="ddc53-160">Représente une unité de mesure La valeur par défaut est DL.</span><span class="sxs-lookup"><span data-stu-id="ddc53-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="ddc53-161">Unités de la cellule.</span><span class="sxs-lookup"><span data-stu-id="ddc53-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="ddc53-162">V</span><span class="sxs-lookup"><span data-stu-id="ddc53-162">V</span></span>  <br/> |<span data-ttu-id="ddc53-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ddc53-163">xsd:string</span></span>  <br/> |<span data-ttu-id="ddc53-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="ddc53-164">optional</span></span>  <br/> |<span data-ttu-id="ddc53-165">Représente la valeur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="ddc53-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="ddc53-166">Valeur de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ddc53-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddc53-167">Remarques</span><span class="sxs-lookup"><span data-stu-id="ddc53-167">Remarks</span></span>

<span data-ttu-id="ddc53-168">**L’attribut N** de cet **élément Cell** doit faire partie d’un ensemble limité de valeurs qui correspondent aux cellules ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ddc53-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="ddc53-169">Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell.**</span><span class="sxs-lookup"><span data-stu-id="ddc53-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="ddc53-170">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ddc53-170">**Value**</span></span>|<span data-ttu-id="ddc53-171">**Description**</span><span class="sxs-lookup"><span data-stu-id="ddc53-171">**Description**</span></span>|<span data-ttu-id="ddc53-172">**Plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="ddc53-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ddc53-173">X</span><span class="sxs-lookup"><span data-stu-id="ddc53-173">X</span></span>  <br/> |<span data-ttu-id="ddc53-174">Coordonnée x du sommet de fin d'un segment de droite.</span><span class="sxs-lookup"><span data-stu-id="ddc53-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="ddc53-175">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="ddc53-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="ddc53-176">v</span><span class="sxs-lookup"><span data-stu-id="ddc53-176">Y</span></span>  <br/> |<span data-ttu-id="ddc53-177">Coordonnée y du sommet de fin d'un segment de droite.</span><span class="sxs-lookup"><span data-stu-id="ddc53-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="ddc53-178">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="ddc53-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

