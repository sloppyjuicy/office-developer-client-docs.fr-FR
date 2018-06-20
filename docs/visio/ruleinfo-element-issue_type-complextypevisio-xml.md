---
title: Élément RuleInfo (Issue_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Spécifie des informations sur la règle de validation concerne le problème de validation parent.
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789560"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="0f6e8-103">Élément RuleInfo (Issue_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0f6e8-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0f6e8-104">Spécifie des informations sur la règle de validation concerne le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f6e8-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="0f6e8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f6e8-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0f6e8-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="0f6e8-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0f6e8-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0f6e8-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0f6e8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0f6e8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0f6e8-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0f6e8-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="0f6e8-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f6e8-113">Définition</span><span class="sxs-lookup"><span data-stu-id="0f6e8-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0f6e8-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0f6e8-114">Elements and attributes</span></span>

<span data-ttu-id="0f6e8-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0f6e8-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f6e8-116">Parent elements</span></span>

|<span data-ttu-id="0f6e8-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-117">**Element**</span></span>|<span data-ttu-id="0f6e8-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-118">**Type**</span></span>|<span data-ttu-id="0f6e8-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f6e8-120">Problème</span><span class="sxs-lookup"><span data-stu-id="0f6e8-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f6e8-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="0f6e8-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f6e8-122">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f6e8-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f6e8-123">Child elements</span></span>

<span data-ttu-id="0f6e8-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f6e8-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f6e8-125">Attributes</span></span>

|<span data-ttu-id="0f6e8-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-126">**Attribute**</span></span>|<span data-ttu-id="0f6e8-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-127">**Type**</span></span>|<span data-ttu-id="0f6e8-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-128">**Required**</span></span>|<span data-ttu-id="0f6e8-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-129">**Description**</span></span>|<span data-ttu-id="0f6e8-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0f6e8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0f6e8-131">ID de la règle</span><span class="sxs-lookup"><span data-stu-id="0f6e8-131">RuleID</span></span>  <br/> |<span data-ttu-id="0f6e8-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f6e8-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0f6e8-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0f6e8-133">required</span></span>  <br/> |<span data-ttu-id="0f6e8-134">Spécifie l’identificateur unique de la règle de validation concerne le problème parent.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="0f6e8-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0f6e8-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="0f6e8-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="0f6e8-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f6e8-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0f6e8-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0f6e8-138">required</span></span>  <br/> |<span data-ttu-id="0f6e8-139">Spécifie l’identificateur unique de l’ensemble de règles de validation concerne le problème parent.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="0f6e8-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0f6e8-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

