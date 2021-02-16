---
title: Élément Validation (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Stocke les informations relatives à la validation du diagramme pour le document.
ms.openlocfilehash: b1b1bcbd70d57d7a7316e91d137cf8c3c3750722
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538549"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="ef41e-103">Élément Validation (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ef41e-103">Validation element (Visio XML)</span></span>

<span data-ttu-id="ef41e-104">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="ef41e-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef41e-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="ef41e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef41e-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ef41e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ef41e-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="ef41e-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ef41e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef41e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ef41e-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ef41e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ef41e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ef41e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ef41e-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="ef41e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ef41e-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="ef41e-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef41e-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ef41e-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef41e-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ef41e-114">Elements and attributes</span></span>

<span data-ttu-id="ef41e-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="ef41e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ef41e-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ef41e-116">Parent elements</span></span>

<span data-ttu-id="ef41e-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="ef41e-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef41e-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef41e-118">Child elements</span></span>

|<span data-ttu-id="ef41e-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ef41e-119">**Element**</span></span>|<span data-ttu-id="ef41e-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ef41e-120">**Type**</span></span>|<span data-ttu-id="ef41e-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef41e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef41e-122">Issues</span><span class="sxs-lookup"><span data-stu-id="ef41e-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef41e-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="ef41e-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef41e-124">Contient tous les **éléments Issue** du document.</span><span class="sxs-lookup"><span data-stu-id="ef41e-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="ef41e-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="ef41e-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef41e-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="ef41e-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef41e-127">Inclut **un élément RuleSet** pour chaque ensemble de règles de validation dans le document.</span><span class="sxs-lookup"><span data-stu-id="ef41e-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="ef41e-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="ef41e-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef41e-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="ef41e-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef41e-130">Encapsule les propriétés liées à la validation du document.</span><span class="sxs-lookup"><span data-stu-id="ef41e-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ef41e-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef41e-131">Attributes</span></span>

<span data-ttu-id="ef41e-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ef41e-132">None.</span></span>
  

