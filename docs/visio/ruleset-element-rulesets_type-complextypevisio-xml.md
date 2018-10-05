---
title: Élément RuleSet (RuleSets_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Représente un ensemble de règles de validation du diagramme.
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387390"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="16616-103">Élément RuleSet (RuleSets_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="16616-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="16616-104">Représente un ensemble de règles de validation du diagramme.</span><span class="sxs-lookup"><span data-stu-id="16616-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16616-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="16616-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16616-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="16616-106">**Element type**</span></span> <br/> |[<span data-ttu-id="16616-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="16616-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="16616-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="16616-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="16616-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="16616-109">**Schema file**</span></span> <br/> |<span data-ttu-id="16616-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="16616-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="16616-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="16616-111">**Document parts**</span></span> <br/> |<span data-ttu-id="16616-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="16616-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="16616-113">Définition</span><span class="sxs-lookup"><span data-stu-id="16616-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="16616-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="16616-114">Elements and attributes</span></span>

<span data-ttu-id="16616-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="16616-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="16616-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="16616-116">Parent elements</span></span>

|<span data-ttu-id="16616-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="16616-117">**Element**</span></span>|<span data-ttu-id="16616-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="16616-118">**Type**</span></span>|<span data-ttu-id="16616-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="16616-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16616-120">Groupes de règles</span><span class="sxs-lookup"><span data-stu-id="16616-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16616-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="16616-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16616-122">Inclut un élément **RuleSet** pour chaque règle de validation définie dans le document.</span><span class="sxs-lookup"><span data-stu-id="16616-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="16616-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="16616-123">Child elements</span></span>

|<span data-ttu-id="16616-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="16616-124">**Element**</span></span>|<span data-ttu-id="16616-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="16616-125">**Type**</span></span>|<span data-ttu-id="16616-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="16616-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16616-127">Règle</span><span class="sxs-lookup"><span data-stu-id="16616-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16616-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="16616-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16616-129">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="16616-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="16616-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="16616-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16616-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="16616-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16616-132">Spécifie les propriétés d’ensembles de règles.</span><span class="sxs-lookup"><span data-stu-id="16616-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="16616-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="16616-133">Attributes</span></span>

|<span data-ttu-id="16616-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="16616-134">**Attribute**</span></span>|<span data-ttu-id="16616-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="16616-135">**Type**</span></span>|<span data-ttu-id="16616-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="16616-136">**Required**</span></span>|<span data-ttu-id="16616-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="16616-137">**Description**</span></span>|<span data-ttu-id="16616-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="16616-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="16616-139">Description</span><span class="sxs-lookup"><span data-stu-id="16616-139">Description</span></span>  <br/> |<span data-ttu-id="16616-140">XSD : String</span><span class="sxs-lookup"><span data-stu-id="16616-140">xsd:string</span></span>  <br/> |<span data-ttu-id="16616-141">facultatif</span><span class="sxs-lookup"><span data-stu-id="16616-141">optional</span></span>  <br/> |<span data-ttu-id="16616-142">Spécifie la description qui apparaît dans l’interface utilisateur pour l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="16616-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="16616-143">Il s'agit par défaut d'une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="16616-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="16616-144">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="16616-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="16616-145">Activé</span><span class="sxs-lookup"><span data-stu-id="16616-145">Enabled</span></span>  <br/> |<span data-ttu-id="16616-146">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="16616-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="16616-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="16616-147">optional</span></span>  <br/> |<span data-ttu-id="16616-148">Spécifie si les règles de l’ensemble de règles de validation spécifié sont vérifiés lors de la validation est déclenchée pour le document actif.</span><span class="sxs-lookup"><span data-stu-id="16616-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="16616-149">Valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="16616-149">Default is True.</span></span>  <br/> |<span data-ttu-id="16616-150">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="16616-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="16616-151">ID</span><span class="sxs-lookup"><span data-stu-id="16616-151">ID</span></span>  <br/> |<span data-ttu-id="16616-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="16616-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="16616-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="16616-153">required</span></span>  <br/> |<span data-ttu-id="16616-154">Spécifie l’identificateur unique de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="16616-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="16616-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="16616-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="16616-156">Nom</span><span class="sxs-lookup"><span data-stu-id="16616-156">Name</span></span>  <br/> |<span data-ttu-id="16616-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="16616-157">xsd:string</span></span>  <br/> |<span data-ttu-id="16616-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="16616-158">optional</span></span>  <br/> |<span data-ttu-id="16616-159">Spécifie le nom local de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="16616-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="16616-160">La valeur par défaut à la valeur de l’attribut NameU.</span><span class="sxs-lookup"><span data-stu-id="16616-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="16616-161">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="16616-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="16616-162">NameU</span><span class="sxs-lookup"><span data-stu-id="16616-162">NameU</span></span>  <br/> |<span data-ttu-id="16616-163">XSD : String</span><span class="sxs-lookup"><span data-stu-id="16616-163">xsd:string</span></span>  <br/> |<span data-ttu-id="16616-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="16616-164">required</span></span>  <br/> |<span data-ttu-id="16616-165">Spécifie le nom universel de l’ensemble de règles de validation.</span><span class="sxs-lookup"><span data-stu-id="16616-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="16616-166">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="16616-166">Values of the xsd:string type.</span></span>  <br/> |
   

