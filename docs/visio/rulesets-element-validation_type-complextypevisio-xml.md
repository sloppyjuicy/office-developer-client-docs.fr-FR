---
title: Élément RuleSets (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Inclut un élément RuleSet pour chaque ensemble de règles de validation dans le document.
ms.openlocfilehash: 0aca3f52bd8b201d1afc2ab7d647757452ff8899
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541574"
---
# <a name="rulesets-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="44682-103">Élément RuleSets (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="44682-103">RuleSets element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="44682-104">Inclut **un élément RuleSet** pour chaque ensemble de règles de validation dans le document.</span><span class="sxs-lookup"><span data-stu-id="44682-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="44682-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="44682-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44682-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="44682-106">**Element type**</span></span> <br/> |[<span data-ttu-id="44682-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="44682-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="44682-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="44682-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="44682-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="44682-109">**Schema file**</span></span> <br/> |<span data-ttu-id="44682-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="44682-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="44682-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="44682-111">**Document parts**</span></span> <br/> |<span data-ttu-id="44682-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="44682-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="44682-113">Définition</span><span class="sxs-lookup"><span data-stu-id="44682-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="44682-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="44682-114">Elements and attributes</span></span>

<span data-ttu-id="44682-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="44682-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="44682-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="44682-116">Parent elements</span></span>

|<span data-ttu-id="44682-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="44682-117">**Element**</span></span>|<span data-ttu-id="44682-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="44682-118">**Type**</span></span>|<span data-ttu-id="44682-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="44682-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44682-120">Valider</span><span class="sxs-lookup"><span data-stu-id="44682-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="44682-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="44682-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44682-122">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="44682-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="44682-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="44682-123">Child elements</span></span>

|<span data-ttu-id="44682-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="44682-124">**Element**</span></span>|<span data-ttu-id="44682-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="44682-125">**Type**</span></span>|<span data-ttu-id="44682-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="44682-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44682-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="44682-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44682-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="44682-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44682-129">Représente un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="44682-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="44682-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="44682-130">Attributes</span></span>

<span data-ttu-id="44682-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="44682-131">None.</span></span>
  

