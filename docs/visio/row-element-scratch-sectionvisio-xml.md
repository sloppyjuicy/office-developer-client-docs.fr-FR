---
title: Row, élément (Scratch Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
ms.openlocfilehash: fb346785b9cb6539d970ae1bd1c44fc706bd657d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541000"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="56322-103">Row, élément (Scratch Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="56322-103">Row element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="56322-104">Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.</span><span class="sxs-lookup"><span data-stu-id="56322-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56322-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="56322-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56322-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="56322-106">**Element type**</span></span> <br/> |[<span data-ttu-id="56322-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="56322-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="56322-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="56322-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="56322-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="56322-109">**Schema file**</span></span> <br/> |<span data-ttu-id="56322-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="56322-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="56322-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="56322-111">**Document parts**</span></span> <br/> |<span data-ttu-id="56322-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="56322-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="56322-113">Définition</span><span class="sxs-lookup"><span data-stu-id="56322-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="56322-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="56322-114">Elements and attributes</span></span>

<span data-ttu-id="56322-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="56322-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="56322-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="56322-116">Parent elements</span></span>

|<span data-ttu-id="56322-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="56322-117">**Element**</span></span>|<span data-ttu-id="56322-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="56322-118">**Type**</span></span>|<span data-ttu-id="56322-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="56322-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56322-120">Section</span><span class="sxs-lookup"><span data-stu-id="56322-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="56322-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="56322-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="56322-122">Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.</span><span class="sxs-lookup"><span data-stu-id="56322-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="56322-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="56322-123">Child elements</span></span>

|<span data-ttu-id="56322-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="56322-124">**Element**</span></span>|<span data-ttu-id="56322-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="56322-125">**Type**</span></span>|<span data-ttu-id="56322-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="56322-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56322-127">Cell</span><span class="sxs-lookup"><span data-stu-id="56322-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="56322-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="56322-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="56322-129">Spécifie une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="56322-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="56322-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="56322-130">Attributes</span></span>

|<span data-ttu-id="56322-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="56322-131">**Attribute**</span></span>|<span data-ttu-id="56322-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="56322-132">**Type**</span></span>|<span data-ttu-id="56322-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="56322-133">**Required**</span></span>|<span data-ttu-id="56322-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="56322-134">**Description**</span></span>|<span data-ttu-id="56322-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="56322-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="56322-136">Del</span><span class="sxs-lookup"><span data-stu-id="56322-136">Del</span></span>  <br/> |<span data-ttu-id="56322-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="56322-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="56322-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="56322-138">optional</span></span>  <br/> |<span data-ttu-id="56322-139">Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="56322-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="56322-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="56322-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="56322-141">IX</span><span class="sxs-lookup"><span data-stu-id="56322-141">IX</span></span>  <br/> |<span data-ttu-id="56322-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="56322-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="56322-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="56322-143">optional</span></span>  <br/> |<span data-ttu-id="56322-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="56322-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="56322-145">Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="56322-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="56322-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="56322-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="56322-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="56322-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="56322-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="56322-148">LocalName</span></span>  <br/> |<span data-ttu-id="56322-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="56322-149">xsd:string</span></span>  <br/> |<span data-ttu-id="56322-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="56322-150">optional</span></span>  <br/> |<span data-ttu-id="56322-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="56322-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="56322-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="56322-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="56322-153">N</span><span class="sxs-lookup"><span data-stu-id="56322-153">N</span></span>  <br/> |<span data-ttu-id="56322-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="56322-154">xsd:string</span></span>  <br/> |<span data-ttu-id="56322-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="56322-155">optional</span></span>  <br/> |<span data-ttu-id="56322-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="56322-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="56322-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="56322-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="56322-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="56322-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="56322-159">T</span><span class="sxs-lookup"><span data-stu-id="56322-159">T</span></span>  <br/> |<span data-ttu-id="56322-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="56322-160">xsd:string</span></span>  <br/> |<span data-ttu-id="56322-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="56322-161">optional</span></span>  <br/> |<span data-ttu-id="56322-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="56322-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="56322-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="56322-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="56322-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="56322-164">Values of the xsd:string type.</span></span>  <br/> |
   

