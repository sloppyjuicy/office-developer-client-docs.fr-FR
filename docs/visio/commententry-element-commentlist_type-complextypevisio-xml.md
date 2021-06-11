---
title: Élément CommentEntry (CommentList_Type complexType) (Visio XML)
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
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="210e0-103">Élément CommentEntry (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="210e0-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="210e0-104">Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="210e0-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="210e0-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="210e0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="210e0-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="210e0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="210e0-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="210e0-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="210e0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="210e0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="210e0-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="210e0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="210e0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="210e0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="210e0-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="210e0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="210e0-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="210e0-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="210e0-113">Définition</span><span class="sxs-lookup"><span data-stu-id="210e0-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="210e0-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="210e0-114">Elements and attributes</span></span>

<span data-ttu-id="210e0-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="210e0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="210e0-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="210e0-116">Parent elements</span></span>

|<span data-ttu-id="210e0-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="210e0-117">**Element**</span></span>|<span data-ttu-id="210e0-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="210e0-118">**Type**</span></span>|<span data-ttu-id="210e0-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="210e0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="210e0-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="210e0-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="210e0-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="210e0-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="210e0-122">Spécifie les commentaires d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="210e0-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="210e0-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="210e0-123">Child elements</span></span>

<span data-ttu-id="210e0-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="210e0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="210e0-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="210e0-125">Attributes</span></span>

|<span data-ttu-id="210e0-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="210e0-126">**Attribute**</span></span>|<span data-ttu-id="210e0-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="210e0-127">**Type**</span></span>|<span data-ttu-id="210e0-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="210e0-128">**Required**</span></span>|<span data-ttu-id="210e0-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="210e0-129">**Description**</span></span>|<span data-ttu-id="210e0-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="210e0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="210e0-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="210e0-131">AuthorID</span></span>  <br/> |<span data-ttu-id="210e0-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="210e0-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="210e0-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="210e0-133">required</span></span>  <br/> |<span data-ttu-id="210e0-134">Valeur basée sur une valeur qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="210e0-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="210e0-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="210e0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="210e0-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="210e0-136">CommentID</span></span>  <br/> |<span data-ttu-id="210e0-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="210e0-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="210e0-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="210e0-138">required</span></span>  <br/> |<span data-ttu-id="210e0-139">Valeur unique qui identifie le commentaire dans une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="210e0-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="210e0-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="210e0-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="210e0-141">Date</span><span class="sxs-lookup"><span data-stu-id="210e0-141">Date</span></span>  <br/> |<span data-ttu-id="210e0-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="210e0-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="210e0-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="210e0-143">required</span></span>  <br/> |<span data-ttu-id="210e0-144">Indique quand un commentaire a été créé.</span><span class="sxs-lookup"><span data-stu-id="210e0-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="210e0-145">Valeurs du type xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="210e0-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="210e0-146">Terminé</span><span class="sxs-lookup"><span data-stu-id="210e0-146">Done</span></span>  <br/> |<span data-ttu-id="210e0-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="210e0-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="210e0-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="210e0-148">optional</span></span>  <br/> |<span data-ttu-id="210e0-149">Spécifie l’état actuel du commentaire.</span><span class="sxs-lookup"><span data-stu-id="210e0-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="210e0-150">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="210e0-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="210e0-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="210e0-151">EditDate</span></span>  <br/> |<span data-ttu-id="210e0-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="210e0-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="210e0-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="210e0-153">optional</span></span>  <br/> |<span data-ttu-id="210e0-154">Indique quand un commentaire a été modifié pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="210e0-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="210e0-155">Valeurs du type xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="210e0-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="210e0-156">PageID</span><span class="sxs-lookup"><span data-stu-id="210e0-156">PageID</span></span>  <br/> |<span data-ttu-id="210e0-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="210e0-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="210e0-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="210e0-158">required</span></span>  <br/> |<span data-ttu-id="210e0-159">Valeur qui identifie la page de dessin où se trouve le commentaire.</span><span class="sxs-lookup"><span data-stu-id="210e0-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="210e0-160">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="210e0-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="210e0-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="210e0-161">ShapeID</span></span>  <br/> |<span data-ttu-id="210e0-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="210e0-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="210e0-163">facultatif</span><span class="sxs-lookup"><span data-stu-id="210e0-163">optional</span></span>  <br/> |<span data-ttu-id="210e0-164">Valeur qui identifie la forme sur quelle forme se trouve le commentaire.</span><span class="sxs-lookup"><span data-stu-id="210e0-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="210e0-165">Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="210e0-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="210e0-166">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="210e0-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

