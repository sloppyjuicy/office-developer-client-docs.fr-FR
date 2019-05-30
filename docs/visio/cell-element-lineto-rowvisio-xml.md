---
title: Élément de cellule (ligne LineTo) (XML Visio)
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
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="48581-103">Élément de cellule (ligne LineTo) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="48581-103">Cell element (LineTo Row) (Visio XML)</span></span>

<span data-ttu-id="48581-104">Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="48581-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48581-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="48581-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48581-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="48581-106">**Element type**</span></span> <br/> |[<span data-ttu-id="48581-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="48581-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="48581-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="48581-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="48581-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="48581-109">**Schema file**</span></span> <br/> |<span data-ttu-id="48581-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="48581-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="48581-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="48581-111">**Document parts**</span></span> <br/> |<span data-ttu-id="48581-112">Master #. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="48581-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48581-113">Définition</span><span class="sxs-lookup"><span data-stu-id="48581-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="48581-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="48581-114">Elements and attributes</span></span>

<span data-ttu-id="48581-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="48581-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="48581-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="48581-116">Parent elements</span></span>

|<span data-ttu-id="48581-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="48581-117">**Element**</span></span>|<span data-ttu-id="48581-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="48581-118">**Type**</span></span>|<span data-ttu-id="48581-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="48581-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48581-120">Élément de ligne (géométrie)</span><span class="sxs-lookup"><span data-stu-id="48581-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="48581-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="48581-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="48581-122">Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="48581-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="48581-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="48581-123">Child elements</span></span>

|<span data-ttu-id="48581-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="48581-124">**Element**</span></span>|<span data-ttu-id="48581-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="48581-125">**Type**</span></span>|<span data-ttu-id="48581-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="48581-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48581-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="48581-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48581-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="48581-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="48581-129">Cette énumération spécifie une référence à une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="48581-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="48581-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="48581-130">Attributes</span></span>

|<span data-ttu-id="48581-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="48581-131">**Attribute**</span></span>|<span data-ttu-id="48581-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="48581-132">**Type**</span></span>|<span data-ttu-id="48581-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="48581-133">**Required**</span></span>|<span data-ttu-id="48581-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="48581-134">**Description**</span></span>|<span data-ttu-id="48581-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="48581-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48581-136">E</span><span class="sxs-lookup"><span data-stu-id="48581-136">E</span></span>  <br/> |<span data-ttu-id="48581-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="48581-137">xsd:string</span></span>  <br/> |<span data-ttu-id="48581-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="48581-138">optional</span></span>  <br/> |<span data-ttu-id="48581-139">Indique que la formule génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="48581-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="48581-140">La valeur **E** est la valeur actuelle (chaîne de message d’erreur); la valeur de l’attribut **V** est la dernière valeur valide.</span><span class="sxs-lookup"><span data-stu-id="48581-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="48581-141">Chaîne de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="48581-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="48581-142">F</span><span class="sxs-lookup"><span data-stu-id="48581-142">F</span></span>  <br/> |<span data-ttu-id="48581-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="48581-143">xsd:string</span></span>  <br/> |<span data-ttu-id="48581-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="48581-144">optional</span></span>  <br/> | <span data-ttu-id="48581-145">Représente la formule de l’élément.</span><span class="sxs-lookup"><span data-stu-id="48581-145">Represents the element's formula.</span></span> <span data-ttu-id="48581-146">Cet attribut peut contenir l’une des chaînes suivantes:</span><span class="sxs-lookup"><span data-stu-id="48581-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="48581-147">' (une formule) 'si la formule existe localement</span><span class="sxs-lookup"><span data-stu-id="48581-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="48581-148">`No Formula`Si la formule est supprimée ou bloquée localement</span><span class="sxs-lookup"><span data-stu-id="48581-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="48581-149">`Inh`Si la formule est héritée.</span><span class="sxs-lookup"><span data-stu-id="48581-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="48581-150">Une formule.</span><span class="sxs-lookup"><span data-stu-id="48581-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="48581-151">N</span><span class="sxs-lookup"><span data-stu-id="48581-151">N</span></span>  <br/> |<span data-ttu-id="48581-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="48581-152">xsd:string</span></span>  <br/> |<span data-ttu-id="48581-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="48581-153">required</span></span>  <br/> |<span data-ttu-id="48581-154">Représente le nom de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="48581-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="48581-155">Nom de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="48581-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="48581-156">Consultez la section Remarques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="48581-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="48581-157">U</span><span class="sxs-lookup"><span data-stu-id="48581-157">U</span></span>  <br/> |<span data-ttu-id="48581-158">xsd: String</span><span class="sxs-lookup"><span data-stu-id="48581-158">xsd:string</span></span>  <br/> |<span data-ttu-id="48581-159">facultatif</span><span class="sxs-lookup"><span data-stu-id="48581-159">optional</span></span>  <br/> |<span data-ttu-id="48581-160">Représente une unité de mesure la valeur par défaut est DL.</span><span class="sxs-lookup"><span data-stu-id="48581-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="48581-161">Unités de la cellule.</span><span class="sxs-lookup"><span data-stu-id="48581-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="48581-162">V</span><span class="sxs-lookup"><span data-stu-id="48581-162">V</span></span>  <br/> |<span data-ttu-id="48581-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="48581-163">xsd:string</span></span>  <br/> |<span data-ttu-id="48581-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="48581-164">optional</span></span>  <br/> |<span data-ttu-id="48581-165">Représente la valeur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="48581-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="48581-166">Valeur de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="48581-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48581-167">Remarques</span><span class="sxs-lookup"><span data-stu-id="48581-167">Remarks</span></span>

<span data-ttu-id="48581-168">L’attribut **N** de cet élément de **cellule** doit correspondre à l’un des jeux de valeurs limités qui correspondent aux cellules de la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="48581-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="48581-169">Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de **cellule** .</span><span class="sxs-lookup"><span data-stu-id="48581-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="48581-170">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="48581-170">**Value**</span></span>|<span data-ttu-id="48581-171">**Description**</span><span class="sxs-lookup"><span data-stu-id="48581-171">**Description**</span></span>|<span data-ttu-id="48581-172">**Plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="48581-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48581-173">X</span><span class="sxs-lookup"><span data-stu-id="48581-173">X</span></span>  <br/> |<span data-ttu-id="48581-174">Coordonnée x du sommet de fin d'un segment de droite.</span><span class="sxs-lookup"><span data-stu-id="48581-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="48581-175">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="48581-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="48581-176">v</span><span class="sxs-lookup"><span data-stu-id="48581-176">Y</span></span>  <br/> |<span data-ttu-id="48581-177">Coordonnée y du sommet de fin d'un segment de droite.</span><span class="sxs-lookup"><span data-stu-id="48581-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="48581-178">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="48581-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

