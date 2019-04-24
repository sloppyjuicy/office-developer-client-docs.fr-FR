---
title: Validation, élément ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Stocke les informations relatives à la validation du diagramme pour le document.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329082"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="a1792-103">Validation, élément ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a1792-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="a1792-104">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="a1792-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1792-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a1792-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1792-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a1792-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a1792-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="a1792-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a1792-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a1792-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a1792-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a1792-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a1792-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a1792-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a1792-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="a1792-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a1792-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="a1792-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1792-113">Définition</span><span class="sxs-lookup"><span data-stu-id="a1792-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a1792-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a1792-114">Elements and attributes</span></span>

<span data-ttu-id="a1792-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a1792-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a1792-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a1792-116">Parent elements</span></span>

<span data-ttu-id="a1792-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="a1792-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1792-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a1792-118">Child elements</span></span>

|<span data-ttu-id="a1792-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a1792-119">**Element**</span></span>|<span data-ttu-id="a1792-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="a1792-120">**Type**</span></span>|<span data-ttu-id="a1792-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="a1792-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1792-122">Issues</span><span class="sxs-lookup"><span data-stu-id="a1792-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1792-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="a1792-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1792-124">Contient tous les éléments de **problème** pour le document.</span><span class="sxs-lookup"><span data-stu-id="a1792-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="a1792-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="a1792-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1792-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="a1792-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1792-127">Inclut un élément **RuleSet** pour chaque ensemble de règles de validation dans le document.</span><span class="sxs-lookup"><span data-stu-id="a1792-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="a1792-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="a1792-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1792-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="a1792-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1792-130">EnCapsule les propriétés liées à la validation du document.</span><span class="sxs-lookup"><span data-stu-id="a1792-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a1792-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="a1792-131">Attributes</span></span>

<span data-ttu-id="a1792-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a1792-132">None.</span></span>
  

