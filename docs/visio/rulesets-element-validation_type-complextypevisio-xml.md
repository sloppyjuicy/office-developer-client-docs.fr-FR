---
title: RuleSets, élément (Validation_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Inclut un élément RuleSet pour chaque règle de validation définie dans le document.
ms.openlocfilehash: 84d64a8539f1b83c16a96a61ea68e9b2660c9036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789583"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="1ed6f-103">RuleSets, élément (Validation_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1ed6f-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1ed6f-104">Inclut un élément **RuleSet** pour chaque règle de validation définie dans le document.</span><span class="sxs-lookup"><span data-stu-id="1ed6f-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1ed6f-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="1ed6f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ed6f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1ed6f-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="1ed6f-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1ed6f-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1ed6f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1ed6f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1ed6f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1ed6f-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1ed6f-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="1ed6f-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ed6f-113">Définition</span><span class="sxs-lookup"><span data-stu-id="1ed6f-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1ed6f-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1ed6f-114">Elements and attributes</span></span>

<span data-ttu-id="1ed6f-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1ed6f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1ed6f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1ed6f-116">Parent elements</span></span>

|<span data-ttu-id="1ed6f-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-117">**Element**</span></span>|<span data-ttu-id="1ed6f-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-118">**Type**</span></span>|<span data-ttu-id="1ed6f-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ed6f-120">Valider</span><span class="sxs-lookup"><span data-stu-id="1ed6f-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="1ed6f-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="1ed6f-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ed6f-122">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="1ed6f-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ed6f-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1ed6f-123">Child elements</span></span>

|<span data-ttu-id="1ed6f-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-124">**Element**</span></span>|<span data-ttu-id="1ed6f-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-125">**Type**</span></span>|<span data-ttu-id="1ed6f-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="1ed6f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ed6f-127">Ensemble de règles</span><span class="sxs-lookup"><span data-stu-id="1ed6f-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ed6f-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="1ed6f-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ed6f-129">Représente un ensemble de règles de validation du diagramme.</span><span class="sxs-lookup"><span data-stu-id="1ed6f-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1ed6f-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="1ed6f-130">Attributes</span></span>

<span data-ttu-id="1ed6f-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1ed6f-131">None.</span></span>
  

