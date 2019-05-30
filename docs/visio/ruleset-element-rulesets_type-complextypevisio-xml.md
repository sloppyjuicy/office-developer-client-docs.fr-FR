---
title: Élément RuleSet (RuleSets_Type, complexType) (XML Visio)
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
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="b9b59-103">Élément RuleSet (RuleSets_Type, complexType) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="b9b59-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b9b59-104">Représente un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="b9b59-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9b59-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="b9b59-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9b59-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="b9b59-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b9b59-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="b9b59-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b9b59-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b9b59-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b9b59-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b9b59-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b9b59-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b9b59-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b9b59-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="b9b59-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b9b59-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="b9b59-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b9b59-113">Définition</span><span class="sxs-lookup"><span data-stu-id="b9b59-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b9b59-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b9b59-114">Elements and attributes</span></span>

<span data-ttu-id="b9b59-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="b9b59-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b9b59-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b9b59-116">Parent elements</span></span>

|<span data-ttu-id="b9b59-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b9b59-117">**Element**</span></span>|<span data-ttu-id="b9b59-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="b9b59-118">**Type**</span></span>|<span data-ttu-id="b9b59-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9b59-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b9b59-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="b9b59-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9b59-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="b9b59-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b9b59-122">Inclut un élément **RuleSet** pour chaque ensemble de règles de validation dans le document.</span><span class="sxs-lookup"><span data-stu-id="b9b59-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b9b59-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b9b59-123">Child elements</span></span>

|<span data-ttu-id="b9b59-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b9b59-124">**Element**</span></span>|<span data-ttu-id="b9b59-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="b9b59-125">**Type**</span></span>|<span data-ttu-id="b9b59-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9b59-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b9b59-127">Règle</span><span class="sxs-lookup"><span data-stu-id="b9b59-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9b59-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="b9b59-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b9b59-129">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="b9b59-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="b9b59-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="b9b59-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9b59-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="b9b59-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b9b59-132">Spécifie les propriétés d’ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="b9b59-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b9b59-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="b9b59-133">Attributes</span></span>

|<span data-ttu-id="b9b59-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b9b59-134">**Attribute**</span></span>|<span data-ttu-id="b9b59-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="b9b59-135">**Type**</span></span>|<span data-ttu-id="b9b59-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b9b59-136">**Required**</span></span>|<span data-ttu-id="b9b59-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9b59-137">**Description**</span></span>|<span data-ttu-id="b9b59-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b9b59-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b9b59-139">Description</span><span class="sxs-lookup"><span data-stu-id="b9b59-139">Description</span></span>  <br/> |<span data-ttu-id="b9b59-140">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b9b59-140">xsd:string</span></span>  <br/> |<span data-ttu-id="b9b59-141">facultatif</span><span class="sxs-lookup"><span data-stu-id="b9b59-141">optional</span></span>  <br/> |<span data-ttu-id="b9b59-142">Spécifie la description qui apparaît dans l’interface utilisateur pour l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="b9b59-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="b9b59-143">Il s'agit par défaut d'une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="b9b59-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="b9b59-144">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b9b59-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b9b59-145">Activé</span><span class="sxs-lookup"><span data-stu-id="b9b59-145">Enabled</span></span>  <br/> |<span data-ttu-id="b9b59-146">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="b9b59-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b9b59-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="b9b59-147">optional</span></span>  <br/> |<span data-ttu-id="b9b59-148">Indique si les règles de l’ensemble de règles de validation spécifié sont vérifiées lorsque la validation est déclenchée pour le document actif.</span><span class="sxs-lookup"><span data-stu-id="b9b59-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="b9b59-149">La valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="b9b59-149">Default is True.</span></span>  <br/> |<span data-ttu-id="b9b59-150">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b9b59-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b9b59-151">ID</span><span class="sxs-lookup"><span data-stu-id="b9b59-151">ID</span></span>  <br/> |<span data-ttu-id="b9b59-152">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b9b59-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b9b59-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b9b59-153">required</span></span>  <br/> |<span data-ttu-id="b9b59-154">Spécifie l’identificateur unique de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="b9b59-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="b9b59-155">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b9b59-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b9b59-156">Nom</span><span class="sxs-lookup"><span data-stu-id="b9b59-156">Name</span></span>  <br/> |<span data-ttu-id="b9b59-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b9b59-157">xsd:string</span></span>  <br/> |<span data-ttu-id="b9b59-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="b9b59-158">optional</span></span>  <br/> |<span data-ttu-id="b9b59-159">Spécifie le nom local de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="b9b59-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="b9b59-160">Par défaut, il s’agit de la valeur de l’attribut Name.</span><span class="sxs-lookup"><span data-stu-id="b9b59-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="b9b59-161">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b9b59-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b9b59-162">NameU</span><span class="sxs-lookup"><span data-stu-id="b9b59-162">NameU</span></span>  <br/> |<span data-ttu-id="b9b59-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b9b59-163">xsd:string</span></span>  <br/> |<span data-ttu-id="b9b59-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b9b59-164">required</span></span>  <br/> |<span data-ttu-id="b9b59-165">Spécifie le nom universel de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="b9b59-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="b9b59-166">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b9b59-166">Values of the xsd:string type.</span></span>  <br/> |
   

