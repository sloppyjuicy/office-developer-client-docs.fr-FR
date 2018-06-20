---
title: Élément RuleFilter (Rule_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.
ms.openlocfilehash: f2862fe4f4b6a644d80ca0393270594766d940be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789552"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="b3f26-103">Élément RuleFilter (Rule_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="b3f26-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b3f26-104">Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.</span><span class="sxs-lookup"><span data-stu-id="b3f26-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3f26-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="b3f26-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3f26-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="b3f26-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b3f26-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="b3f26-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b3f26-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="b3f26-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b3f26-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b3f26-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b3f26-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b3f26-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b3f26-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="b3f26-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b3f26-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="b3f26-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b3f26-113">Définition</span><span class="sxs-lookup"><span data-stu-id="b3f26-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b3f26-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b3f26-114">Elements and attributes</span></span>

<span data-ttu-id="b3f26-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="b3f26-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b3f26-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b3f26-116">Parent elements</span></span>

|<span data-ttu-id="b3f26-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b3f26-117">**Element**</span></span>|<span data-ttu-id="b3f26-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="b3f26-118">**Type**</span></span>|<span data-ttu-id="b3f26-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3f26-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3f26-120">Règle</span><span class="sxs-lookup"><span data-stu-id="b3f26-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b3f26-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="b3f26-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b3f26-122">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="b3f26-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b3f26-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b3f26-123">Child elements</span></span>

<span data-ttu-id="b3f26-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b3f26-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3f26-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="b3f26-125">Attributes</span></span>

|<span data-ttu-id="b3f26-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b3f26-126">**Attribute**</span></span>|<span data-ttu-id="b3f26-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="b3f26-127">**Type**</span></span>|<span data-ttu-id="b3f26-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b3f26-128">**Required**</span></span>|<span data-ttu-id="b3f26-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3f26-129">**Description**</span></span>|<span data-ttu-id="b3f26-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b3f26-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b3f26-131">Formule</span><span class="sxs-lookup"><span data-stu-id="b3f26-131">Formula</span></span>  <br/> |<span data-ttu-id="b3f26-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="b3f26-132">xsd:string</span></span>  <br/> |<span data-ttu-id="b3f26-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="b3f26-133">optional</span></span>  <br/> |<span data-ttu-id="b3f26-134">Représente la formule de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b3f26-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="b3f26-135">Valeurs de la xsd : String.</span><span class="sxs-lookup"><span data-stu-id="b3f26-135">Values of the xsd:string.</span></span>  <br/> |
   

