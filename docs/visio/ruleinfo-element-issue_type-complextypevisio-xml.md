---
title: Élément RuleInfo (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Spécifie les informations relatives à la règle de validation à qui appartient le problème de validation parent.
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541686"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="bd387-103">Élément RuleInfo (Issue_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bd387-103">RuleInfo element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="bd387-104">Spécifie les informations relatives à la règle de validation à qui appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="bd387-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd387-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="bd387-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd387-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="bd387-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bd387-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="bd387-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bd387-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bd387-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bd387-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="bd387-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bd387-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bd387-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bd387-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="bd387-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bd387-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="bd387-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd387-113">Définition</span><span class="sxs-lookup"><span data-stu-id="bd387-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bd387-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="bd387-114">Elements and attributes</span></span>

<span data-ttu-id="bd387-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="bd387-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bd387-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bd387-116">Parent elements</span></span>

|<span data-ttu-id="bd387-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="bd387-117">**Element**</span></span>|<span data-ttu-id="bd387-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="bd387-118">**Type**</span></span>|<span data-ttu-id="bd387-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd387-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bd387-120">Problème</span><span class="sxs-lookup"><span data-stu-id="bd387-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bd387-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="bd387-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bd387-122">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="bd387-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bd387-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bd387-123">Child elements</span></span>

<span data-ttu-id="bd387-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bd387-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd387-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="bd387-125">Attributes</span></span>

|<span data-ttu-id="bd387-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bd387-126">**Attribute**</span></span>|<span data-ttu-id="bd387-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="bd387-127">**Type**</span></span>|<span data-ttu-id="bd387-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="bd387-128">**Required**</span></span>|<span data-ttu-id="bd387-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd387-129">**Description**</span></span>|<span data-ttu-id="bd387-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="bd387-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd387-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="bd387-131">RuleID</span></span>  <br/> |<span data-ttu-id="bd387-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd387-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd387-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="bd387-133">required</span></span>  <br/> |<span data-ttu-id="bd387-134">Spécifie l’identificateur unique de la règle de validation à qui appartient le problème parent.</span><span class="sxs-lookup"><span data-stu-id="bd387-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="bd387-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd387-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd387-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="bd387-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="bd387-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd387-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd387-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="bd387-138">required</span></span>  <br/> |<span data-ttu-id="bd387-139">Spécifie l’identificateur unique de l’ensemble de règles de validation à qui appartient le problème parent.</span><span class="sxs-lookup"><span data-stu-id="bd387-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="bd387-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd387-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

