---
title: Élément RuleInfo (complexType Issue_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541686"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="27081-103">Élément RuleInfo (complexType Issue_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="27081-103">RuleInfo element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="27081-104">Fournit des informations sur la règle de validation à laquelle appartient le problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="27081-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27081-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="27081-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27081-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="27081-106">**Element type**</span></span> <br/> |[<span data-ttu-id="27081-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="27081-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="27081-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="27081-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="27081-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="27081-109">**Schema file**</span></span> <br/> |<span data-ttu-id="27081-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="27081-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="27081-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="27081-111">**Document parts**</span></span> <br/> |<span data-ttu-id="27081-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="27081-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27081-113">Définition</span><span class="sxs-lookup"><span data-stu-id="27081-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="27081-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="27081-114">Elements and attributes</span></span>

<span data-ttu-id="27081-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="27081-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="27081-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="27081-116">Parent elements</span></span>

|<span data-ttu-id="27081-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="27081-117">**Element**</span></span>|<span data-ttu-id="27081-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="27081-118">**Type**</span></span>|<span data-ttu-id="27081-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="27081-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27081-120">Problème</span><span class="sxs-lookup"><span data-stu-id="27081-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="27081-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="27081-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="27081-122">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="27081-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="27081-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="27081-123">Child elements</span></span>

<span data-ttu-id="27081-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="27081-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27081-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="27081-125">Attributes</span></span>

|<span data-ttu-id="27081-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="27081-126">**Attribute**</span></span>|<span data-ttu-id="27081-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="27081-127">**Type**</span></span>|<span data-ttu-id="27081-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="27081-128">**Required**</span></span>|<span data-ttu-id="27081-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="27081-129">**Description**</span></span>|<span data-ttu-id="27081-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="27081-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="27081-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="27081-131">RuleID</span></span>  <br/> |<span data-ttu-id="27081-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="27081-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="27081-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="27081-133">required</span></span>  <br/> |<span data-ttu-id="27081-134">Spécifie l’identificateur unique de la règle de validation à laquelle le problème parent est lié.</span><span class="sxs-lookup"><span data-stu-id="27081-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="27081-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="27081-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="27081-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="27081-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="27081-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="27081-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="27081-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="27081-138">required</span></span>  <br/> |<span data-ttu-id="27081-139">Spécifie l’identificateur unique de l’ensemble de règles de validation auquel le problème parent se rapporte.</span><span class="sxs-lookup"><span data-stu-id="27081-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="27081-140">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="27081-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

