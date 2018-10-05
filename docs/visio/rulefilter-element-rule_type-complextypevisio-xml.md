---
title: Élément RuleFilter (Rule_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.
ms.openlocfilehash: 8d4167fbb8dde54c55e49debb77fe307ecab6771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396727"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="66c15-103">Élément RuleFilter (Rule_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="66c15-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="66c15-104">Spécifie l’expression logique qui détermine si la règle de validation doit être appliquée à un objet cible.</span><span class="sxs-lookup"><span data-stu-id="66c15-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66c15-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="66c15-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66c15-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="66c15-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66c15-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="66c15-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66c15-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="66c15-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66c15-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="66c15-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66c15-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="66c15-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66c15-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="66c15-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66c15-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="66c15-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66c15-113">Définition</span><span class="sxs-lookup"><span data-stu-id="66c15-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66c15-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="66c15-114">Elements and attributes</span></span>

<span data-ttu-id="66c15-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="66c15-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66c15-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="66c15-116">Parent elements</span></span>

|<span data-ttu-id="66c15-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="66c15-117">**Element**</span></span>|<span data-ttu-id="66c15-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="66c15-118">**Type**</span></span>|<span data-ttu-id="66c15-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="66c15-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66c15-120">Règle</span><span class="sxs-lookup"><span data-stu-id="66c15-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66c15-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="66c15-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66c15-122">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="66c15-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66c15-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66c15-123">Child elements</span></span>

<span data-ttu-id="66c15-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="66c15-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66c15-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="66c15-125">Attributes</span></span>

|<span data-ttu-id="66c15-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="66c15-126">**Attribute**</span></span>|<span data-ttu-id="66c15-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="66c15-127">**Type**</span></span>|<span data-ttu-id="66c15-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="66c15-128">**Required**</span></span>|<span data-ttu-id="66c15-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="66c15-129">**Description**</span></span>|<span data-ttu-id="66c15-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="66c15-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="66c15-131">Formule</span><span class="sxs-lookup"><span data-stu-id="66c15-131">Formula</span></span>  <br/> |<span data-ttu-id="66c15-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="66c15-132">xsd:string</span></span>  <br/> |<span data-ttu-id="66c15-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="66c15-133">optional</span></span>  <br/> |<span data-ttu-id="66c15-134">Représente la formule de l’élément.</span><span class="sxs-lookup"><span data-stu-id="66c15-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="66c15-135">Valeurs de la xsd : String.</span><span class="sxs-lookup"><span data-stu-id="66c15-135">Values of the xsd:string.</span></span>  <br/> |
   

