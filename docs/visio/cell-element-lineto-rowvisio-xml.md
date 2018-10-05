---
title: Élément de cellule (ligne LineTo) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Contient x- ou la coordonnée y du sommet de fin d’un segment de trait droit.
ms.openlocfilehash: 5b7d8128cbef57c4dd9fb69d5b82e1c1c2ccef68
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386592"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="2a2d2-103">Élément de cellule (ligne LineTo) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="2a2d2-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="2a2d2-104">Contient x- ou la coordonnée y du sommet de fin d’un segment de trait droit.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a2d2-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="2a2d2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a2d2-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2a2d2-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2a2d2-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2a2d2-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2a2d2-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2a2d2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2a2d2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2a2d2-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2a2d2-112">master # .xml, page # .xml</span><span class="sxs-lookup"><span data-stu-id="2a2d2-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2a2d2-113">Définition</span><span class="sxs-lookup"><span data-stu-id="2a2d2-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2a2d2-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2a2d2-114">Elements and attributes</span></span>

<span data-ttu-id="2a2d2-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2a2d2-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2a2d2-116">Parent elements</span></span>

|<span data-ttu-id="2a2d2-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-117">**Element**</span></span>|<span data-ttu-id="2a2d2-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-118">**Type**</span></span>|<span data-ttu-id="2a2d2-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2a2d2-120">Row, élément (Geometry)</span><span class="sxs-lookup"><span data-stu-id="2a2d2-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2a2d2-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="2a2d2-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2a2d2-122">Contient x- ou la coordonnée y du sommet de fin d’un segment de trait droit.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2a2d2-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a2d2-123">Child elements</span></span>

|<span data-ttu-id="2a2d2-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-124">**Element**</span></span>|<span data-ttu-id="2a2d2-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-125">**Type**</span></span>|<span data-ttu-id="2a2d2-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2a2d2-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="2a2d2-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2a2d2-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="2a2d2-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2a2d2-129">Spécifie une référence à une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2a2d2-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="2a2d2-130">Attributes</span></span>

|<span data-ttu-id="2a2d2-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-131">**Attribute**</span></span>|<span data-ttu-id="2a2d2-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-132">**Type**</span></span>|<span data-ttu-id="2a2d2-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-133">**Required**</span></span>|<span data-ttu-id="2a2d2-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-134">**Description**</span></span>|<span data-ttu-id="2a2d2-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2a2d2-136">E</span><span class="sxs-lookup"><span data-stu-id="2a2d2-136">E</span></span>  <br/> |<span data-ttu-id="2a2d2-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2a2d2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2a2d2-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="2a2d2-138">optional</span></span>  <br/> |<span data-ttu-id="2a2d2-139">Indique que la formule génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="2a2d2-140">La valeur de **E** est la valeur actuelle (chaîne message d’erreur) ; la valeur de l’attribut de **V** est la dernière valeur valide.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="2a2d2-141">Chaîne de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="2a2d2-142">F</span><span class="sxs-lookup"><span data-stu-id="2a2d2-142">F</span></span>  <br/> |<span data-ttu-id="2a2d2-143">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2a2d2-143">xsd:string</span></span>  <br/> |<span data-ttu-id="2a2d2-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="2a2d2-144">optional</span></span>  <br/> | <span data-ttu-id="2a2d2-145">Représente la formule de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-145">Represents the element's formula.</span></span> <span data-ttu-id="2a2d2-146">Cet attribut peut contenir une des chaînes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a2d2-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="2a2d2-147">« (une formule) » si la formule existe localement</span><span class="sxs-lookup"><span data-stu-id="2a2d2-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="2a2d2-148">`No Formula`Si la formule est localement supprimée ou bloquée</span><span class="sxs-lookup"><span data-stu-id="2a2d2-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="2a2d2-149">`Inh`Si la formule est héritée.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="2a2d2-150">Une formule.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="2a2d2-151">N</span><span class="sxs-lookup"><span data-stu-id="2a2d2-151">N</span></span>  <br/> |<span data-ttu-id="2a2d2-152">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2a2d2-152">xsd:string</span></span>  <br/> |<span data-ttu-id="2a2d2-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2a2d2-153">required</span></span>  <br/> |<span data-ttu-id="2a2d2-154">Représente le nom de la cellule de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="2a2d2-155">Le nom de la cellule de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="2a2d2-156">Voir la section Remarques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="2a2d2-157">U</span><span class="sxs-lookup"><span data-stu-id="2a2d2-157">U</span></span>  <br/> |<span data-ttu-id="2a2d2-158">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2a2d2-158">xsd:string</span></span>  <br/> |<span data-ttu-id="2a2d2-159">facultatif</span><span class="sxs-lookup"><span data-stu-id="2a2d2-159">optional</span></span>  <br/> |<span data-ttu-id="2a2d2-160">Représente une unité de mesure par défaut est la liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="2a2d2-161">Unités de la cellule.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="2a2d2-162">V</span><span class="sxs-lookup"><span data-stu-id="2a2d2-162">V</span></span>  <br/> |<span data-ttu-id="2a2d2-163">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2a2d2-163">xsd:string</span></span>  <br/> |<span data-ttu-id="2a2d2-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="2a2d2-164">optional</span></span>  <br/> |<span data-ttu-id="2a2d2-165">Représente la valeur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="2a2d2-166">La valeur de la cellule de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a2d2-167">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a2d2-167">Remarks</span></span>

<span data-ttu-id="2a2d2-168">L’attribut **N** de cet élément de **cellule** doit être un ensemble limité de valeurs qui correspondent à des cellules ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="2a2d2-169">Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de **cellule** .</span><span class="sxs-lookup"><span data-stu-id="2a2d2-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="2a2d2-170">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-170">**Value**</span></span>|<span data-ttu-id="2a2d2-171">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-171">**Description**</span></span>|<span data-ttu-id="2a2d2-172">**Plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="2a2d2-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a2d2-173">X </span><span class="sxs-lookup"><span data-stu-id="2a2d2-173">X</span></span>  <br/> |<span data-ttu-id="2a2d2-174">Coordonnée x du sommet de fin d'un segment de droite.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="2a2d2-175">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="2a2d2-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="2a2d2-176">Y</span><span class="sxs-lookup"><span data-stu-id="2a2d2-176">Y</span></span>  <br/> |<span data-ttu-id="2a2d2-177">Coordonnée y du sommet de fin d’un segment de trait droit.</span><span class="sxs-lookup"><span data-stu-id="2a2d2-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="2a2d2-178">LineTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="2a2d2-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

