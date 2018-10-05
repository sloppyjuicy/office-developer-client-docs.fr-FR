---
title: Row, élément (Section liens hypertexte) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f87cd7a4-b9de-5fb1-20ec-90759c966bd9
description: Contient des éléments pour créer des liens entre une forme ou page et une autre page de dessin, un autre fichier ou un site Web de dessin.
ms.openlocfilehash: 16935e463e76e0f0ee72b3fa40964551cf125cdd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400032"
---
# <a name="row-element-hyperlink-section-visio-xml"></a><span data-ttu-id="f550f-103">Row, élément (Section liens hypertexte) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="f550f-103">Row element (Hyperlink Section) ('Visio XML')</span></span>

<span data-ttu-id="f550f-104">Contient des éléments pour créer des liens entre une forme ou page et une autre page de dessin, un autre fichier ou un site Web de dessin.</span><span class="sxs-lookup"><span data-stu-id="f550f-104">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f550f-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="f550f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f550f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="f550f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f550f-107">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="f550f-107">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f550f-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="f550f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f550f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f550f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f550f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f550f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f550f-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="f550f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f550f-112">master # .xml, page # .xml</span><span class="sxs-lookup"><span data-stu-id="f550f-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f550f-113">Définition</span><span class="sxs-lookup"><span data-stu-id="f550f-113">Definition</span></span>

```XML
< xs:element name="Row" type="HyperlinkRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f550f-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f550f-114">Elements and attributes</span></span>

<span data-ttu-id="f550f-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="f550f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f550f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f550f-116">Parent elements</span></span>

|<span data-ttu-id="f550f-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f550f-117">**Element**</span></span>|<span data-ttu-id="f550f-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="f550f-118">**Type**</span></span>|<span data-ttu-id="f550f-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="f550f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f550f-120">Section</span><span class="sxs-lookup"><span data-stu-id="f550f-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f550f-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="f550f-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f550f-122">Contient des éléments pour créer des liens entre une forme ou page et une autre page de dessin, un autre fichier ou un site Web de dessin.</span><span class="sxs-lookup"><span data-stu-id="f550f-122">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f550f-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f550f-123">Child elements</span></span>

|<span data-ttu-id="f550f-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f550f-124">**Element**</span></span>|<span data-ttu-id="f550f-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="f550f-125">**Type**</span></span>|<span data-ttu-id="f550f-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="f550f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f550f-127">Cell</span><span class="sxs-lookup"><span data-stu-id="f550f-127">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="f550f-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f550f-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f550f-129">Contient les informations d’un lien hypertexte associé à une forme</span><span class="sxs-lookup"><span data-stu-id="f550f-129">Contains the information for a single hyperlink associated with a shape</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f550f-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="f550f-130">Attributes</span></span>

|<span data-ttu-id="f550f-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f550f-131">**Attribute**</span></span>|<span data-ttu-id="f550f-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="f550f-132">**Type**</span></span>|<span data-ttu-id="f550f-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f550f-133">**Required**</span></span>|<span data-ttu-id="f550f-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="f550f-134">**Description**</span></span>|<span data-ttu-id="f550f-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f550f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f550f-136">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="f550f-136">Del</span></span>  <br/> |<span data-ttu-id="f550f-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="f550f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f550f-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="f550f-138">optional</span></span>  <br/> |<span data-ttu-id="f550f-139">Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="f550f-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="f550f-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="f550f-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f550f-141">IX</span><span class="sxs-lookup"><span data-stu-id="f550f-141">IX</span></span>  <br/> |<span data-ttu-id="f550f-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f550f-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f550f-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="f550f-143">optional</span></span>  <br/> |<span data-ttu-id="f550f-144">Spécifie l’identificateur de base 1 pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="f550f-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="f550f-145">Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets.</span><span class="sxs-lookup"><span data-stu-id="f550f-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="f550f-146">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="f550f-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f550f-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f550f-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f550f-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="f550f-148">LocalName</span></span>  <br/> |<span data-ttu-id="f550f-149">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f550f-149">xsd:string</span></span>  <br/> |<span data-ttu-id="f550f-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="f550f-150">optional</span></span>  <br/> |<span data-ttu-id="f550f-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="f550f-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="f550f-152">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f550f-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f550f-153">N</span><span class="sxs-lookup"><span data-stu-id="f550f-153">N</span></span>  <br/> |<span data-ttu-id="f550f-154">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f550f-154">xsd:string</span></span>  <br/> |<span data-ttu-id="f550f-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="f550f-155">optional</span></span>  <br/> |<span data-ttu-id="f550f-156">Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="f550f-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="f550f-157">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="f550f-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f550f-158">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f550f-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f550f-159">T</span><span class="sxs-lookup"><span data-stu-id="f550f-159">T</span></span>  <br/> |<span data-ttu-id="f550f-160">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f550f-160">xsd:string</span></span>  <br/> |<span data-ttu-id="f550f-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="f550f-161">optional</span></span>  <br/> |<span data-ttu-id="f550f-162">Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="f550f-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="f550f-163">L’attribut T est utilisée uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="f550f-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="f550f-164">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="f550f-164">Values of the xsd:string type.</span></span>  <br/> |
   

