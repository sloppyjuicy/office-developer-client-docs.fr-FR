---
title: Élément de ligne (section Scratch) (Visio XML)
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
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="18280-103">Élément de ligne (section Scratch) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="18280-103">Row element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="18280-104">Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.</span><span class="sxs-lookup"><span data-stu-id="18280-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18280-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="18280-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18280-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="18280-106">**Element type**</span></span> <br/> |[<span data-ttu-id="18280-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="18280-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="18280-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="18280-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="18280-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="18280-109">**Schema file**</span></span> <br/> |<span data-ttu-id="18280-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="18280-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="18280-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="18280-111">**Document parts**</span></span> <br/> |<span data-ttu-id="18280-112">document. xml, Masters. xml, Master #. xml, pages. xml, page #. Xml</span><span class="sxs-lookup"><span data-stu-id="18280-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18280-113">Définition</span><span class="sxs-lookup"><span data-stu-id="18280-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="18280-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="18280-114">Elements and attributes</span></span>

<span data-ttu-id="18280-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="18280-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="18280-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="18280-116">Parent elements</span></span>

|<span data-ttu-id="18280-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="18280-117">**Element**</span></span>|<span data-ttu-id="18280-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="18280-118">**Type**</span></span>|<span data-ttu-id="18280-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="18280-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18280-120">Section</span><span class="sxs-lookup"><span data-stu-id="18280-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="18280-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="18280-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="18280-122">Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.</span><span class="sxs-lookup"><span data-stu-id="18280-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18280-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="18280-123">Child elements</span></span>

|<span data-ttu-id="18280-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="18280-124">**Element**</span></span>|<span data-ttu-id="18280-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="18280-125">**Type**</span></span>|<span data-ttu-id="18280-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="18280-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18280-127">Cell</span><span class="sxs-lookup"><span data-stu-id="18280-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="18280-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="18280-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="18280-129">Spécifie une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="18280-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="18280-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="18280-130">Attributes</span></span>

|<span data-ttu-id="18280-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="18280-131">**Attribute**</span></span>|<span data-ttu-id="18280-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="18280-132">**Type**</span></span>|<span data-ttu-id="18280-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="18280-133">**Required**</span></span>|<span data-ttu-id="18280-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="18280-134">**Description**</span></span>|<span data-ttu-id="18280-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="18280-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="18280-136">Suppr</span><span class="sxs-lookup"><span data-stu-id="18280-136">Del</span></span>  <br/> |<span data-ttu-id="18280-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="18280-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="18280-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="18280-138">optional</span></span>  <br/> |<span data-ttu-id="18280-139">Indique si une ligne qui serait normalement héritée d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="18280-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="18280-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="18280-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="18280-141">IX</span><span class="sxs-lookup"><span data-stu-id="18280-141">IX</span></span>  <br/> |<span data-ttu-id="18280-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="18280-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="18280-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="18280-143">optional</span></span>  <br/> |<span data-ttu-id="18280-144">Spécifie l’identificateur de base 1 de la ligne.</span><span class="sxs-lookup"><span data-stu-id="18280-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="18280-145">Elle doit être unique et supérieure à celle des autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paragraph, Reviewer, Scratch et tabs.</span><span class="sxs-lookup"><span data-stu-id="18280-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="18280-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="18280-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="18280-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="18280-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="18280-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="18280-148">LocalName</span></span>  <br/> |<span data-ttu-id="18280-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="18280-149">xsd:string</span></span>  <br/> |<span data-ttu-id="18280-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="18280-150">optional</span></span>  <br/> |<span data-ttu-id="18280-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="18280-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="18280-152">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="18280-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="18280-153">N</span><span class="sxs-lookup"><span data-stu-id="18280-153">N</span></span>  <br/> |<span data-ttu-id="18280-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="18280-154">xsd:string</span></span>  <br/> |<span data-ttu-id="18280-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="18280-155">optional</span></span>  <br/> |<span data-ttu-id="18280-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, actions, Control, Connection, HYPERLINK et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="18280-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="18280-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="18280-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="18280-158">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="18280-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="18280-159">T</span><span class="sxs-lookup"><span data-stu-id="18280-159">T</span></span>  <br/> |<span data-ttu-id="18280-160">xsd: String</span><span class="sxs-lookup"><span data-stu-id="18280-160">xsd:string</span></span>  <br/> |<span data-ttu-id="18280-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="18280-161">optional</span></span>  <br/> |<span data-ttu-id="18280-162">Cette énumération spécifie le type de tracé géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="18280-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="18280-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="18280-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="18280-164">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="18280-164">Values of the xsd:string type.</span></span>  <br/> |
   

