---
title: Élément IssueTarget (Issue_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: En fonction de la cible de l’objet parent de validation, spécifie soit la page, ou la page et la forme, associé à ce problème de validation parent. Si la cible de la publication de validation parent est un document IssueTarget spécifie une page ni une forme.
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385360"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="e2f93-104">Élément IssueTarget (Issue_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e2f93-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e2f93-105">En fonction de la cible de l’objet parent de validation, spécifie soit la page, ou la page et la forme, associé à ce problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="e2f93-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="e2f93-106">Si la cible de la publication de validation parent est un document **IssueTarget** spécifie une page ni une forme.</span><span class="sxs-lookup"><span data-stu-id="e2f93-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e2f93-107">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="e2f93-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2f93-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e2f93-108">**Element type**</span></span> <br/> |[<span data-ttu-id="e2f93-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="e2f93-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e2f93-110">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e2f93-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e2f93-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e2f93-111">**Schema file**</span></span> <br/> |<span data-ttu-id="e2f93-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e2f93-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e2f93-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e2f93-113">**Document parts**</span></span> <br/> |<span data-ttu-id="e2f93-114">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="e2f93-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e2f93-115">Définition</span><span class="sxs-lookup"><span data-stu-id="e2f93-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e2f93-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e2f93-116">Elements and attributes</span></span>

<span data-ttu-id="e2f93-117">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e2f93-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e2f93-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e2f93-118">Parent elements</span></span>

|<span data-ttu-id="e2f93-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e2f93-119">**Element**</span></span>|<span data-ttu-id="e2f93-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="e2f93-120">**Type**</span></span>|<span data-ttu-id="e2f93-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2f93-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2f93-122">Problème</span><span class="sxs-lookup"><span data-stu-id="e2f93-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2f93-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="e2f93-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2f93-124">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="e2f93-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2f93-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e2f93-125">Child elements</span></span>

<span data-ttu-id="e2f93-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e2f93-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2f93-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="e2f93-127">Attributes</span></span>

|<span data-ttu-id="e2f93-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e2f93-128">**Attribute**</span></span>|<span data-ttu-id="e2f93-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="e2f93-129">**Type**</span></span>|<span data-ttu-id="e2f93-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e2f93-130">**Required**</span></span>|<span data-ttu-id="e2f93-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2f93-131">**Description**</span></span>|<span data-ttu-id="e2f93-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e2f93-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2f93-133">PageID</span><span class="sxs-lookup"><span data-stu-id="e2f93-133">PageID</span></span>  <br/> |<span data-ttu-id="e2f93-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e2f93-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e2f93-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e2f93-135">required</span></span>  <br/> |<span data-ttu-id="e2f93-136">Spécifie l’identificateur unique de la page qui est associée au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="e2f93-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="e2f93-137">Si la cible est le document, la valeur PageID peut être 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="e2f93-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="e2f93-138">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e2f93-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e2f93-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="e2f93-139">ShapeID</span></span>  <br/> |<span data-ttu-id="e2f93-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e2f93-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e2f93-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e2f93-141">required</span></span>  <br/> |<span data-ttu-id="e2f93-142">Spécifie l’identificateur unique de la forme qui est associée au problème de validation parent.</span><span class="sxs-lookup"><span data-stu-id="e2f93-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="e2f93-143">Si la cible est le document ou une page, la valeur ShapeID peut être 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="e2f93-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="e2f93-144">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e2f93-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

