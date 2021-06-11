---
title: Élément RuleSet (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Représente un ensemble de règles de validation de diagramme.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541637"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a><span data-ttu-id="4356d-103">Élément RuleSet (RuleSets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4356d-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4356d-104">Représente un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="4356d-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4356d-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="4356d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4356d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4356d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4356d-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="4356d-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4356d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4356d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4356d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4356d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4356d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4356d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4356d-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="4356d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4356d-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="4356d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4356d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="4356d-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4356d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4356d-114">Elements and attributes</span></span>

<span data-ttu-id="4356d-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="4356d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4356d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4356d-116">Parent elements</span></span>

|<span data-ttu-id="4356d-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4356d-117">**Element**</span></span>|<span data-ttu-id="4356d-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4356d-118">**Type**</span></span>|<span data-ttu-id="4356d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="4356d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4356d-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="4356d-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4356d-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="4356d-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4356d-122">Inclut **un élément RuleSet** pour chaque ensemble de règles de validation dans le document.</span><span class="sxs-lookup"><span data-stu-id="4356d-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4356d-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4356d-123">Child elements</span></span>

|<span data-ttu-id="4356d-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4356d-124">**Element**</span></span>|<span data-ttu-id="4356d-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4356d-125">**Type**</span></span>|<span data-ttu-id="4356d-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="4356d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4356d-127">Règle</span><span class="sxs-lookup"><span data-stu-id="4356d-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4356d-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="4356d-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4356d-129">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="4356d-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="4356d-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="4356d-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4356d-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="4356d-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4356d-132">Spécifie les propriétés des ensembles de règles.</span><span class="sxs-lookup"><span data-stu-id="4356d-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4356d-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="4356d-133">Attributes</span></span>

|<span data-ttu-id="4356d-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4356d-134">**Attribute**</span></span>|<span data-ttu-id="4356d-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="4356d-135">**Type**</span></span>|<span data-ttu-id="4356d-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4356d-136">**Required**</span></span>|<span data-ttu-id="4356d-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="4356d-137">**Description**</span></span>|<span data-ttu-id="4356d-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4356d-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4356d-139">Description</span><span class="sxs-lookup"><span data-stu-id="4356d-139">Description</span></span>  <br/> |<span data-ttu-id="4356d-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4356d-140">xsd:string</span></span>  <br/> |<span data-ttu-id="4356d-141">facultatif</span><span class="sxs-lookup"><span data-stu-id="4356d-141">optional</span></span>  <br/> |<span data-ttu-id="4356d-142">Spécifie la description qui apparaît dans l’interface utilisateur pour l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="4356d-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="4356d-143">Il s'agit par défaut d'une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4356d-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="4356d-144">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4356d-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4356d-145">Activé</span><span class="sxs-lookup"><span data-stu-id="4356d-145">Enabled</span></span>  <br/> |<span data-ttu-id="4356d-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4356d-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4356d-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="4356d-147">optional</span></span>  <br/> |<span data-ttu-id="4356d-148">Spécifie si les règles de l’ensemble de règles de validation spécifié sont vérifiées lorsque la validation est déclenchée pour le document actuel.</span><span class="sxs-lookup"><span data-stu-id="4356d-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="4356d-149">La valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="4356d-149">Default is True.</span></span>  <br/> |<span data-ttu-id="4356d-150">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4356d-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4356d-151">ID</span><span class="sxs-lookup"><span data-stu-id="4356d-151">ID</span></span>  <br/> |<span data-ttu-id="4356d-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4356d-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4356d-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4356d-153">required</span></span>  <br/> |<span data-ttu-id="4356d-154">Spécifie l’identificateur unique de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="4356d-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="4356d-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4356d-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4356d-156">Nom</span><span class="sxs-lookup"><span data-stu-id="4356d-156">Name</span></span>  <br/> |<span data-ttu-id="4356d-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4356d-157">xsd:string</span></span>  <br/> |<span data-ttu-id="4356d-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="4356d-158">optional</span></span>  <br/> |<span data-ttu-id="4356d-159">Spécifie le nom local de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="4356d-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="4356d-160">Valeur par défaut de l’attribut NameU.</span><span class="sxs-lookup"><span data-stu-id="4356d-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="4356d-161">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4356d-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4356d-162">NameU</span><span class="sxs-lookup"><span data-stu-id="4356d-162">NameU</span></span>  <br/> |<span data-ttu-id="4356d-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4356d-163">xsd:string</span></span>  <br/> |<span data-ttu-id="4356d-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4356d-164">required</span></span>  <br/> |<span data-ttu-id="4356d-165">Spécifie le nom universel de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="4356d-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="4356d-166">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4356d-166">Values of the xsd:string type.</span></span>  <br/> |
   

