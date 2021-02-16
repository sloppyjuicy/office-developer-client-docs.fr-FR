---
title: Élément IssueTarget (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Selon la cible du problème de validation parent, spécifie la page, ou la page et la forme, associées au problème de validation parent. Si la cible du problème de validation parent est un document, IssueTarget ne spécule ni une page, ni une forme.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542953"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="7e8b1-104">Élément IssueTarget (Issue_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7e8b1-104">IssueTarget element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7e8b1-105">Selon la cible du problème de validation parent, spécifie la page, ou la page et la forme, associées au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="7e8b1-106">Si la cible du problème de validation parent est un document, **IssueTarget** ne spécule ni une page, ni une forme.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7e8b1-107">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="7e8b1-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e8b1-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-108">**Element type**</span></span> <br/> |[<span data-ttu-id="7e8b1-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="7e8b1-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7e8b1-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7e8b1-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-111">**Schema file**</span></span> <br/> |<span data-ttu-id="7e8b1-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7e8b1-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7e8b1-113">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-113">**Document parts**</span></span> <br/> |<span data-ttu-id="7e8b1-114">validation.xml</span><span class="sxs-lookup"><span data-stu-id="7e8b1-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7e8b1-115">Définition</span><span class="sxs-lookup"><span data-stu-id="7e8b1-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7e8b1-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7e8b1-116">Elements and attributes</span></span>

<span data-ttu-id="7e8b1-117">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7e8b1-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7e8b1-118">Parent elements</span></span>

|<span data-ttu-id="7e8b1-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-119">**Element**</span></span>|<span data-ttu-id="7e8b1-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-120">**Type**</span></span>|<span data-ttu-id="7e8b1-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e8b1-122">Problème</span><span class="sxs-lookup"><span data-stu-id="7e8b1-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7e8b1-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="7e8b1-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7e8b1-124">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7e8b1-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7e8b1-125">Child elements</span></span>

<span data-ttu-id="7e8b1-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e8b1-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="7e8b1-127">Attributes</span></span>

|<span data-ttu-id="7e8b1-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-128">**Attribute**</span></span>|<span data-ttu-id="7e8b1-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-129">**Type**</span></span>|<span data-ttu-id="7e8b1-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-130">**Required**</span></span>|<span data-ttu-id="7e8b1-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-131">**Description**</span></span>|<span data-ttu-id="7e8b1-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7e8b1-133">PageID</span><span class="sxs-lookup"><span data-stu-id="7e8b1-133">PageID</span></span>  <br/> |<span data-ttu-id="7e8b1-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7e8b1-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7e8b1-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7e8b1-135">required</span></span>  <br/> |<span data-ttu-id="7e8b1-136">Spécifie l’identificateur unique de la page associée au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="7e8b1-137">Si la cible est le document, la valeur PageID peut être 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="7e8b1-138">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7e8b1-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="7e8b1-139">ShapeID</span></span>  <br/> |<span data-ttu-id="7e8b1-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7e8b1-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7e8b1-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7e8b1-141">required</span></span>  <br/> |<span data-ttu-id="7e8b1-142">Spécifie l’identificateur unique de la forme associée au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="7e8b1-143">Si la cible est le document ou une page, la valeur ShapeID peut être 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="7e8b1-144">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

