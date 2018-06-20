---
title: Row, élément (Section Controls) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Contient les cellules d’une poignée de contrôle définie pour une forme.
ms.openlocfilehash: cf8015b82f759ba2c166ff5179b2c4324c168e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789517"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="16781-103">Row, élément (Section Controls) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="16781-103">Row element (Controls Section) ('Visio XML')</span></span>

<span data-ttu-id="16781-104">Contient les cellules d’une poignée de contrôle définie pour une forme.</span><span class="sxs-lookup"><span data-stu-id="16781-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16781-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="16781-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16781-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="16781-106">**Element type**</span></span> <br/> |[<span data-ttu-id="16781-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="16781-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="16781-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="16781-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="16781-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="16781-109">**Schema file**</span></span> <br/> |<span data-ttu-id="16781-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="16781-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="16781-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="16781-111">**Document parts**</span></span> <br/> |<span data-ttu-id="16781-112">master # .xml, page # .xml</span><span class="sxs-lookup"><span data-stu-id="16781-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="16781-113">Définition</span><span class="sxs-lookup"><span data-stu-id="16781-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="16781-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="16781-114">Elements and attributes</span></span>

<span data-ttu-id="16781-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="16781-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="16781-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="16781-116">Parent elements</span></span>

|<span data-ttu-id="16781-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="16781-117">**Element**</span></span>|<span data-ttu-id="16781-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="16781-118">**Type**</span></span>|<span data-ttu-id="16781-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="16781-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16781-120">Section</span><span class="sxs-lookup"><span data-stu-id="16781-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16781-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="16781-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16781-122">Contient les cellules d’une poignée de contrôle définie pour une forme.</span><span class="sxs-lookup"><span data-stu-id="16781-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="16781-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="16781-123">Child elements</span></span>

|<span data-ttu-id="16781-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="16781-124">**Element**</span></span>|<span data-ttu-id="16781-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="16781-125">**Type**</span></span>|<span data-ttu-id="16781-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="16781-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16781-127">Cell</span><span class="sxs-lookup"><span data-stu-id="16781-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="16781-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="16781-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16781-129">Contient une propriété d’une poignée de contrôle définie pour une forme.</span><span class="sxs-lookup"><span data-stu-id="16781-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="16781-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="16781-130">Attributes</span></span>

|<span data-ttu-id="16781-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="16781-131">**Attribute**</span></span>|<span data-ttu-id="16781-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="16781-132">**Type**</span></span>|<span data-ttu-id="16781-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="16781-133">**Required**</span></span>|<span data-ttu-id="16781-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="16781-134">**Description**</span></span>|<span data-ttu-id="16781-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="16781-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="16781-136">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="16781-136">Del</span></span>  <br/> |<span data-ttu-id="16781-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="16781-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="16781-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="16781-138">optional</span></span>  <br/> |<span data-ttu-id="16781-139">Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="16781-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="16781-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="16781-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="16781-141">IX</span><span class="sxs-lookup"><span data-stu-id="16781-141">IX</span></span>  <br/> |<span data-ttu-id="16781-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="16781-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="16781-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="16781-143">optional</span></span>  <br/> |<span data-ttu-id="16781-144">Spécifie l’identificateur de base 1 pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="16781-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="16781-145">Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets.</span><span class="sxs-lookup"><span data-stu-id="16781-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="16781-146">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="16781-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="16781-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="16781-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="16781-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="16781-148">LocalName</span></span>  <br/> |<span data-ttu-id="16781-149">XSD : String</span><span class="sxs-lookup"><span data-stu-id="16781-149">xsd:string</span></span>  <br/> |<span data-ttu-id="16781-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="16781-150">optional</span></span>  <br/> |<span data-ttu-id="16781-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="16781-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="16781-152">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="16781-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="16781-153">N</span><span class="sxs-lookup"><span data-stu-id="16781-153">N</span></span>  <br/> |<span data-ttu-id="16781-154">XSD : String</span><span class="sxs-lookup"><span data-stu-id="16781-154">xsd:string</span></span>  <br/> |<span data-ttu-id="16781-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="16781-155">optional</span></span>  <br/> |<span data-ttu-id="16781-156">Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="16781-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="16781-157">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="16781-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="16781-158">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="16781-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="16781-159">T</span><span class="sxs-lookup"><span data-stu-id="16781-159">T</span></span>  <br/> |<span data-ttu-id="16781-160">XSD : String</span><span class="sxs-lookup"><span data-stu-id="16781-160">xsd:string</span></span>  <br/> |<span data-ttu-id="16781-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="16781-161">optional</span></span>  <br/> |<span data-ttu-id="16781-162">Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="16781-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="16781-163">L’attribut T est utilisée uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="16781-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="16781-164">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="16781-164">Values of the xsd:string type.</span></span>  <br/> |
   

