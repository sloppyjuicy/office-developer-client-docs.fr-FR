---
title: RuleSet, élément (RuleSets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Représente un ensemble de règles de validation de diagramme.
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318913"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="d5cfb-103">RuleSet, élément (RuleSets_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d5cfb-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d5cfb-104">Représente un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5cfb-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="d5cfb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5cfb-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d5cfb-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="d5cfb-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d5cfb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d5cfb-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d5cfb-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d5cfb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d5cfb-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d5cfb-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="d5cfb-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5cfb-113">Définition</span><span class="sxs-lookup"><span data-stu-id="d5cfb-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d5cfb-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d5cfb-114">Elements and attributes</span></span>

<span data-ttu-id="d5cfb-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d5cfb-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d5cfb-116">Parent elements</span></span>

|<span data-ttu-id="d5cfb-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-117">**Element**</span></span>|<span data-ttu-id="d5cfb-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-118">**Type**</span></span>|<span data-ttu-id="d5cfb-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5cfb-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="d5cfb-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5cfb-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="d5cfb-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d5cfb-122">Inclut un élément **RuleSet** pour chaque ensemble de règles de validation dans le document.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d5cfb-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d5cfb-123">Child elements</span></span>

|<span data-ttu-id="d5cfb-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-124">**Element**</span></span>|<span data-ttu-id="d5cfb-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-125">**Type**</span></span>|<span data-ttu-id="d5cfb-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5cfb-127">Règle</span><span class="sxs-lookup"><span data-stu-id="d5cfb-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5cfb-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="d5cfb-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d5cfb-129">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="d5cfb-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="d5cfb-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5cfb-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="d5cfb-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d5cfb-132">Spécifie les propriétés d'ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d5cfb-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="d5cfb-133">Attributes</span></span>

|<span data-ttu-id="d5cfb-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-134">**Attribute**</span></span>|<span data-ttu-id="d5cfb-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-135">**Type**</span></span>|<span data-ttu-id="d5cfb-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-136">**Required**</span></span>|<span data-ttu-id="d5cfb-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-137">**Description**</span></span>|<span data-ttu-id="d5cfb-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d5cfb-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5cfb-139">Description</span><span class="sxs-lookup"><span data-stu-id="d5cfb-139">Description</span></span>  <br/> |<span data-ttu-id="d5cfb-140">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d5cfb-140">xsd:string</span></span>  <br/> |<span data-ttu-id="d5cfb-141">facultatif</span><span class="sxs-lookup"><span data-stu-id="d5cfb-141">optional</span></span>  <br/> |<span data-ttu-id="d5cfb-142">Spécifie la description qui apparaît dans l'interface utilisateur pour l'ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="d5cfb-143">Il s'agit par défaut d'une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="d5cfb-144">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d5cfb-145">Activé</span><span class="sxs-lookup"><span data-stu-id="d5cfb-145">Enabled</span></span>  <br/> |<span data-ttu-id="d5cfb-146">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="d5cfb-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d5cfb-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="d5cfb-147">optional</span></span>  <br/> |<span data-ttu-id="d5cfb-148">Indique si les règles de l'ensemble de règles de validation spécifié sont vérifiées lorsque la validation est déclenchée pour le document actif.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="d5cfb-149">La valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-149">Default is True.</span></span>  <br/> |<span data-ttu-id="d5cfb-150">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d5cfb-151">ID</span><span class="sxs-lookup"><span data-stu-id="d5cfb-151">ID</span></span>  <br/> |<span data-ttu-id="d5cfb-152">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5cfb-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5cfb-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d5cfb-153">required</span></span>  <br/> |<span data-ttu-id="d5cfb-154">Spécifie l'identificateur unique de l'ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="d5cfb-155">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5cfb-156">Nom</span><span class="sxs-lookup"><span data-stu-id="d5cfb-156">Name</span></span>  <br/> |<span data-ttu-id="d5cfb-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d5cfb-157">xsd:string</span></span>  <br/> |<span data-ttu-id="d5cfb-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="d5cfb-158">optional</span></span>  <br/> |<span data-ttu-id="d5cfb-159">Spécifie le nom local de l'ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="d5cfb-160">Par défaut, il s'agit de la valeur de l'attribut Name.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="d5cfb-161">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d5cfb-162">NameU</span><span class="sxs-lookup"><span data-stu-id="d5cfb-162">NameU</span></span>  <br/> |<span data-ttu-id="d5cfb-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d5cfb-163">xsd:string</span></span>  <br/> |<span data-ttu-id="d5cfb-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d5cfb-164">required</span></span>  <br/> |<span data-ttu-id="d5cfb-165">Spécifie le nom universel de l'ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="d5cfb-166">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d5cfb-166">Values of the xsd:string type.</span></span>  <br/> |
   

