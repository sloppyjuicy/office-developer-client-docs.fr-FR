---
title: Élément Issue (Issues_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Représente un problème de validation unique dans le document.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541126"
---
# <a name="issue-element-issues_type-complextype-visio-xml"></a><span data-ttu-id="8bed1-103">Élément Issue (Issues_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8bed1-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8bed1-104">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="8bed1-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bed1-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="8bed1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bed1-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="8bed1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8bed1-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8bed1-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8bed1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8bed1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8bed1-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="8bed1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8bed1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8bed1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8bed1-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="8bed1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8bed1-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="8bed1-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8bed1-113">Définition</span><span class="sxs-lookup"><span data-stu-id="8bed1-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8bed1-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="8bed1-114">Elements and attributes</span></span>

<span data-ttu-id="8bed1-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="8bed1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8bed1-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8bed1-116">Parent elements</span></span>

|<span data-ttu-id="8bed1-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8bed1-117">**Element**</span></span>|<span data-ttu-id="8bed1-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="8bed1-118">**Type**</span></span>|<span data-ttu-id="8bed1-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="8bed1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8bed1-120">Issues</span><span class="sxs-lookup"><span data-stu-id="8bed1-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8bed1-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="8bed1-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8bed1-122">Contient tous les **éléments Issue** du document.</span><span class="sxs-lookup"><span data-stu-id="8bed1-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8bed1-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8bed1-123">Child elements</span></span>

|<span data-ttu-id="8bed1-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8bed1-124">**Element**</span></span>|<span data-ttu-id="8bed1-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="8bed1-125">**Type**</span></span>|<span data-ttu-id="8bed1-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="8bed1-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8bed1-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="8bed1-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8bed1-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="8bed1-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8bed1-129">Selon la cible du problème de validation parent, spécifie la page, ou la page et la forme, associées au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="8bed1-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="8bed1-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="8bed1-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8bed1-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="8bed1-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8bed1-132">Spécifie les informations relatives à la règle de validation à qui appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="8bed1-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8bed1-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="8bed1-133">Attributes</span></span>

|<span data-ttu-id="8bed1-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8bed1-134">**Attribute**</span></span>|<span data-ttu-id="8bed1-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="8bed1-135">**Type**</span></span>|<span data-ttu-id="8bed1-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8bed1-136">**Required**</span></span>|<span data-ttu-id="8bed1-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="8bed1-137">**Description**</span></span>|<span data-ttu-id="8bed1-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8bed1-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8bed1-139">ID</span><span class="sxs-lookup"><span data-stu-id="8bed1-139">ID</span></span>  <br/> |<span data-ttu-id="8bed1-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8bed1-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8bed1-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8bed1-141">required</span></span>  <br/> |<span data-ttu-id="8bed1-142">Spécifie l’identificateur unique du problème de validation.</span><span class="sxs-lookup"><span data-stu-id="8bed1-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="8bed1-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8bed1-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8bed1-144">Ignoré</span><span class="sxs-lookup"><span data-stu-id="8bed1-144">Ignored</span></span>  <br/> |<span data-ttu-id="8bed1-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8bed1-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8bed1-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="8bed1-146">optional</span></span>  <br/> |<span data-ttu-id="8bed1-147">Spécifie les informations relatives à la règle de validation à qui appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="8bed1-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="8bed1-148">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8bed1-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

