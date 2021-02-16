---
title: Élément Rule (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541707"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a><span data-ttu-id="3c98c-103">Élément Rule (RuleSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3c98c-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3c98c-104">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="3c98c-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c98c-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="3c98c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c98c-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="3c98c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3c98c-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="3c98c-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3c98c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3c98c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3c98c-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3c98c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3c98c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3c98c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3c98c-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="3c98c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3c98c-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="3c98c-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c98c-113">Définition</span><span class="sxs-lookup"><span data-stu-id="3c98c-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3c98c-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3c98c-114">Elements and attributes</span></span>

<span data-ttu-id="3c98c-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="3c98c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3c98c-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3c98c-116">Parent elements</span></span>

|<span data-ttu-id="3c98c-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3c98c-117">**Element**</span></span>|<span data-ttu-id="3c98c-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="3c98c-118">**Type**</span></span>|<span data-ttu-id="3c98c-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="3c98c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c98c-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="3c98c-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c98c-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="3c98c-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c98c-122">Représente un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="3c98c-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c98c-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3c98c-123">Child elements</span></span>

|<span data-ttu-id="3c98c-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3c98c-124">**Element**</span></span>|<span data-ttu-id="3c98c-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="3c98c-125">**Type**</span></span>|<span data-ttu-id="3c98c-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="3c98c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c98c-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="3c98c-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c98c-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="3c98c-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c98c-129">Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.</span><span class="sxs-lookup"><span data-stu-id="3c98c-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="3c98c-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="3c98c-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c98c-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="3c98c-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c98c-132">Spécifie l’expression logique qui détermine si l’objet cible satisfait à la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="3c98c-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3c98c-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="3c98c-133">Attributes</span></span>

|<span data-ttu-id="3c98c-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3c98c-134">**Attribute**</span></span>|<span data-ttu-id="3c98c-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="3c98c-135">**Type**</span></span>|<span data-ttu-id="3c98c-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3c98c-136">**Required**</span></span>|<span data-ttu-id="3c98c-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="3c98c-137">**Description**</span></span>|<span data-ttu-id="3c98c-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="3c98c-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3c98c-139">Catégorie</span><span class="sxs-lookup"><span data-stu-id="3c98c-139">Category</span></span>  <br/> |<span data-ttu-id="3c98c-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3c98c-140">xsd:string</span></span>  <br/> |<span data-ttu-id="3c98c-141">facultatif</span><span class="sxs-lookup"><span data-stu-id="3c98c-141">optional</span></span>  <br/> |<span data-ttu-id="3c98c-142">Spécifie le texte affiché dans la colonne **Catégorie** de la fenêtre Problèmes.</span><span class="sxs-lookup"><span data-stu-id="3c98c-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="3c98c-143">Il s'agit par défaut d'une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="3c98c-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="3c98c-144">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c98c-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c98c-145">Description</span><span class="sxs-lookup"><span data-stu-id="3c98c-145">Description</span></span>  <br/> |<span data-ttu-id="3c98c-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3c98c-146">xsd:string</span></span>  <br/> |<span data-ttu-id="3c98c-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="3c98c-147">optional</span></span>  <br/> |<span data-ttu-id="3c98c-148">Spécifie la description de la règle de validation qui apparaît dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c98c-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="3c98c-149">La valeur par défaut est « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="3c98c-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="3c98c-150">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c98c-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c98c-151">ID</span><span class="sxs-lookup"><span data-stu-id="3c98c-151">ID</span></span>  <br/> |<span data-ttu-id="3c98c-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3c98c-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c98c-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="3c98c-153">required</span></span>  <br/> |<span data-ttu-id="3c98c-154">Spécifie l’identificateur unique de la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="3c98c-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="3c98c-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3c98c-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3c98c-156">Ignoré</span><span class="sxs-lookup"><span data-stu-id="3c98c-156">Ignored</span></span>  <br/> |<span data-ttu-id="3c98c-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="3c98c-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3c98c-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="3c98c-158">optional</span></span>  <br/> |<span data-ttu-id="3c98c-159">Spécifie si la règle de validation est actuellement ignorée.</span><span class="sxs-lookup"><span data-stu-id="3c98c-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="3c98c-160">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="3c98c-160">Default is False.</span></span>  <br/> |<span data-ttu-id="3c98c-161">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3c98c-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3c98c-162">NameU</span><span class="sxs-lookup"><span data-stu-id="3c98c-162">NameU</span></span>  <br/> |<span data-ttu-id="3c98c-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3c98c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="3c98c-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="3c98c-164">required</span></span>  <br/> |<span data-ttu-id="3c98c-165">Spécifie le nom universel de la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="3c98c-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="3c98c-166">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c98c-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c98c-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="3c98c-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="3c98c-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="3c98c-168">xsd:int</span></span>  <br/> |<span data-ttu-id="3c98c-169">facultatif</span><span class="sxs-lookup"><span data-stu-id="3c98c-169">optional</span></span>  <br/> |<span data-ttu-id="3c98c-170">Spécifie le type d’objet auquel la règle de validation s’applique.</span><span class="sxs-lookup"><span data-stu-id="3c98c-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="3c98c-171">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="3c98c-171">Values of the xsd:int type.</span></span>  <br/> |
   

