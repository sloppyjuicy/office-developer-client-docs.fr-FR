---
title: Row, élément (Paragraph Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 00ecaa82-3b40-24cc-91c0-b2562e92161d
description: Indique les attributs de mise en forme de paragraphe du texte de la forme, tels que les retraits, l'interligne, les puces et l'alignement horizontal des paragraphes.
ms.openlocfilehash: 48d32f3a0712e2ed3110ced545d5b946f147d755
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540818"
---
# <a name="row-element-paragraph-section-visio-xml"></a><span data-ttu-id="5397d-103">Row, élément (Paragraph Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5397d-103">Row element (Paragraph Section) (Visio XML)</span></span>

<span data-ttu-id="5397d-104">Indique les attributs de mise en forme de paragraphe du texte de la forme, tels que les retraits, l'interligne, les puces et l'alignement horizontal des paragraphes.</span><span class="sxs-lookup"><span data-stu-id="5397d-104">Shows the paragraph formatting attributes for the shape's text, such as indents, line spacing, bullets, and horizontal alignment of paragraphs.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5397d-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="5397d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5397d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="5397d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5397d-107">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="5397d-107">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5397d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5397d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5397d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5397d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5397d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5397d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5397d-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="5397d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5397d-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="5397d-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5397d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="5397d-113">Definition</span></span>

```XML
< xs:element name="Row" type="ParagraphRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5397d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5397d-114">Elements and attributes</span></span>

<span data-ttu-id="5397d-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="5397d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5397d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5397d-116">Parent elements</span></span>

|<span data-ttu-id="5397d-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5397d-117">**Element**</span></span>|<span data-ttu-id="5397d-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="5397d-118">**Type**</span></span>|<span data-ttu-id="5397d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="5397d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5397d-120">Section</span><span class="sxs-lookup"><span data-stu-id="5397d-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5397d-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5397d-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5397d-122">Indique les attributs de mise en forme de paragraphe du texte de la forme, tels que les retraits, l'interligne, les puces et l'alignement horizontal des paragraphes.</span><span class="sxs-lookup"><span data-stu-id="5397d-122">Shows the paragraph formatting attributes for the shape's text, such as indents, line spacing, bullets, and horizontal alignment of paragraphs.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5397d-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5397d-123">Child elements</span></span>

|<span data-ttu-id="5397d-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5397d-124">**Element**</span></span>|<span data-ttu-id="5397d-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="5397d-125">**Type**</span></span>|<span data-ttu-id="5397d-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="5397d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5397d-127">Cell</span><span class="sxs-lookup"><span data-stu-id="5397d-127">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5397d-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5397d-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5397d-129">Spécifie une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="5397d-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5397d-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="5397d-130">Attributes</span></span>

|<span data-ttu-id="5397d-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5397d-131">**Attribute**</span></span>|<span data-ttu-id="5397d-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="5397d-132">**Type**</span></span>|<span data-ttu-id="5397d-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="5397d-133">**Required**</span></span>|<span data-ttu-id="5397d-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="5397d-134">**Description**</span></span>|<span data-ttu-id="5397d-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="5397d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5397d-136">Del</span><span class="sxs-lookup"><span data-stu-id="5397d-136">Del</span></span>  <br/> |<span data-ttu-id="5397d-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5397d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5397d-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="5397d-138">optional</span></span>  <br/> |<span data-ttu-id="5397d-139">Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="5397d-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="5397d-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5397d-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5397d-141">IX</span><span class="sxs-lookup"><span data-stu-id="5397d-141">IX</span></span>  <br/> |<span data-ttu-id="5397d-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5397d-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5397d-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="5397d-143">optional</span></span>  <br/> |<span data-ttu-id="5397d-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="5397d-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="5397d-145">Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="5397d-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="5397d-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="5397d-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="5397d-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5397d-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5397d-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="5397d-148">LocalName</span></span>  <br/> |<span data-ttu-id="5397d-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5397d-149">xsd:string</span></span>  <br/> |<span data-ttu-id="5397d-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="5397d-150">optional</span></span>  <br/> |<span data-ttu-id="5397d-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="5397d-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="5397d-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5397d-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5397d-153">N</span><span class="sxs-lookup"><span data-stu-id="5397d-153">N</span></span>  <br/> |<span data-ttu-id="5397d-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5397d-154">xsd:string</span></span>  <br/> |<span data-ttu-id="5397d-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="5397d-155">optional</span></span>  <br/> |<span data-ttu-id="5397d-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="5397d-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="5397d-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="5397d-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="5397d-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5397d-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5397d-159">T</span><span class="sxs-lookup"><span data-stu-id="5397d-159">T</span></span>  <br/> |<span data-ttu-id="5397d-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5397d-160">xsd:string</span></span>  <br/> |<span data-ttu-id="5397d-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="5397d-161">optional</span></span>  <br/> |<span data-ttu-id="5397d-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="5397d-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="5397d-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="5397d-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="5397d-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5397d-164">Values of the xsd:string type.</span></span>  <br/> |
   

