---
title: Élément de ligne (section dégradé de lignes) («Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Contient la couleur, la transparence et la position d'un point de dégradé pour un dégradé de ligne.
ms.openlocfilehash: 105d93344343f223a6b5d909f1174f7df56ffb4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358428"
---
# <a name="row-element-line-gradient-section-visio-xml"></a><span data-ttu-id="65cd0-103">Élément de ligne (section dégradé de lignes) («Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="65cd0-103">Row element (Line Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="65cd0-104">Contient la couleur, la transparence et la position d'un point de dégradé pour un dégradé de ligne.</span><span class="sxs-lookup"><span data-stu-id="65cd0-104">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65cd0-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="65cd0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65cd0-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="65cd0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="65cd0-107">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="65cd0-107">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="65cd0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65cd0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="65cd0-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="65cd0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="65cd0-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="65cd0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="65cd0-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="65cd0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="65cd0-112">document. xml, Master #. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="65cd0-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65cd0-113">Définition</span><span class="sxs-lookup"><span data-stu-id="65cd0-113">Definition</span></span>

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65cd0-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="65cd0-114">Elements and attributes</span></span>

<span data-ttu-id="65cd0-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="65cd0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="65cd0-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="65cd0-116">Parent elements</span></span>

|<span data-ttu-id="65cd0-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="65cd0-117">**Element**</span></span>|<span data-ttu-id="65cd0-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="65cd0-118">**Type**</span></span>|<span data-ttu-id="65cd0-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="65cd0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65cd0-120">Section</span><span class="sxs-lookup"><span data-stu-id="65cd0-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65cd0-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="65cd0-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65cd0-122">Contient la couleur, la transparence et la position d'un point de dégradé pour un dégradé de ligne.</span><span class="sxs-lookup"><span data-stu-id="65cd0-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65cd0-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="65cd0-123">Child elements</span></span>

|<span data-ttu-id="65cd0-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="65cd0-124">**Element**</span></span>|<span data-ttu-id="65cd0-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="65cd0-125">**Type**</span></span>|<span data-ttu-id="65cd0-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="65cd0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65cd0-127">Cell</span><span class="sxs-lookup"><span data-stu-id="65cd0-127">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="65cd0-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="65cd0-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65cd0-129">Spécifie une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="65cd0-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="65cd0-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="65cd0-130">Attributes</span></span>

|<span data-ttu-id="65cd0-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="65cd0-131">**Attribute**</span></span>|<span data-ttu-id="65cd0-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="65cd0-132">**Type**</span></span>|<span data-ttu-id="65cd0-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="65cd0-133">**Required**</span></span>|<span data-ttu-id="65cd0-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="65cd0-134">**Description**</span></span>|<span data-ttu-id="65cd0-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="65cd0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65cd0-136">Suppr</span><span class="sxs-lookup"><span data-stu-id="65cd0-136">Del</span></span>  <br/> |<span data-ttu-id="65cd0-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="65cd0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="65cd0-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="65cd0-138">optional</span></span>  <br/> |<span data-ttu-id="65cd0-139">Indique si une ligne qui serait normalement héritée d'une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="65cd0-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="65cd0-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="65cd0-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="65cd0-141">IX</span><span class="sxs-lookup"><span data-stu-id="65cd0-141">IX</span></span>  <br/> |<span data-ttu-id="65cd0-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65cd0-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65cd0-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="65cd0-143">optional</span></span>  <br/> |<span data-ttu-id="65cd0-144">Spécifie l'identificateur de base 1 de la ligne.</span><span class="sxs-lookup"><span data-stu-id="65cd0-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="65cd0-145">Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L'attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs.</span><span class="sxs-lookup"><span data-stu-id="65cd0-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="65cd0-146">Une ligne ne peut avoir qu'un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="65cd0-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="65cd0-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="65cd0-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65cd0-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="65cd0-148">LocalName</span></span>  <br/> |<span data-ttu-id="65cd0-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="65cd0-149">xsd:string</span></span>  <br/> |<span data-ttu-id="65cd0-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="65cd0-150">optional</span></span>  <br/> |<span data-ttu-id="65cd0-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="65cd0-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="65cd0-152">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="65cd0-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65cd0-153">N</span><span class="sxs-lookup"><span data-stu-id="65cd0-153">N</span></span>  <br/> |<span data-ttu-id="65cd0-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="65cd0-154">xsd:string</span></span>  <br/> |<span data-ttu-id="65cd0-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="65cd0-155">optional</span></span>  <br/> |<span data-ttu-id="65cd0-156">Spécifie le nom unique indépendant de la langue de la ligne. L'attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, hyperLink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="65cd0-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="65cd0-157">Une ligne ne peut avoir qu'un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="65cd0-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="65cd0-158">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="65cd0-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65cd0-159">T</span><span class="sxs-lookup"><span data-stu-id="65cd0-159">T</span></span>  <br/> |<span data-ttu-id="65cd0-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="65cd0-160">xsd:string</span></span>  <br/> |<span data-ttu-id="65cd0-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="65cd0-161">optional</span></span>  <br/> |<span data-ttu-id="65cd0-162">Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="65cd0-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="65cd0-163">L'attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="65cd0-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="65cd0-164">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="65cd0-164">Values of the xsd:string type.</span></span>  <br/> |
   

