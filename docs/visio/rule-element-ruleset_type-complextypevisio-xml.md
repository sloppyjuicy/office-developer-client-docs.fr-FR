---
title: Rule, élément (RuleSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395909"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="9fcf7-103">Rule, élément (RuleSet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9fcf7-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9fcf7-104">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fcf7-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="9fcf7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fcf7-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9fcf7-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="9fcf7-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9fcf7-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9fcf7-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9fcf7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9fcf7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9fcf7-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9fcf7-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="9fcf7-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fcf7-113">Définition</span><span class="sxs-lookup"><span data-stu-id="9fcf7-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fcf7-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9fcf7-114">Elements and attributes</span></span>

<span data-ttu-id="9fcf7-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9fcf7-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9fcf7-116">Parent elements</span></span>

|<span data-ttu-id="9fcf7-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-117">**Element**</span></span>|<span data-ttu-id="9fcf7-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-118">**Type**</span></span>|<span data-ttu-id="9fcf7-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fcf7-120">Ensemble de règles</span><span class="sxs-lookup"><span data-stu-id="9fcf7-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fcf7-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="9fcf7-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fcf7-122">Représente un ensemble de règles de validation du diagramme.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9fcf7-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9fcf7-123">Child elements</span></span>

|<span data-ttu-id="9fcf7-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-124">**Element**</span></span>|<span data-ttu-id="9fcf7-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-125">**Type**</span></span>|<span data-ttu-id="9fcf7-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fcf7-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="9fcf7-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fcf7-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="9fcf7-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fcf7-129">Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="9fcf7-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="9fcf7-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fcf7-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="9fcf7-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fcf7-132">Spécifie l’expression logique qui détermine si l’objet cible correspond à la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9fcf7-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="9fcf7-133">Attributes</span></span>

|<span data-ttu-id="9fcf7-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-134">**Attribute**</span></span>|<span data-ttu-id="9fcf7-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-135">**Type**</span></span>|<span data-ttu-id="9fcf7-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-136">**Required**</span></span>|<span data-ttu-id="9fcf7-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-137">**Description**</span></span>|<span data-ttu-id="9fcf7-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9fcf7-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9fcf7-139">Category</span><span class="sxs-lookup"><span data-stu-id="9fcf7-139">Category</span></span>  <br/> |<span data-ttu-id="9fcf7-140">XSD : String</span><span class="sxs-lookup"><span data-stu-id="9fcf7-140">xsd:string</span></span>  <br/> |<span data-ttu-id="9fcf7-141">facultatif</span><span class="sxs-lookup"><span data-stu-id="9fcf7-141">optional</span></span>  <br/> |<span data-ttu-id="9fcf7-142">Spécifie le texte affiché dans la colonne **catégorie** de la fenêtre problèmes.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="9fcf7-143">Il s'agit par défaut d'une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="9fcf7-144">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9fcf7-145">Description</span><span class="sxs-lookup"><span data-stu-id="9fcf7-145">Description</span></span>  <br/> |<span data-ttu-id="9fcf7-146">XSD : String</span><span class="sxs-lookup"><span data-stu-id="9fcf7-146">xsd:string</span></span>  <br/> |<span data-ttu-id="9fcf7-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="9fcf7-147">optional</span></span>  <br/> |<span data-ttu-id="9fcf7-148">Spécifie la description de la règle de validation qui s’affiche dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="9fcf7-149">Valeur par défaut est « Inconnue ».</span><span class="sxs-lookup"><span data-stu-id="9fcf7-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="9fcf7-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9fcf7-151">ID</span><span class="sxs-lookup"><span data-stu-id="9fcf7-151">ID</span></span>  <br/> |<span data-ttu-id="9fcf7-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9fcf7-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9fcf7-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9fcf7-153">required</span></span>  <br/> |<span data-ttu-id="9fcf7-154">Spécifie l’identificateur unique de la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="9fcf7-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9fcf7-156">Ignoré</span><span class="sxs-lookup"><span data-stu-id="9fcf7-156">Ignored</span></span>  <br/> |<span data-ttu-id="9fcf7-157">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="9fcf7-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9fcf7-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="9fcf7-158">optional</span></span>  <br/> |<span data-ttu-id="9fcf7-159">Spécifie si la règle de validation est actuellement ignorée.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="9fcf7-160">Valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-160">Default is False.</span></span>  <br/> |<span data-ttu-id="9fcf7-161">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9fcf7-162">NameU</span><span class="sxs-lookup"><span data-stu-id="9fcf7-162">NameU</span></span>  <br/> |<span data-ttu-id="9fcf7-163">XSD : String</span><span class="sxs-lookup"><span data-stu-id="9fcf7-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9fcf7-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9fcf7-164">required</span></span>  <br/> |<span data-ttu-id="9fcf7-165">Spécifie le nom universel de la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="9fcf7-166">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9fcf7-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="9fcf7-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="9fcf7-168">XSD : int</span><span class="sxs-lookup"><span data-stu-id="9fcf7-168">xsd:int</span></span>  <br/> |<span data-ttu-id="9fcf7-169">facultatif</span><span class="sxs-lookup"><span data-stu-id="9fcf7-169">optional</span></span>  <br/> |<span data-ttu-id="9fcf7-170">Spécifie le type d’objet auquel s’applique la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="9fcf7-171">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="9fcf7-171">Values of the xsd:int type.</span></span>  <br/> |
   

