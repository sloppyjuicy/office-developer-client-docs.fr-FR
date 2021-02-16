---
title: Row, élément (section Actions) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.
ms.openlocfilehash: dfe23aa7d635fc09d625c414e5548a0166384fbb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540412"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="4b655-103">Row, élément (section Actions) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4b655-103">Row element (Actions Section) (Visio XML)</span></span>

<span data-ttu-id="4b655-104">Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.</span><span class="sxs-lookup"><span data-stu-id="4b655-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b655-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="4b655-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b655-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4b655-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4b655-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="4b655-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4b655-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4b655-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4b655-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4b655-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4b655-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4b655-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4b655-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="4b655-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4b655-112">masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="4b655-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b655-113">Définition</span><span class="sxs-lookup"><span data-stu-id="4b655-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4b655-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4b655-114">Elements and attributes</span></span>

<span data-ttu-id="4b655-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="4b655-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4b655-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4b655-116">Parent elements</span></span>

|<span data-ttu-id="4b655-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4b655-117">**Element**</span></span>|<span data-ttu-id="4b655-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4b655-118">**Type**</span></span>|<span data-ttu-id="4b655-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b655-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b655-120">Section</span><span class="sxs-lookup"><span data-stu-id="4b655-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b655-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="4b655-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b655-122">Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.</span><span class="sxs-lookup"><span data-stu-id="4b655-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4b655-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4b655-123">Child elements</span></span>

|<span data-ttu-id="4b655-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4b655-124">**Element**</span></span>|<span data-ttu-id="4b655-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4b655-125">**Type**</span></span>|<span data-ttu-id="4b655-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b655-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b655-127">Cell</span><span class="sxs-lookup"><span data-stu-id="4b655-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="4b655-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4b655-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b655-129">Spécifie une propriété d’une action associée à une commande personnalisée dans un menu de raccourci ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="4b655-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4b655-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="4b655-130">Attributes</span></span>

|<span data-ttu-id="4b655-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4b655-131">**Attribute**</span></span>|<span data-ttu-id="4b655-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="4b655-132">**Type**</span></span>|<span data-ttu-id="4b655-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4b655-133">**Required**</span></span>|<span data-ttu-id="4b655-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b655-134">**Description**</span></span>|<span data-ttu-id="4b655-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4b655-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b655-136">Del</span><span class="sxs-lookup"><span data-stu-id="4b655-136">Del</span></span>  <br/> |<span data-ttu-id="4b655-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4b655-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4b655-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b655-138">optional</span></span>  <br/> |<span data-ttu-id="4b655-139">Spécifie si une ligne qui sinon serait héritée d’une forme de forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="4b655-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="4b655-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4b655-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4b655-141">IX</span><span class="sxs-lookup"><span data-stu-id="4b655-141">IX</span></span>  <br/> |<span data-ttu-id="4b655-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b655-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b655-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b655-143">optional</span></span>  <br/> |<span data-ttu-id="4b655-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="4b655-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="4b655-145">Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="4b655-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="4b655-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="4b655-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4b655-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b655-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b655-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="4b655-148">LocalName</span></span>  <br/> |<span data-ttu-id="4b655-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4b655-149">xsd:string</span></span>  <br/> |<span data-ttu-id="4b655-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b655-150">optional</span></span>  <br/> |<span data-ttu-id="4b655-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="4b655-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="4b655-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4b655-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b655-153">N</span><span class="sxs-lookup"><span data-stu-id="4b655-153">N</span></span>  <br/> |<span data-ttu-id="4b655-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4b655-154">xsd:string</span></span>  <br/> |<span data-ttu-id="4b655-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b655-155">optional</span></span>  <br/> |<span data-ttu-id="4b655-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="4b655-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="4b655-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="4b655-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4b655-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4b655-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b655-159">T</span><span class="sxs-lookup"><span data-stu-id="4b655-159">T</span></span>  <br/> |<span data-ttu-id="4b655-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4b655-160">xsd:string</span></span>  <br/> |<span data-ttu-id="4b655-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b655-161">optional</span></span>  <br/> |<span data-ttu-id="4b655-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="4b655-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="4b655-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="4b655-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="4b655-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4b655-164">Values of the xsd:string type.</span></span>  <br/> |
   

