---
title: Élément de cellule (ligne LineTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Contient les coordonnées x ou y du sommet de fin d'un segment de ligne droite.
ms.openlocfilehash: 5b7d8128cbef57c4dd9fb69d5b82e1c1c2ccef68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318200"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="a8c34-103">Élément de cellule (ligne LineTo) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a8c34-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="a8c34-104">Contient les coordonnées x ou y du sommet de fin d'un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="a8c34-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8c34-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a8c34-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8c34-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a8c34-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a8c34-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a8c34-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a8c34-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a8c34-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a8c34-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a8c34-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a8c34-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a8c34-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a8c34-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="a8c34-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a8c34-112">Master #. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="a8c34-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8c34-113">Définition</span><span class="sxs-lookup"><span data-stu-id="a8c34-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8c34-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a8c34-114">Elements and attributes</span></span>

<span data-ttu-id="a8c34-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a8c34-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a8c34-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a8c34-116">Parent elements</span></span>

|<span data-ttu-id="a8c34-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a8c34-117">**Element**</span></span>|<span data-ttu-id="a8c34-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8c34-118">**Type**</span></span>|<span data-ttu-id="a8c34-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8c34-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8c34-120">Élément de ligne (géométrie)</span><span class="sxs-lookup"><span data-stu-id="a8c34-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a8c34-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="a8c34-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8c34-122">Contient les coordonnées x ou y du sommet de fin d'un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="a8c34-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a8c34-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8c34-123">Child elements</span></span>

|<span data-ttu-id="a8c34-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a8c34-124">**Element**</span></span>|<span data-ttu-id="a8c34-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8c34-125">**Type**</span></span>|<span data-ttu-id="a8c34-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8c34-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8c34-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="a8c34-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a8c34-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a8c34-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8c34-129">Cette énumération spécifie une référence à une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="a8c34-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a8c34-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8c34-130">Attributes</span></span>

|<span data-ttu-id="a8c34-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a8c34-131">**Attribute**</span></span>|<span data-ttu-id="a8c34-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8c34-132">**Type**</span></span>|<span data-ttu-id="a8c34-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a8c34-133">**Required**</span></span>|<span data-ttu-id="a8c34-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8c34-134">**Description**</span></span>|<span data-ttu-id="a8c34-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a8c34-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8c34-136">E</span><span class="sxs-lookup"><span data-stu-id="a8c34-136">E</span></span>  <br/> |<span data-ttu-id="a8c34-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c34-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c34-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8c34-138">optional</span></span>  <br/> |<span data-ttu-id="a8c34-139">Indique que la formule génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="a8c34-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="a8c34-140">La valeur **E** est la valeur actuelle (chaîne de message d'erreur); la valeur de l'attribut **V** est la dernière valeur valide.</span><span class="sxs-lookup"><span data-stu-id="a8c34-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="a8c34-141">Chaîne de message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="a8c34-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="a8c34-142">F</span><span class="sxs-lookup"><span data-stu-id="a8c34-142">F</span></span>  <br/> |<span data-ttu-id="a8c34-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c34-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c34-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8c34-144">optional</span></span>  <br/> | <span data-ttu-id="a8c34-145">Représente la formule de l'élément.</span><span class="sxs-lookup"><span data-stu-id="a8c34-145">Represents the element's formula.</span></span> <span data-ttu-id="a8c34-146">Cet attribut peut contenir l'une des chaînes suivantes:</span><span class="sxs-lookup"><span data-stu-id="a8c34-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="a8c34-147">' (une formule) 'si la formule existe localement</span><span class="sxs-lookup"><span data-stu-id="a8c34-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="a8c34-148">`No Formula`Si la formule est supprimée ou bloquée localement</span><span class="sxs-lookup"><span data-stu-id="a8c34-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="a8c34-149">`Inh`Si la formule est héritée.</span><span class="sxs-lookup"><span data-stu-id="a8c34-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="a8c34-150">Une formule.</span><span class="sxs-lookup"><span data-stu-id="a8c34-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="a8c34-151">N</span><span class="sxs-lookup"><span data-stu-id="a8c34-151">N</span></span>  <br/> |<span data-ttu-id="a8c34-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c34-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c34-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8c34-153">required</span></span>  <br/> |<span data-ttu-id="a8c34-154">Représente le nom de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c34-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="a8c34-155">Nom de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c34-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="a8c34-156">Consultez la section Remarques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a8c34-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="a8c34-157">U</span><span class="sxs-lookup"><span data-stu-id="a8c34-157">U</span></span>  <br/> |<span data-ttu-id="a8c34-158">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c34-158">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c34-159">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8c34-159">optional</span></span>  <br/> |<span data-ttu-id="a8c34-160">Représente une unité de mesure la valeur par défaut est DL.</span><span class="sxs-lookup"><span data-stu-id="a8c34-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="a8c34-161">Unités de la cellule.</span><span class="sxs-lookup"><span data-stu-id="a8c34-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="a8c34-162">V</span><span class="sxs-lookup"><span data-stu-id="a8c34-162">V</span></span>  <br/> |<span data-ttu-id="a8c34-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c34-163">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c34-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8c34-164">optional</span></span>  <br/> |<span data-ttu-id="a8c34-165">Représente la valeur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="a8c34-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="a8c34-166">Valeur de la cellule ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c34-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8c34-167">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8c34-167">Remarks</span></span>

<span data-ttu-id="a8c34-168">L'attribut **N** de cet élément de **cellule** doit correspondre à l'un des jeux de valeurs limités qui correspondent aux cellules de la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c34-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="a8c34-169">RePortez-vous au tableau ci-dessous pour déterminer les valeurs de l'attribut **N** qui sont autorisées pour cet élément de **cellule** .</span><span class="sxs-lookup"><span data-stu-id="a8c34-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="a8c34-170">**Value**</span><span class="sxs-lookup"><span data-stu-id="a8c34-170">**Value**</span></span>|<span data-ttu-id="a8c34-171">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8c34-171">**Description**</span></span>|<span data-ttu-id="a8c34-172">**Plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="a8c34-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8c34-173">X</span><span class="sxs-lookup"><span data-stu-id="a8c34-173">X</span></span>  <br/> |<span data-ttu-id="a8c34-174">Coordonnée x du sommet de fin d'un segment de droite.</span><span class="sxs-lookup"><span data-stu-id="a8c34-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="a8c34-175">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="a8c34-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="a8c34-176">v</span><span class="sxs-lookup"><span data-stu-id="a8c34-176">Y</span></span>  <br/> |<span data-ttu-id="a8c34-177">Coordonnée y du sommet de fin d'un segment de droite.</span><span class="sxs-lookup"><span data-stu-id="a8c34-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="a8c34-178">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="a8c34-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

