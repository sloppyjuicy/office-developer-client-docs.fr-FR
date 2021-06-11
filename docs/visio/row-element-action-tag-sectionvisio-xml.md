---
title: Row, élément (Action Tag Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Définit une balise d’action sur une forme ou une page.
ms.openlocfilehash: 44008d43871bfec9b5b943f19ce6ce0a069323d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540426"
---
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="87985-103">Row, élément (Action Tag Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="87985-103">Row element (Action Tag Section) (Visio XML)</span></span>

<span data-ttu-id="87985-104">Définit une balise d’action sur une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="87985-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87985-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="87985-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87985-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="87985-106">**Element type**</span></span> <br/> |[<span data-ttu-id="87985-107">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="87985-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="87985-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87985-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="87985-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="87985-109">**Schema file**</span></span> <br/> |<span data-ttu-id="87985-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="87985-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="87985-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="87985-111">**Document parts**</span></span> <br/> |<span data-ttu-id="87985-112">masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="87985-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87985-113">Définition</span><span class="sxs-lookup"><span data-stu-id="87985-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87985-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="87985-114">Elements and attributes</span></span>

<span data-ttu-id="87985-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="87985-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="87985-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="87985-116">Parent elements</span></span>

|<span data-ttu-id="87985-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="87985-117">**Element**</span></span>|<span data-ttu-id="87985-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="87985-118">**Type**</span></span>|<span data-ttu-id="87985-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="87985-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87985-120">Section</span><span class="sxs-lookup"><span data-stu-id="87985-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87985-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="87985-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87985-122">Définit une balise d’action sur une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="87985-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87985-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="87985-123">Child elements</span></span>

|<span data-ttu-id="87985-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="87985-124">**Element**</span></span>|<span data-ttu-id="87985-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="87985-125">**Type**</span></span>|<span data-ttu-id="87985-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="87985-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87985-127">Cell</span><span class="sxs-lookup"><span data-stu-id="87985-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="87985-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="87985-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87985-129">Définit une propriété pour une balise d’action sur une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="87985-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="87985-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="87985-130">Attributes</span></span>

|<span data-ttu-id="87985-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="87985-131">**Attribute**</span></span>|<span data-ttu-id="87985-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="87985-132">**Type**</span></span>|<span data-ttu-id="87985-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="87985-133">**Required**</span></span>|<span data-ttu-id="87985-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="87985-134">**Description**</span></span>|<span data-ttu-id="87985-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="87985-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="87985-136">Del</span><span class="sxs-lookup"><span data-stu-id="87985-136">Del</span></span>  <br/> |<span data-ttu-id="87985-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="87985-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="87985-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="87985-138">optional</span></span>  <br/> |<span data-ttu-id="87985-139">Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="87985-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="87985-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="87985-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="87985-141">IX</span><span class="sxs-lookup"><span data-stu-id="87985-141">IX</span></span>  <br/> |<span data-ttu-id="87985-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="87985-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="87985-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="87985-143">optional</span></span>  <br/> |<span data-ttu-id="87985-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="87985-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="87985-145">Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="87985-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="87985-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="87985-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="87985-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="87985-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="87985-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="87985-148">LocalName</span></span>  <br/> |<span data-ttu-id="87985-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="87985-149">xsd:string</span></span>  <br/> |<span data-ttu-id="87985-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="87985-150">optional</span></span>  <br/> |<span data-ttu-id="87985-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="87985-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="87985-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="87985-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87985-153">N</span><span class="sxs-lookup"><span data-stu-id="87985-153">N</span></span>  <br/> |<span data-ttu-id="87985-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="87985-154">xsd:string</span></span>  <br/> |<span data-ttu-id="87985-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="87985-155">optional</span></span>  <br/> |<span data-ttu-id="87985-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="87985-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="87985-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="87985-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="87985-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="87985-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87985-159">T</span><span class="sxs-lookup"><span data-stu-id="87985-159">T</span></span>  <br/> |<span data-ttu-id="87985-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="87985-160">xsd:string</span></span>  <br/> |<span data-ttu-id="87985-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="87985-161">optional</span></span>  <br/> |<span data-ttu-id="87985-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="87985-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="87985-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="87985-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="87985-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="87985-164">Values of the xsd:string type.</span></span>  <br/> |
   

