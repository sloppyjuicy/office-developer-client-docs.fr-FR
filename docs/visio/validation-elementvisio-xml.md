---
title: Élément de validation (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Stocke les informations relatives à la validation du diagramme pour le document.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382357"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="5636d-103">Élément de validation (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="5636d-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="5636d-104">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="5636d-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5636d-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="5636d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5636d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="5636d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5636d-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="5636d-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5636d-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="5636d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5636d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5636d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5636d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5636d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5636d-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="5636d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5636d-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="5636d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5636d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="5636d-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5636d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5636d-114">Elements and attributes</span></span>

<span data-ttu-id="5636d-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="5636d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5636d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5636d-116">Parent elements</span></span>

<span data-ttu-id="5636d-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="5636d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5636d-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5636d-118">Child elements</span></span>

|<span data-ttu-id="5636d-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5636d-119">**Element**</span></span>|<span data-ttu-id="5636d-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="5636d-120">**Type**</span></span>|<span data-ttu-id="5636d-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="5636d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5636d-122">Problèmes</span><span class="sxs-lookup"><span data-stu-id="5636d-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5636d-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="5636d-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5636d-124">Contient tous les éléments de **problème** pour le document.</span><span class="sxs-lookup"><span data-stu-id="5636d-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="5636d-125">Groupes de règles</span><span class="sxs-lookup"><span data-stu-id="5636d-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5636d-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="5636d-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5636d-127">Inclut un élément **RuleSet** pour chaque règle de validation définie dans le document.</span><span class="sxs-lookup"><span data-stu-id="5636d-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="5636d-128">Propriétésla</span><span class="sxs-lookup"><span data-stu-id="5636d-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5636d-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="5636d-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5636d-130">Encapsule les propriétés qui sont liées à la validation du document.</span><span class="sxs-lookup"><span data-stu-id="5636d-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5636d-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="5636d-131">Attributes</span></span>

<span data-ttu-id="5636d-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5636d-132">None.</span></span>
  

