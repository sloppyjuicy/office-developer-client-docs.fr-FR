---
title: Élément issue (Issues_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Représente un problème de validation unique dans le document.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317905"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="8398f-103">Élément issue (Issues_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8398f-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8398f-104">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="8398f-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8398f-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="8398f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8398f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="8398f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8398f-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8398f-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8398f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8398f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8398f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="8398f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8398f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8398f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8398f-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="8398f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8398f-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="8398f-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8398f-113">Définition</span><span class="sxs-lookup"><span data-stu-id="8398f-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8398f-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="8398f-114">Elements and attributes</span></span>

<span data-ttu-id="8398f-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="8398f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8398f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8398f-116">Parent elements</span></span>

|<span data-ttu-id="8398f-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8398f-117">**Element**</span></span>|<span data-ttu-id="8398f-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="8398f-118">**Type**</span></span>|<span data-ttu-id="8398f-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="8398f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8398f-120">Issues</span><span class="sxs-lookup"><span data-stu-id="8398f-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8398f-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="8398f-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8398f-122">Contient tous les éléments de **problème** pour le document.</span><span class="sxs-lookup"><span data-stu-id="8398f-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8398f-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8398f-123">Child elements</span></span>

|<span data-ttu-id="8398f-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8398f-124">**Element**</span></span>|<span data-ttu-id="8398f-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="8398f-125">**Type**</span></span>|<span data-ttu-id="8398f-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="8398f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8398f-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="8398f-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8398f-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="8398f-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8398f-129">En fonction de la cible du problème de validation parent, spécifie soit la page, soit la page et la forme, associées au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="8398f-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="8398f-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="8398f-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8398f-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="8398f-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8398f-132">Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="8398f-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8398f-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="8398f-133">Attributes</span></span>

|<span data-ttu-id="8398f-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8398f-134">**Attribute**</span></span>|<span data-ttu-id="8398f-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="8398f-135">**Type**</span></span>|<span data-ttu-id="8398f-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8398f-136">**Required**</span></span>|<span data-ttu-id="8398f-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="8398f-137">**Description**</span></span>|<span data-ttu-id="8398f-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8398f-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8398f-139">ID</span><span class="sxs-lookup"><span data-stu-id="8398f-139">ID</span></span>  <br/> |<span data-ttu-id="8398f-140">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8398f-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8398f-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8398f-141">required</span></span>  <br/> |<span data-ttu-id="8398f-142">Spécifie l'identificateur unique du problème de validation.</span><span class="sxs-lookup"><span data-stu-id="8398f-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="8398f-143">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8398f-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8398f-144">Ignoré</span><span class="sxs-lookup"><span data-stu-id="8398f-144">Ignored</span></span>  <br/> |<span data-ttu-id="8398f-145">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="8398f-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8398f-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="8398f-146">optional</span></span>  <br/> |<span data-ttu-id="8398f-147">Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="8398f-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="8398f-148">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8398f-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

