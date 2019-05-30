---
title: Élément RuleFilter (complexType Rule_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541679"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="04418-103">Élément RuleFilter (complexType Rule_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="04418-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="04418-104">Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.</span><span class="sxs-lookup"><span data-stu-id="04418-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04418-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="04418-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04418-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="04418-106">**Element type**</span></span> <br/> |[<span data-ttu-id="04418-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="04418-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="04418-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="04418-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="04418-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="04418-109">**Schema file**</span></span> <br/> |<span data-ttu-id="04418-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="04418-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="04418-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="04418-111">**Document parts**</span></span> <br/> |<span data-ttu-id="04418-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="04418-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04418-113">Définition</span><span class="sxs-lookup"><span data-stu-id="04418-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="04418-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="04418-114">Elements and attributes</span></span>

<span data-ttu-id="04418-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="04418-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="04418-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="04418-116">Parent elements</span></span>

|<span data-ttu-id="04418-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="04418-117">**Element**</span></span>|<span data-ttu-id="04418-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="04418-118">**Type**</span></span>|<span data-ttu-id="04418-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="04418-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="04418-120">Règle</span><span class="sxs-lookup"><span data-stu-id="04418-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="04418-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="04418-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="04418-122">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="04418-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="04418-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="04418-123">Child elements</span></span>

<span data-ttu-id="04418-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="04418-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04418-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="04418-125">Attributes</span></span>

|<span data-ttu-id="04418-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="04418-126">**Attribute**</span></span>|<span data-ttu-id="04418-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="04418-127">**Type**</span></span>|<span data-ttu-id="04418-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="04418-128">**Required**</span></span>|<span data-ttu-id="04418-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="04418-129">**Description**</span></span>|<span data-ttu-id="04418-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="04418-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04418-131">Formule</span><span class="sxs-lookup"><span data-stu-id="04418-131">Formula</span></span>  <br/> |<span data-ttu-id="04418-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="04418-132">xsd:string</span></span>  <br/> |<span data-ttu-id="04418-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="04418-133">optional</span></span>  <br/> |<span data-ttu-id="04418-134">Représente la formule de l’élément.</span><span class="sxs-lookup"><span data-stu-id="04418-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="04418-135">Valeurs de la chaîne XSD: String.</span><span class="sxs-lookup"><span data-stu-id="04418-135">Values of the xsd:string.</span></span>  <br/> |
   

