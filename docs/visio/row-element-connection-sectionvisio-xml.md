---
title: Row, élément (Section Connection) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Contient les coordonnées x ou y, direction horizontale et verticale et le type d’un point de connexion unique d’une forme.
ms.openlocfilehash: 9f8f5f0735f7eeff2f1b2ec4562b79e6550d1716
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389917"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="40493-103">Row, élément (Section Connection) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="40493-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="40493-104">Contient les coordonnées x ou y, direction horizontale et verticale et le type d’un point de connexion unique d’une forme.</span><span class="sxs-lookup"><span data-stu-id="40493-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40493-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="40493-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40493-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="40493-106">**Element type**</span></span> <br/> |[<span data-ttu-id="40493-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="40493-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="40493-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="40493-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="40493-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="40493-109">**Schema file**</span></span> <br/> |<span data-ttu-id="40493-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="40493-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="40493-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="40493-111">**Document parts**</span></span> <br/> |<span data-ttu-id="40493-112">master # .xml, page # .xml</span><span class="sxs-lookup"><span data-stu-id="40493-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40493-113">Définition</span><span class="sxs-lookup"><span data-stu-id="40493-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="40493-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="40493-114">Elements and attributes</span></span>

<span data-ttu-id="40493-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="40493-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="40493-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="40493-116">Parent elements</span></span>

|<span data-ttu-id="40493-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="40493-117">**Element**</span></span>|<span data-ttu-id="40493-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="40493-118">**Type**</span></span>|<span data-ttu-id="40493-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="40493-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40493-120">Section</span><span class="sxs-lookup"><span data-stu-id="40493-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40493-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="40493-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40493-122">Contient les coordonnées x ou y, direction horizontale et verticale et le type d’un point de connexion unique d’une forme.</span><span class="sxs-lookup"><span data-stu-id="40493-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="40493-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="40493-123">Child elements</span></span>

|<span data-ttu-id="40493-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="40493-124">**Element**</span></span>|<span data-ttu-id="40493-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="40493-125">**Type**</span></span>|<span data-ttu-id="40493-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="40493-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40493-127">Cell</span><span class="sxs-lookup"><span data-stu-id="40493-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="40493-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="40493-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40493-129">Spécifie une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="40493-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="40493-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="40493-130">Attributes</span></span>

|<span data-ttu-id="40493-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="40493-131">**Attribute**</span></span>|<span data-ttu-id="40493-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="40493-132">**Type**</span></span>|<span data-ttu-id="40493-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="40493-133">**Required**</span></span>|<span data-ttu-id="40493-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="40493-134">**Description**</span></span>|<span data-ttu-id="40493-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="40493-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="40493-136">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="40493-136">Del</span></span>  <br/> |<span data-ttu-id="40493-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="40493-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="40493-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="40493-138">optional</span></span>  <br/> |<span data-ttu-id="40493-139">Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="40493-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="40493-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="40493-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="40493-141">IX</span><span class="sxs-lookup"><span data-stu-id="40493-141">IX</span></span>  <br/> |<span data-ttu-id="40493-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40493-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40493-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="40493-143">optional</span></span>  <br/> |<span data-ttu-id="40493-144">Spécifie l’identificateur de base 1 pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="40493-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="40493-145">Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets.</span><span class="sxs-lookup"><span data-stu-id="40493-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="40493-146">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="40493-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="40493-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="40493-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="40493-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="40493-148">LocalName</span></span>  <br/> |<span data-ttu-id="40493-149">XSD : String</span><span class="sxs-lookup"><span data-stu-id="40493-149">xsd:string</span></span>  <br/> |<span data-ttu-id="40493-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="40493-150">optional</span></span>  <br/> |<span data-ttu-id="40493-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="40493-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="40493-152">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="40493-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="40493-153">N</span><span class="sxs-lookup"><span data-stu-id="40493-153">N</span></span>  <br/> |<span data-ttu-id="40493-154">XSD : String</span><span class="sxs-lookup"><span data-stu-id="40493-154">xsd:string</span></span>  <br/> |<span data-ttu-id="40493-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="40493-155">optional</span></span>  <br/> |<span data-ttu-id="40493-156">Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="40493-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="40493-157">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="40493-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="40493-158">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="40493-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="40493-159">T</span><span class="sxs-lookup"><span data-stu-id="40493-159">T</span></span>  <br/> |<span data-ttu-id="40493-160">XSD : String</span><span class="sxs-lookup"><span data-stu-id="40493-160">xsd:string</span></span>  <br/> |<span data-ttu-id="40493-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="40493-161">optional</span></span>  <br/> |<span data-ttu-id="40493-162">Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="40493-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="40493-163">L’attribut T est utilisée uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="40493-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="40493-164">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="40493-164">Values of the xsd:string type.</span></span>  <br/> |
   

