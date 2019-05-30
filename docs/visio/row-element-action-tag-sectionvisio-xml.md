---
title: Élément de ligne (section balise d’action) (Visio XML)
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
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="3ef0a-103">Élément de ligne (section balise d’action) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3ef0a-103">Row element (Action Tag Section) (Visio XML)</span></span>

<span data-ttu-id="3ef0a-104">Définit une balise d’action sur une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ef0a-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="3ef0a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ef0a-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3ef0a-107">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="3ef0a-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3ef0a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3ef0a-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3ef0a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3ef0a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3ef0a-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3ef0a-112">Masters. xml, Master #. xml, pages. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="3ef0a-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ef0a-113">Définition</span><span class="sxs-lookup"><span data-stu-id="3ef0a-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ef0a-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3ef0a-114">Elements and attributes</span></span>

<span data-ttu-id="3ef0a-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3ef0a-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3ef0a-116">Parent elements</span></span>

|<span data-ttu-id="3ef0a-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-117">**Element**</span></span>|<span data-ttu-id="3ef0a-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-118">**Type**</span></span>|<span data-ttu-id="3ef0a-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ef0a-120">Section</span><span class="sxs-lookup"><span data-stu-id="3ef0a-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ef0a-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="3ef0a-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ef0a-122">Définit une balise d’action sur une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ef0a-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3ef0a-123">Child elements</span></span>

|<span data-ttu-id="3ef0a-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-124">**Element**</span></span>|<span data-ttu-id="3ef0a-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-125">**Type**</span></span>|<span data-ttu-id="3ef0a-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ef0a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="3ef0a-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="3ef0a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3ef0a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ef0a-129">Définit une propriété pour une balise d’action sur une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3ef0a-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ef0a-130">Attributes</span></span>

|<span data-ttu-id="3ef0a-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-131">**Attribute**</span></span>|<span data-ttu-id="3ef0a-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-132">**Type**</span></span>|<span data-ttu-id="3ef0a-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-133">**Required**</span></span>|<span data-ttu-id="3ef0a-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-134">**Description**</span></span>|<span data-ttu-id="3ef0a-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="3ef0a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ef0a-136">Suppr</span><span class="sxs-lookup"><span data-stu-id="3ef0a-136">Del</span></span>  <br/> |<span data-ttu-id="3ef0a-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="3ef0a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3ef0a-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="3ef0a-138">optional</span></span>  <br/> |<span data-ttu-id="3ef0a-139">Indique si une ligne qui serait normalement héritée d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="3ef0a-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3ef0a-141">IX</span><span class="sxs-lookup"><span data-stu-id="3ef0a-141">IX</span></span>  <br/> |<span data-ttu-id="3ef0a-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3ef0a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3ef0a-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="3ef0a-143">optional</span></span>  <br/> |<span data-ttu-id="3ef0a-144">Spécifie l’identificateur de base 1 de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="3ef0a-145">Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="3ef0a-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="3ef0a-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3ef0a-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="3ef0a-148">LocalName</span></span>  <br/> |<span data-ttu-id="3ef0a-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3ef0a-149">xsd:string</span></span>  <br/> |<span data-ttu-id="3ef0a-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="3ef0a-150">optional</span></span>  <br/> |<span data-ttu-id="3ef0a-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="3ef0a-152">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3ef0a-153">N</span><span class="sxs-lookup"><span data-stu-id="3ef0a-153">N</span></span>  <br/> |<span data-ttu-id="3ef0a-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3ef0a-154">xsd:string</span></span>  <br/> |<span data-ttu-id="3ef0a-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="3ef0a-155">optional</span></span>  <br/> |<span data-ttu-id="3ef0a-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, HYPERLINK et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="3ef0a-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="3ef0a-158">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3ef0a-159">T</span><span class="sxs-lookup"><span data-stu-id="3ef0a-159">T</span></span>  <br/> |<span data-ttu-id="3ef0a-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3ef0a-160">xsd:string</span></span>  <br/> |<span data-ttu-id="3ef0a-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="3ef0a-161">optional</span></span>  <br/> |<span data-ttu-id="3ef0a-162">Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="3ef0a-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="3ef0a-164">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3ef0a-164">Values of the xsd:string type.</span></span>  <br/> |
   

