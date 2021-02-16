---
title: Élément Row (Layer Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contient des éléments qui définissent une couche unique et ses propriétés pour une page.
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540861"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="66043-103">Élément Row (Layer Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="66043-103">Row element (Layer Section) (Visio XML)</span></span>

<span data-ttu-id="66043-104">Contient des éléments qui définissent une couche unique et ses propriétés pour une page.</span><span class="sxs-lookup"><span data-stu-id="66043-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66043-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="66043-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66043-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="66043-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66043-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="66043-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66043-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="66043-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66043-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="66043-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66043-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="66043-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66043-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="66043-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66043-112">masters.xml, pages.xml</span><span class="sxs-lookup"><span data-stu-id="66043-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66043-113">Définition</span><span class="sxs-lookup"><span data-stu-id="66043-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66043-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="66043-114">Elements and attributes</span></span>

<span data-ttu-id="66043-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="66043-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66043-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="66043-116">Parent elements</span></span>

|<span data-ttu-id="66043-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="66043-117">**Element**</span></span>|<span data-ttu-id="66043-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="66043-118">**Type**</span></span>|<span data-ttu-id="66043-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="66043-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66043-120">Section</span><span class="sxs-lookup"><span data-stu-id="66043-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66043-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="66043-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66043-122">Contient des éléments qui définissent une couche unique et ses propriétés pour une page.</span><span class="sxs-lookup"><span data-stu-id="66043-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66043-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66043-123">Child elements</span></span>

|<span data-ttu-id="66043-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="66043-124">**Element**</span></span>|<span data-ttu-id="66043-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="66043-125">**Type**</span></span>|<span data-ttu-id="66043-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="66043-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66043-127">Cell</span><span class="sxs-lookup"><span data-stu-id="66043-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="66043-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="66043-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66043-129">Spécifie une propriété pour un calque ou ses propriétés pour une page.</span><span class="sxs-lookup"><span data-stu-id="66043-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="66043-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="66043-130">Attributes</span></span>

|<span data-ttu-id="66043-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="66043-131">**Attribute**</span></span>|<span data-ttu-id="66043-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="66043-132">**Type**</span></span>|<span data-ttu-id="66043-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="66043-133">**Required**</span></span>|<span data-ttu-id="66043-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="66043-134">**Description**</span></span>|<span data-ttu-id="66043-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="66043-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="66043-136">Del</span><span class="sxs-lookup"><span data-stu-id="66043-136">Del</span></span>  <br/> |<span data-ttu-id="66043-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="66043-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="66043-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="66043-138">optional</span></span>  <br/> |<span data-ttu-id="66043-139">Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="66043-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="66043-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="66043-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="66043-141">IX</span><span class="sxs-lookup"><span data-stu-id="66043-141">IX</span></span>  <br/> |<span data-ttu-id="66043-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="66043-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="66043-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="66043-143">optional</span></span>  <br/> |<span data-ttu-id="66043-144">Spécifie l’identificateur à base un de la ligne.</span><span class="sxs-lookup"><span data-stu-id="66043-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="66043-145">Il doit être unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs.</span><span class="sxs-lookup"><span data-stu-id="66043-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="66043-146">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="66043-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="66043-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="66043-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="66043-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="66043-148">LocalName</span></span>  <br/> |<span data-ttu-id="66043-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="66043-149">xsd:string</span></span>  <br/> |<span data-ttu-id="66043-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="66043-150">optional</span></span>  <br/> |<span data-ttu-id="66043-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="66043-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="66043-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="66043-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="66043-153">N</span><span class="sxs-lookup"><span data-stu-id="66043-153">N</span></span>  <br/> |<span data-ttu-id="66043-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="66043-154">xsd:string</span></span>  <br/> |<span data-ttu-id="66043-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="66043-155">optional</span></span>  <br/> |<span data-ttu-id="66043-156">Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="66043-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="66043-157">Une ligne ne peut avoir qu’un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="66043-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="66043-158">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="66043-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="66043-159">T</span><span class="sxs-lookup"><span data-stu-id="66043-159">T</span></span>  <br/> |<span data-ttu-id="66043-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="66043-160">xsd:string</span></span>  <br/> |<span data-ttu-id="66043-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="66043-161">optional</span></span>  <br/> |<span data-ttu-id="66043-162">Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="66043-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="66043-163">L’attribut T est utilisé uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="66043-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="66043-164">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="66043-164">Values of the xsd:string type.</span></span>  <br/> |
   

