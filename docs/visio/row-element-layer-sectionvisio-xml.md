---
title: Row, élément (Section Layer) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contient des éléments qui définissent une couche unique et à ses propriétés pour une page.
ms.openlocfilehash: 2aff1666f5a2cb87ed10b76e0facdb19a4278c89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396840"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="288bb-103">Row, élément (Section Layer) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="288bb-103">Row element (Layer Section) ('Visio XML')</span></span>

<span data-ttu-id="288bb-104">Contient des éléments qui définissent une couche unique et à ses propriétés pour une page.</span><span class="sxs-lookup"><span data-stu-id="288bb-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="288bb-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="288bb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="288bb-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="288bb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="288bb-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="288bb-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="288bb-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="288bb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="288bb-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="288bb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="288bb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="288bb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="288bb-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="288bb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="288bb-112">Masters.XML, pages.xml</span><span class="sxs-lookup"><span data-stu-id="288bb-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="288bb-113">Définition</span><span class="sxs-lookup"><span data-stu-id="288bb-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="288bb-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="288bb-114">Elements and attributes</span></span>

<span data-ttu-id="288bb-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="288bb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="288bb-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="288bb-116">Parent elements</span></span>

|<span data-ttu-id="288bb-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="288bb-117">**Element**</span></span>|<span data-ttu-id="288bb-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="288bb-118">**Type**</span></span>|<span data-ttu-id="288bb-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="288bb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="288bb-120">Section</span><span class="sxs-lookup"><span data-stu-id="288bb-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="288bb-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="288bb-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="288bb-122">Contient des éléments qui définissent une couche unique et à ses propriétés pour une page.</span><span class="sxs-lookup"><span data-stu-id="288bb-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="288bb-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="288bb-123">Child elements</span></span>

|<span data-ttu-id="288bb-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="288bb-124">**Element**</span></span>|<span data-ttu-id="288bb-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="288bb-125">**Type**</span></span>|<span data-ttu-id="288bb-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="288bb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="288bb-127">Cell</span><span class="sxs-lookup"><span data-stu-id="288bb-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="288bb-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="288bb-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="288bb-129">Spécifie une propriété d’un calque ou ses propriétés pour une page.</span><span class="sxs-lookup"><span data-stu-id="288bb-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="288bb-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="288bb-130">Attributes</span></span>

|<span data-ttu-id="288bb-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="288bb-131">**Attribute**</span></span>|<span data-ttu-id="288bb-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="288bb-132">**Type**</span></span>|<span data-ttu-id="288bb-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="288bb-133">**Required**</span></span>|<span data-ttu-id="288bb-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="288bb-134">**Description**</span></span>|<span data-ttu-id="288bb-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="288bb-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="288bb-136">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="288bb-136">Del</span></span>  <br/> |<span data-ttu-id="288bb-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="288bb-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="288bb-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="288bb-138">optional</span></span>  <br/> |<span data-ttu-id="288bb-139">Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="288bb-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="288bb-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="288bb-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="288bb-141">IX</span><span class="sxs-lookup"><span data-stu-id="288bb-141">IX</span></span>  <br/> |<span data-ttu-id="288bb-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="288bb-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="288bb-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="288bb-143">optional</span></span>  <br/> |<span data-ttu-id="288bb-144">Spécifie l’identificateur de base 1 pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="288bb-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="288bb-145">Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets.</span><span class="sxs-lookup"><span data-stu-id="288bb-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="288bb-146">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="288bb-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="288bb-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="288bb-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="288bb-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="288bb-148">LocalName</span></span>  <br/> |<span data-ttu-id="288bb-149">XSD : String</span><span class="sxs-lookup"><span data-stu-id="288bb-149">xsd:string</span></span>  <br/> |<span data-ttu-id="288bb-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="288bb-150">optional</span></span>  <br/> |<span data-ttu-id="288bb-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="288bb-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="288bb-152">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="288bb-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="288bb-153">N</span><span class="sxs-lookup"><span data-stu-id="288bb-153">N</span></span>  <br/> |<span data-ttu-id="288bb-154">XSD : String</span><span class="sxs-lookup"><span data-stu-id="288bb-154">xsd:string</span></span>  <br/> |<span data-ttu-id="288bb-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="288bb-155">optional</span></span>  <br/> |<span data-ttu-id="288bb-156">Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="288bb-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="288bb-157">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="288bb-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="288bb-158">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="288bb-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="288bb-159">T</span><span class="sxs-lookup"><span data-stu-id="288bb-159">T</span></span>  <br/> |<span data-ttu-id="288bb-160">XSD : String</span><span class="sxs-lookup"><span data-stu-id="288bb-160">xsd:string</span></span>  <br/> |<span data-ttu-id="288bb-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="288bb-161">optional</span></span>  <br/> |<span data-ttu-id="288bb-162">Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="288bb-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="288bb-163">L’attribut T est utilisée uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="288bb-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="288bb-164">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="288bb-164">Values of the xsd:string type.</span></span>  <br/> |
   

