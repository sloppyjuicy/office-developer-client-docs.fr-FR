---
title: Élément de ligne (section actions) («Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "32356419"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="70903-103">Élément de ligne (section actions) («Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="70903-103">Row element (Actions Section) ('Visio XML')</span></span>

<span data-ttu-id="70903-104">Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.</span><span class="sxs-lookup"><span data-stu-id="70903-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70903-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="70903-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70903-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="70903-106">**Element type**</span></span> <br/> |[<span data-ttu-id="70903-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="70903-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="70903-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="70903-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="70903-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="70903-109">**Schema file**</span></span> <br/> |<span data-ttu-id="70903-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="70903-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="70903-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="70903-111">**Document parts**</span></span> <br/> |<span data-ttu-id="70903-112">Masters. xml, Master #. xml, pages. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="70903-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70903-113">Définition</span><span class="sxs-lookup"><span data-stu-id="70903-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70903-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="70903-114">Elements and attributes</span></span>

<span data-ttu-id="70903-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="70903-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="70903-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="70903-116">Parent elements</span></span>

|<span data-ttu-id="70903-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="70903-117">**Element**</span></span>|<span data-ttu-id="70903-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="70903-118">**Type**</span></span>|<span data-ttu-id="70903-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="70903-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70903-120">Section</span><span class="sxs-lookup"><span data-stu-id="70903-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70903-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="70903-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70903-122">Contient des lignes qui décrivent les options de menu contextuel ou de balise d’action d’une forme ou d’une page.</span><span class="sxs-lookup"><span data-stu-id="70903-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="70903-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="70903-123">Child elements</span></span>

|<span data-ttu-id="70903-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="70903-124">**Element**</span></span>|<span data-ttu-id="70903-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="70903-125">**Type**</span></span>|<span data-ttu-id="70903-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="70903-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70903-127">Cellule</span><span class="sxs-lookup"><span data-stu-id="70903-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="70903-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="70903-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70903-129">Spécifie une propriété d'une action associée à une commande personnalisée dans un menu contextuel ou de balise d'action.</span><span class="sxs-lookup"><span data-stu-id="70903-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="70903-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="70903-130">Attributes</span></span>

|<span data-ttu-id="70903-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="70903-131">**Attribute**</span></span>|<span data-ttu-id="70903-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="70903-132">**Type**</span></span>|<span data-ttu-id="70903-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="70903-133">**Required**</span></span>|<span data-ttu-id="70903-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="70903-134">**Description**</span></span>|<span data-ttu-id="70903-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="70903-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70903-136">Suppr</span><span class="sxs-lookup"><span data-stu-id="70903-136">Del</span></span>  <br/> |<span data-ttu-id="70903-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="70903-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="70903-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="70903-138">optional</span></span>  <br/> |<span data-ttu-id="70903-139">Indique si une ligne qui serait normalement héritée d'une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="70903-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="70903-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="70903-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="70903-141">IX</span><span class="sxs-lookup"><span data-stu-id="70903-141">IX</span></span>  <br/> |<span data-ttu-id="70903-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70903-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70903-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="70903-143">optional</span></span>  <br/> |<span data-ttu-id="70903-144">Spécifie l'identificateur de base 1 de la ligne.</span><span class="sxs-lookup"><span data-stu-id="70903-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="70903-145">Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L'attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs.</span><span class="sxs-lookup"><span data-stu-id="70903-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="70903-146">Une ligne ne peut avoir qu'un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="70903-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="70903-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70903-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70903-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="70903-148">LocalName</span></span>  <br/> |<span data-ttu-id="70903-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="70903-149">xsd:string</span></span>  <br/> |<span data-ttu-id="70903-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="70903-150">optional</span></span>  <br/> |<span data-ttu-id="70903-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="70903-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="70903-152">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="70903-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70903-153">N</span><span class="sxs-lookup"><span data-stu-id="70903-153">N</span></span>  <br/> |<span data-ttu-id="70903-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="70903-154">xsd:string</span></span>  <br/> |<span data-ttu-id="70903-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="70903-155">optional</span></span>  <br/> |<span data-ttu-id="70903-156">Spécifie le nom unique indépendant de la langue de la ligne. L'attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, hyperLink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="70903-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="70903-157">Une ligne ne peut avoir qu'un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="70903-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="70903-158">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="70903-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70903-159">T</span><span class="sxs-lookup"><span data-stu-id="70903-159">T</span></span>  <br/> |<span data-ttu-id="70903-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="70903-160">xsd:string</span></span>  <br/> |<span data-ttu-id="70903-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="70903-161">optional</span></span>  <br/> |<span data-ttu-id="70903-162">Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="70903-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="70903-163">L'attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="70903-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="70903-164">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="70903-164">Values of the xsd:string type.</span></span>  <br/> |
   

