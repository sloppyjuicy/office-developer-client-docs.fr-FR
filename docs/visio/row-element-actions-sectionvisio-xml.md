---
title: Row, élément (Actions Section) (Visio XML)
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
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="68578-103">Row, élément (Actions Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="68578-103">Row element (Actions Section) (Visio XML)</span></span>

<span data-ttu-id="68578-104">Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.</span><span class="sxs-lookup"><span data-stu-id="68578-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68578-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="68578-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68578-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="68578-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68578-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="68578-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68578-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68578-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68578-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="68578-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68578-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="68578-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68578-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="68578-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68578-112">masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="68578-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68578-113">Définition</span><span class="sxs-lookup"><span data-stu-id="68578-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68578-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="68578-114">Elements and attributes</span></span>

<span data-ttu-id="68578-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="68578-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68578-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="68578-116">Parent elements</span></span>

|<span data-ttu-id="68578-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="68578-117">**Element**</span></span>|<span data-ttu-id="68578-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="68578-118">**Type**</span></span>|<span data-ttu-id="68578-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="68578-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68578-120">Section</span><span class="sxs-lookup"><span data-stu-id="68578-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68578-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="68578-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68578-122">Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.</span><span class="sxs-lookup"><span data-stu-id="68578-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68578-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="68578-123">Child elements</span></span>

|<span data-ttu-id="68578-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="68578-124">**Element**</span></span>|<span data-ttu-id="68578-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="68578-125">**Type**</span></span>|<span data-ttu-id="68578-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="68578-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68578-127">Cell</span><span class="sxs-lookup"><span data-stu-id="68578-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="68578-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="68578-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68578-129">Spécifie une propriété d’une action associée à une commande personnalisée dans un menu de raccourci ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="68578-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="68578-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="68578-130">Attributes</span></span>

|<span data-ttu-id="68578-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68578-131">**Attribute**</span></span>|<span data-ttu-id="68578-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="68578-132">**Type**</span></span>|<span data-ttu-id="68578-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="68578-133">**Required**</span></span>|<span data-ttu-id="68578-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="68578-134">**Description**</span></span>|<span data-ttu-id="68578-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="68578-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68578-136">Del</span><span class="sxs-lookup"><span data-stu-id="68578-136">Del</span></span>  <br/> |<span data-ttu-id="68578-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="68578-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="68578-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="68578-138">optional</span></span>  <br/> |<span data-ttu-id="68578-139">Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="68578-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="68578-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="68578-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="68578-141">IX</span><span class="sxs-lookup"><span data-stu-id="68578-141">IX</span></span>  <br/> |<span data-ttu-id="68578-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68578-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68578-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="68578-143">optional</span></span>  <br/> |<span data-ttu-id="68578-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="68578-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="68578-145">Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="68578-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="68578-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="68578-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="68578-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="68578-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68578-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="68578-148">LocalName</span></span>  <br/> |<span data-ttu-id="68578-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="68578-149">xsd:string</span></span>  <br/> |<span data-ttu-id="68578-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="68578-150">optional</span></span>  <br/> |<span data-ttu-id="68578-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="68578-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="68578-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="68578-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="68578-153">N</span><span class="sxs-lookup"><span data-stu-id="68578-153">N</span></span>  <br/> |<span data-ttu-id="68578-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="68578-154">xsd:string</span></span>  <br/> |<span data-ttu-id="68578-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="68578-155">optional</span></span>  <br/> |<span data-ttu-id="68578-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="68578-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="68578-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="68578-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="68578-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="68578-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="68578-159">T</span><span class="sxs-lookup"><span data-stu-id="68578-159">T</span></span>  <br/> |<span data-ttu-id="68578-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="68578-160">xsd:string</span></span>  <br/> |<span data-ttu-id="68578-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="68578-161">optional</span></span>  <br/> |<span data-ttu-id="68578-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="68578-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="68578-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="68578-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="68578-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="68578-164">Values of the xsd:string type.</span></span>  <br/> |
   

