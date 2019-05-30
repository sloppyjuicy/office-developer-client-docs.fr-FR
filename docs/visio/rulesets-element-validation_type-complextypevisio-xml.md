---
title: Élément de la Validation_Type (complexType XML)
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
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="17281-103">Élément de la Validation_Type (complexType XML)</span><span class="sxs-lookup"><span data-stu-id="17281-103">RuleSets element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="17281-104">Inclut un élément **RuleSet** pour chaque ensemble de règles de validation dans le document.</span><span class="sxs-lookup"><span data-stu-id="17281-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="17281-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="17281-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17281-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="17281-106">**Element type**</span></span> <br/> |[<span data-ttu-id="17281-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="17281-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="17281-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17281-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="17281-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="17281-109">**Schema file**</span></span> <br/> |<span data-ttu-id="17281-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="17281-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="17281-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="17281-111">**Document parts**</span></span> <br/> |<span data-ttu-id="17281-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="17281-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17281-113">Définition</span><span class="sxs-lookup"><span data-stu-id="17281-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17281-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="17281-114">Elements and attributes</span></span>

<span data-ttu-id="17281-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="17281-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17281-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="17281-116">Parent elements</span></span>

|<span data-ttu-id="17281-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="17281-117">**Element**</span></span>|<span data-ttu-id="17281-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="17281-118">**Type**</span></span>|<span data-ttu-id="17281-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="17281-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17281-120">Valider</span><span class="sxs-lookup"><span data-stu-id="17281-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="17281-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="17281-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17281-122">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="17281-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17281-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17281-123">Child elements</span></span>

|<span data-ttu-id="17281-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="17281-124">**Element**</span></span>|<span data-ttu-id="17281-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="17281-125">**Type**</span></span>|<span data-ttu-id="17281-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="17281-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17281-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="17281-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17281-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="17281-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17281-129">Représente un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="17281-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="17281-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="17281-130">Attributes</span></span>

<span data-ttu-id="17281-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="17281-131">None.</span></span>
  

