---
title: Row, élément (Section Shape Data) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Spécifie une entrée de données de forme pour associer les données à une forme.
ms.openlocfilehash: 19dc4fe4759e7546f56160e41100d73721f9f6e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789540"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="232c7-103">Row, élément (Section Shape Data) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="232c7-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="232c7-104">Spécifie une entrée de données de forme pour associer les données à une forme.</span><span class="sxs-lookup"><span data-stu-id="232c7-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="232c7-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="232c7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="232c7-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="232c7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="232c7-107">Forme type_de_données</span><span class="sxs-lookup"><span data-stu-id="232c7-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="232c7-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="232c7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="232c7-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="232c7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="232c7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="232c7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="232c7-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="232c7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="232c7-112">master # .xml, page # .xml</span><span class="sxs-lookup"><span data-stu-id="232c7-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="232c7-113">Définition</span><span class="sxs-lookup"><span data-stu-id="232c7-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="232c7-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="232c7-114">Elements and attributes</span></span>

<span data-ttu-id="232c7-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="232c7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="232c7-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="232c7-116">Parent elements</span></span>

|<span data-ttu-id="232c7-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="232c7-117">**Element**</span></span>|<span data-ttu-id="232c7-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="232c7-118">**Type**</span></span>|<span data-ttu-id="232c7-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="232c7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="232c7-120">Section</span><span class="sxs-lookup"><span data-stu-id="232c7-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="232c7-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="232c7-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="232c7-122">Spécifie une entrée de données de forme pour associer les données à une forme.</span><span class="sxs-lookup"><span data-stu-id="232c7-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="232c7-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="232c7-123">Child elements</span></span>

|<span data-ttu-id="232c7-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="232c7-124">**Element**</span></span>|<span data-ttu-id="232c7-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="232c7-125">**Type**</span></span>|<span data-ttu-id="232c7-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="232c7-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="232c7-127">Cell</span><span class="sxs-lookup"><span data-stu-id="232c7-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="232c7-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="232c7-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="232c7-129">Spécifie une propriété de données de forme.</span><span class="sxs-lookup"><span data-stu-id="232c7-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="232c7-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="232c7-130">Attributes</span></span>

|<span data-ttu-id="232c7-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="232c7-131">**Attribute**</span></span>|<span data-ttu-id="232c7-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="232c7-132">**Type**</span></span>|<span data-ttu-id="232c7-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="232c7-133">**Required**</span></span>|<span data-ttu-id="232c7-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="232c7-134">**Description**</span></span>|<span data-ttu-id="232c7-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="232c7-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="232c7-136">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="232c7-136">Del</span></span>  <br/> |<span data-ttu-id="232c7-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="232c7-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="232c7-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="232c7-138">optional</span></span>  <br/> |<span data-ttu-id="232c7-139">Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="232c7-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="232c7-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="232c7-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="232c7-141">IX</span><span class="sxs-lookup"><span data-stu-id="232c7-141">IX</span></span>  <br/> |<span data-ttu-id="232c7-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="232c7-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="232c7-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="232c7-143">optional</span></span>  <br/> |<span data-ttu-id="232c7-144">Spécifie l’identificateur de base 1 pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="232c7-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="232c7-145">Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets.</span><span class="sxs-lookup"><span data-stu-id="232c7-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="232c7-146">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="232c7-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="232c7-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="232c7-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="232c7-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="232c7-148">LocalName</span></span>  <br/> |<span data-ttu-id="232c7-149">XSD : String</span><span class="sxs-lookup"><span data-stu-id="232c7-149">xsd:string</span></span>  <br/> |<span data-ttu-id="232c7-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="232c7-150">optional</span></span>  <br/> |<span data-ttu-id="232c7-151">Spécifie le nom unique dépendant de la langue de la ligne.</span><span class="sxs-lookup"><span data-stu-id="232c7-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="232c7-152">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="232c7-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="232c7-153">N</span><span class="sxs-lookup"><span data-stu-id="232c7-153">N</span></span>  <br/> |<span data-ttu-id="232c7-154">XSD : String</span><span class="sxs-lookup"><span data-stu-id="232c7-154">xsd:string</span></span>  <br/> |<span data-ttu-id="232c7-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="232c7-155">optional</span></span>  <br/> |<span data-ttu-id="232c7-156">Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag.</span><span class="sxs-lookup"><span data-stu-id="232c7-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="232c7-157">Une ligne peut être un des attributs IX ou N.</span><span class="sxs-lookup"><span data-stu-id="232c7-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="232c7-158">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="232c7-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="232c7-159">T</span><span class="sxs-lookup"><span data-stu-id="232c7-159">T</span></span>  <br/> |<span data-ttu-id="232c7-160">XSD : String</span><span class="sxs-lookup"><span data-stu-id="232c7-160">xsd:string</span></span>  <br/> |<span data-ttu-id="232c7-161">facultatif</span><span class="sxs-lookup"><span data-stu-id="232c7-161">optional</span></span>  <br/> |<span data-ttu-id="232c7-162">Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie.</span><span class="sxs-lookup"><span data-stu-id="232c7-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="232c7-163">L’attribut T est utilisée uniquement pour la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="232c7-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="232c7-164">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="232c7-164">Values of the xsd:string type.</span></span>  <br/> |
   

