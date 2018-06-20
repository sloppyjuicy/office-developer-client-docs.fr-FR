---
title: Élément RuleTest (Rule_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: Spécifie l’expression logique qui détermine si l’objet cible correspond à la règle de validation.
ms.openlocfilehash: 25569530af5bc6f4b00e8600d1e25d968a01f246
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789580"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="1f7ea-103">Élément RuleTest (Rule_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1f7ea-103">RuleTest element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1f7ea-104">Spécifie l’expression logique qui détermine si l’objet cible correspond à la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="1f7ea-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f7ea-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="1f7ea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f7ea-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1f7ea-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="1f7ea-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1f7ea-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1f7ea-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1f7ea-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1f7ea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1f7ea-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1f7ea-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="1f7ea-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1f7ea-113">Définition</span><span class="sxs-lookup"><span data-stu-id="1f7ea-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1f7ea-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1f7ea-114">Elements and attributes</span></span>

<span data-ttu-id="1f7ea-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1f7ea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1f7ea-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1f7ea-116">Parent elements</span></span>

|<span data-ttu-id="1f7ea-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-117">**Element**</span></span>|<span data-ttu-id="1f7ea-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-118">**Type**</span></span>|<span data-ttu-id="1f7ea-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1f7ea-120">Règle</span><span class="sxs-lookup"><span data-stu-id="1f7ea-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f7ea-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="1f7ea-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1f7ea-122">Représente une règle de validation unique dans un ensemble de règles de validation de diagramme.</span><span class="sxs-lookup"><span data-stu-id="1f7ea-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1f7ea-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1f7ea-123">Child elements</span></span>

<span data-ttu-id="1f7ea-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1f7ea-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f7ea-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="1f7ea-125">Attributes</span></span>

|<span data-ttu-id="1f7ea-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-126">**Attribute**</span></span>|<span data-ttu-id="1f7ea-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-127">**Type**</span></span>|<span data-ttu-id="1f7ea-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-128">**Required**</span></span>|<span data-ttu-id="1f7ea-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-129">**Description**</span></span>|<span data-ttu-id="1f7ea-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1f7ea-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1f7ea-131">Formule</span><span class="sxs-lookup"><span data-stu-id="1f7ea-131">Formula</span></span>  <br/> |<span data-ttu-id="1f7ea-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1f7ea-132">xsd:string</span></span>  <br/> |<span data-ttu-id="1f7ea-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="1f7ea-133">optional</span></span>  <br/> |<span data-ttu-id="1f7ea-134">Représente la formule de l’élément.</span><span class="sxs-lookup"><span data-stu-id="1f7ea-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="1f7ea-135">Valeurs de la xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1f7ea-135">Values of the xsd:string.</span></span>  <br/> |
   

