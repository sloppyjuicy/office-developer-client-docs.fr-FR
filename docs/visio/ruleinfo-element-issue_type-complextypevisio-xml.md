---
title: Élément RuleInfo (Issue_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Spécifie des informations sur la règle de validation concerne le problème de validation parent.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394747"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="cf6f7-103">Élément RuleInfo (Issue_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="cf6f7-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cf6f7-104">Spécifie des informations sur la règle de validation concerne le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf6f7-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="cf6f7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf6f7-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cf6f7-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="cf6f7-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cf6f7-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cf6f7-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cf6f7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cf6f7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cf6f7-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cf6f7-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="cf6f7-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf6f7-113">Définition</span><span class="sxs-lookup"><span data-stu-id="cf6f7-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf6f7-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="cf6f7-114">Elements and attributes</span></span>

<span data-ttu-id="cf6f7-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cf6f7-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cf6f7-116">Parent elements</span></span>

|<span data-ttu-id="cf6f7-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-117">**Element**</span></span>|<span data-ttu-id="cf6f7-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-118">**Type**</span></span>|<span data-ttu-id="cf6f7-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cf6f7-120">Problème</span><span class="sxs-lookup"><span data-stu-id="cf6f7-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cf6f7-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="cf6f7-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cf6f7-122">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf6f7-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cf6f7-123">Child elements</span></span>

<span data-ttu-id="cf6f7-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf6f7-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="cf6f7-125">Attributes</span></span>

|<span data-ttu-id="cf6f7-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-126">**Attribute**</span></span>|<span data-ttu-id="cf6f7-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-127">**Type**</span></span>|<span data-ttu-id="cf6f7-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-128">**Required**</span></span>|<span data-ttu-id="cf6f7-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-129">**Description**</span></span>|<span data-ttu-id="cf6f7-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf6f7-131">ID de la règle</span><span class="sxs-lookup"><span data-stu-id="cf6f7-131">RuleID</span></span>  <br/> |<span data-ttu-id="cf6f7-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf6f7-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf6f7-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cf6f7-133">required</span></span>  <br/> |<span data-ttu-id="cf6f7-134">Spécifie l’identificateur unique de la règle de validation concerne le problème parent.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="cf6f7-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf6f7-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="cf6f7-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="cf6f7-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf6f7-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf6f7-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cf6f7-138">required</span></span>  <br/> |<span data-ttu-id="cf6f7-139">Spécifie l’identificateur unique de l’ensemble de règles de validation concerne le problème parent.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="cf6f7-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

