---
title: Élément issue (Issues_Type complexType) (XML Visio)
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
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="fa957-103">Élément issue (Issues_Type complexType) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="fa957-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fa957-104">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="fa957-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa957-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="fa957-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa957-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="fa957-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fa957-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="fa957-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fa957-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fa957-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fa957-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fa957-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fa957-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fa957-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fa957-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="fa957-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fa957-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="fa957-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fa957-113">Définition</span><span class="sxs-lookup"><span data-stu-id="fa957-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fa957-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fa957-114">Elements and attributes</span></span>

<span data-ttu-id="fa957-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="fa957-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fa957-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fa957-116">Parent elements</span></span>

|<span data-ttu-id="fa957-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fa957-117">**Element**</span></span>|<span data-ttu-id="fa957-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="fa957-118">**Type**</span></span>|<span data-ttu-id="fa957-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fa957-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fa957-120">Issues</span><span class="sxs-lookup"><span data-stu-id="fa957-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fa957-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="fa957-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fa957-122">Contient tous les éléments de **problème** pour le document.</span><span class="sxs-lookup"><span data-stu-id="fa957-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fa957-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fa957-123">Child elements</span></span>

|<span data-ttu-id="fa957-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fa957-124">**Element**</span></span>|<span data-ttu-id="fa957-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="fa957-125">**Type**</span></span>|<span data-ttu-id="fa957-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="fa957-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fa957-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="fa957-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fa957-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="fa957-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fa957-129">En fonction de la cible du problème de validation parent, spécifie soit la page, soit la page et la forme, associées au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="fa957-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="fa957-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="fa957-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fa957-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="fa957-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fa957-132">Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="fa957-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fa957-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="fa957-133">Attributes</span></span>

|<span data-ttu-id="fa957-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fa957-134">**Attribute**</span></span>|<span data-ttu-id="fa957-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="fa957-135">**Type**</span></span>|<span data-ttu-id="fa957-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fa957-136">**Required**</span></span>|<span data-ttu-id="fa957-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="fa957-137">**Description**</span></span>|<span data-ttu-id="fa957-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fa957-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fa957-139">ID</span><span class="sxs-lookup"><span data-stu-id="fa957-139">ID</span></span>  <br/> |<span data-ttu-id="fa957-140">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fa957-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fa957-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fa957-141">required</span></span>  <br/> |<span data-ttu-id="fa957-142">Spécifie l’identificateur unique du problème de validation.</span><span class="sxs-lookup"><span data-stu-id="fa957-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="fa957-143">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fa957-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fa957-144">Ignoré</span><span class="sxs-lookup"><span data-stu-id="fa957-144">Ignored</span></span>  <br/> |<span data-ttu-id="fa957-145">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="fa957-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fa957-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="fa957-146">optional</span></span>  <br/> |<span data-ttu-id="fa957-147">Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="fa957-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="fa957-148">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="fa957-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

