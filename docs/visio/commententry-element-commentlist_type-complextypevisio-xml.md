---
title: Élément CommentEntry (complexType CommentList_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540111"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="a8078-103">Élément CommentEntry (complexType CommentList_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="a8078-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a8078-104">Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="a8078-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8078-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a8078-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8078-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a8078-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a8078-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="a8078-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a8078-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a8078-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a8078-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a8078-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a8078-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a8078-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a8078-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="a8078-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a8078-112">Comments. Xml</span><span class="sxs-lookup"><span data-stu-id="a8078-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8078-113">Définition</span><span class="sxs-lookup"><span data-stu-id="a8078-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8078-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a8078-114">Elements and attributes</span></span>

<span data-ttu-id="a8078-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a8078-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a8078-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a8078-116">Parent elements</span></span>

|<span data-ttu-id="a8078-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a8078-117">**Element**</span></span>|<span data-ttu-id="a8078-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8078-118">**Type**</span></span>|<span data-ttu-id="a8078-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8078-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8078-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="a8078-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a8078-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="a8078-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8078-122">Cette énumération spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="a8078-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a8078-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8078-123">Child elements</span></span>

<span data-ttu-id="a8078-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a8078-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8078-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8078-125">Attributes</span></span>

|<span data-ttu-id="a8078-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a8078-126">**Attribute**</span></span>|<span data-ttu-id="a8078-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8078-127">**Type**</span></span>|<span data-ttu-id="a8078-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a8078-128">**Required**</span></span>|<span data-ttu-id="a8078-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8078-129">**Description**</span></span>|<span data-ttu-id="a8078-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a8078-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8078-131">Faut</span><span class="sxs-lookup"><span data-stu-id="a8078-131">AuthorID</span></span>  <br/> |<span data-ttu-id="a8078-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8078-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8078-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8078-133">required</span></span>  <br/> |<span data-ttu-id="a8078-134">Une valeur basée sur un qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="a8078-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="a8078-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8078-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8078-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="a8078-136">CommentID</span></span>  <br/> |<span data-ttu-id="a8078-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8078-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8078-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8078-138">required</span></span>  <br/> |<span data-ttu-id="a8078-139">Valeur unique qui identifie le commentaire dans une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="a8078-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="a8078-140">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8078-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8078-141">Date</span><span class="sxs-lookup"><span data-stu-id="a8078-141">Date</span></span>  <br/> |<span data-ttu-id="a8078-142">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="a8078-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="a8078-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8078-143">required</span></span>  <br/> |<span data-ttu-id="a8078-144">Indique la date de création d’un commentaire.</span><span class="sxs-lookup"><span data-stu-id="a8078-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="a8078-145">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="a8078-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="a8078-146">Terminé</span><span class="sxs-lookup"><span data-stu-id="a8078-146">Done</span></span>  <br/> |<span data-ttu-id="a8078-147">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="a8078-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a8078-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8078-148">optional</span></span>  <br/> |<span data-ttu-id="a8078-149">Spécifie l’état actuel du commentaire.</span><span class="sxs-lookup"><span data-stu-id="a8078-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="a8078-150">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a8078-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a8078-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="a8078-151">EditDate</span></span>  <br/> |<span data-ttu-id="a8078-152">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="a8078-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="a8078-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8078-153">optional</span></span>  <br/> |<span data-ttu-id="a8078-154">Indique la date de la dernière modification d’un commentaire.</span><span class="sxs-lookup"><span data-stu-id="a8078-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="a8078-155">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="a8078-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="a8078-156">PageID</span><span class="sxs-lookup"><span data-stu-id="a8078-156">PageID</span></span>  <br/> |<span data-ttu-id="a8078-157">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8078-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8078-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8078-158">required</span></span>  <br/> |<span data-ttu-id="a8078-159">Valeur qui identifie la page de dessin sur laquelle se trouve le commentaire.</span><span class="sxs-lookup"><span data-stu-id="a8078-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="a8078-160">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8078-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8078-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="a8078-161">ShapeID</span></span>  <br/> |<span data-ttu-id="a8078-162">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8078-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8078-163">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8078-163">optional</span></span>  <br/> |<span data-ttu-id="a8078-164">Valeur qui identifie la forme sur laquelle le commentaire est activé.</span><span class="sxs-lookup"><span data-stu-id="a8078-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="a8078-165">Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="a8078-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="a8078-166">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8078-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

