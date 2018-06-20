---
title: Élément RuleSet (RuleSets_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Représente un ensemble de règles de validation du diagramme.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789577"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="780ab-103">Élément RuleSet (RuleSets_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="780ab-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="780ab-104">Représente un ensemble de règles de validation du diagramme.</span><span class="sxs-lookup"><span data-stu-id="780ab-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="780ab-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="780ab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="780ab-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="780ab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="780ab-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="780ab-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="780ab-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="780ab-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="780ab-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="780ab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="780ab-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="780ab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="780ab-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="780ab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="780ab-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="780ab-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="780ab-113">Définition</span><span class="sxs-lookup"><span data-stu-id="780ab-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="780ab-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="780ab-114">Elements and attributes</span></span>

<span data-ttu-id="780ab-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="780ab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="780ab-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="780ab-116">Parent elements</span></span>

|<span data-ttu-id="780ab-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="780ab-117">**Element**</span></span>|<span data-ttu-id="780ab-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="780ab-118">**Type**</span></span>|<span data-ttu-id="780ab-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="780ab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="780ab-120">Groupes de règles</span><span class="sxs-lookup"><span data-stu-id="780ab-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="780ab-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="780ab-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="780ab-122">Inclut un élément **RuleSet** pour chaque règle de validation définie dans le document.</span><span class="sxs-lookup"><span data-stu-id="780ab-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="780ab-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="780ab-123">Child elements</span></span>

|<span data-ttu-id="780ab-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="780ab-124">**Element**</span></span>|<span data-ttu-id="780ab-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="780ab-125">**Type**</span></span>|<span data-ttu-id="780ab-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="780ab-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="780ab-127">Règle</span><span class="sxs-lookup"><span data-stu-id="780ab-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="780ab-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="780ab-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="780ab-129">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="780ab-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="780ab-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="780ab-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="780ab-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="780ab-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="780ab-132">Spécifie les propriétés d’ensembles de règles.</span><span class="sxs-lookup"><span data-stu-id="780ab-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="780ab-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="780ab-133">Attributes</span></span>

|<span data-ttu-id="780ab-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="780ab-134">**Attribute**</span></span>|<span data-ttu-id="780ab-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="780ab-135">**Type**</span></span>|<span data-ttu-id="780ab-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="780ab-136">**Required**</span></span>|<span data-ttu-id="780ab-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="780ab-137">**Description**</span></span>|<span data-ttu-id="780ab-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="780ab-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="780ab-139">Description</span><span class="sxs-lookup"><span data-stu-id="780ab-139">Description</span></span>  <br/> |<span data-ttu-id="780ab-140">XSD : String</span><span class="sxs-lookup"><span data-stu-id="780ab-140">xsd:string</span></span>  <br/> |<span data-ttu-id="780ab-141">facultatif</span><span class="sxs-lookup"><span data-stu-id="780ab-141">optional</span></span>  <br/> |<span data-ttu-id="780ab-142">Spécifie la description qui apparaît dans l’interface utilisateur pour l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="780ab-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="780ab-143">Il s'agit par défaut d'une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="780ab-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="780ab-144">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="780ab-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="780ab-145">Activé</span><span class="sxs-lookup"><span data-stu-id="780ab-145">Enabled</span></span>  <br/> |<span data-ttu-id="780ab-146">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="780ab-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="780ab-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="780ab-147">optional</span></span>  <br/> |<span data-ttu-id="780ab-148">Spécifie si les règles de l’ensemble de règles de validation spécifié sont vérifiés lors de la validation est déclenchée pour le document actif.</span><span class="sxs-lookup"><span data-stu-id="780ab-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="780ab-149">Valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="780ab-149">Default is True.</span></span>  <br/> |<span data-ttu-id="780ab-150">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="780ab-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="780ab-151">ID</span><span class="sxs-lookup"><span data-stu-id="780ab-151">ID</span></span>  <br/> |<span data-ttu-id="780ab-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="780ab-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="780ab-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="780ab-153">required</span></span>  <br/> |<span data-ttu-id="780ab-154">Spécifie l’identificateur unique de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="780ab-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="780ab-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="780ab-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="780ab-156">Nom</span><span class="sxs-lookup"><span data-stu-id="780ab-156">Name</span></span>  <br/> |<span data-ttu-id="780ab-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="780ab-157">xsd:string</span></span>  <br/> |<span data-ttu-id="780ab-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="780ab-158">optional</span></span>  <br/> |<span data-ttu-id="780ab-159">Spécifie le nom local de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="780ab-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="780ab-160">La valeur par défaut à la valeur de l’attribut NameU.</span><span class="sxs-lookup"><span data-stu-id="780ab-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="780ab-161">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="780ab-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="780ab-162">NameU</span><span class="sxs-lookup"><span data-stu-id="780ab-162">NameU</span></span>  <br/> |<span data-ttu-id="780ab-163">XSD : String</span><span class="sxs-lookup"><span data-stu-id="780ab-163">xsd:string</span></span>  <br/> |<span data-ttu-id="780ab-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="780ab-164">required</span></span>  <br/> |<span data-ttu-id="780ab-165">Spécifie le nom universel de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="780ab-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="780ab-166">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="780ab-166">Values of the xsd:string type.</span></span>  <br/> |
   

