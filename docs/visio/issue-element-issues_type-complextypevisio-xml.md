---
title: Élément problème (Issues_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Représente un problème de validation unique dans le document.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788879"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="fdd04-103">Élément problème (Issues_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="fdd04-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fdd04-104">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="fdd04-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fdd04-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="fdd04-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fdd04-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="fdd04-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fdd04-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="fdd04-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fdd04-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="fdd04-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fdd04-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fdd04-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fdd04-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fdd04-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fdd04-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="fdd04-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fdd04-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="fdd04-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fdd04-113">Définition</span><span class="sxs-lookup"><span data-stu-id="fdd04-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fdd04-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fdd04-114">Elements and attributes</span></span>

<span data-ttu-id="fdd04-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="fdd04-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fdd04-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fdd04-116">Parent elements</span></span>

|<span data-ttu-id="fdd04-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fdd04-117">**Element**</span></span>|<span data-ttu-id="fdd04-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="fdd04-118">**Type**</span></span>|<span data-ttu-id="fdd04-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fdd04-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fdd04-120">Problèmes</span><span class="sxs-lookup"><span data-stu-id="fdd04-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fdd04-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="fdd04-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fdd04-122">Contient tous les éléments de **problème** pour le document.</span><span class="sxs-lookup"><span data-stu-id="fdd04-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fdd04-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fdd04-123">Child elements</span></span>

|<span data-ttu-id="fdd04-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fdd04-124">**Element**</span></span>|<span data-ttu-id="fdd04-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="fdd04-125">**Type**</span></span>|<span data-ttu-id="fdd04-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="fdd04-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fdd04-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="fdd04-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fdd04-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="fdd04-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fdd04-129">En fonction de la cible de l’objet parent de validation, spécifie soit la page, ou la page et la forme, associé à ce problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="fdd04-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="fdd04-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="fdd04-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fdd04-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="fdd04-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fdd04-132">Spécifie des informations sur la règle de validation concerne le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="fdd04-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fdd04-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="fdd04-133">Attributes</span></span>

|<span data-ttu-id="fdd04-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fdd04-134">**Attribute**</span></span>|<span data-ttu-id="fdd04-135">**Type**</span><span class="sxs-lookup"><span data-stu-id="fdd04-135">**Type**</span></span>|<span data-ttu-id="fdd04-136">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fdd04-136">**Required**</span></span>|<span data-ttu-id="fdd04-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="fdd04-137">**Description**</span></span>|<span data-ttu-id="fdd04-138">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fdd04-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fdd04-139">ID</span><span class="sxs-lookup"><span data-stu-id="fdd04-139">ID</span></span>  <br/> |<span data-ttu-id="fdd04-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fdd04-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fdd04-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fdd04-141">required</span></span>  <br/> |<span data-ttu-id="fdd04-142">Spécifie l’identificateur unique du problème de validation.</span><span class="sxs-lookup"><span data-stu-id="fdd04-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="fdd04-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fdd04-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fdd04-144">Ignoré</span><span class="sxs-lookup"><span data-stu-id="fdd04-144">Ignored</span></span>  <br/> |<span data-ttu-id="fdd04-145">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="fdd04-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fdd04-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="fdd04-146">optional</span></span>  <br/> |<span data-ttu-id="fdd04-147">Spécifie des informations sur la règle de validation concerne le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="fdd04-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="fdd04-148">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="fdd04-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

