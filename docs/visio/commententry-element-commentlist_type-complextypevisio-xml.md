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
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="89ac1-103">Élément CommentEntry (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="89ac1-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="89ac1-104">Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="89ac1-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89ac1-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="89ac1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89ac1-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="89ac1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="89ac1-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="89ac1-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="89ac1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="89ac1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="89ac1-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="89ac1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="89ac1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="89ac1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="89ac1-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="89ac1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="89ac1-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="89ac1-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="89ac1-113">Définition</span><span class="sxs-lookup"><span data-stu-id="89ac1-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="89ac1-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="89ac1-114">Elements and attributes</span></span>

<span data-ttu-id="89ac1-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="89ac1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="89ac1-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="89ac1-116">Parent elements</span></span>

|<span data-ttu-id="89ac1-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="89ac1-117">**Element**</span></span>|<span data-ttu-id="89ac1-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="89ac1-118">**Type**</span></span>|<span data-ttu-id="89ac1-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="89ac1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="89ac1-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="89ac1-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="89ac1-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="89ac1-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="89ac1-122">Spécifie les commentaires d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="89ac1-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="89ac1-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="89ac1-123">Child elements</span></span>

<span data-ttu-id="89ac1-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="89ac1-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89ac1-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="89ac1-125">Attributes</span></span>

|<span data-ttu-id="89ac1-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="89ac1-126">**Attribute**</span></span>|<span data-ttu-id="89ac1-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="89ac1-127">**Type**</span></span>|<span data-ttu-id="89ac1-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="89ac1-128">**Required**</span></span>|<span data-ttu-id="89ac1-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="89ac1-129">**Description**</span></span>|<span data-ttu-id="89ac1-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="89ac1-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="89ac1-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="89ac1-131">AuthorID</span></span>  <br/> |<span data-ttu-id="89ac1-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="89ac1-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="89ac1-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="89ac1-133">required</span></span>  <br/> |<span data-ttu-id="89ac1-134">Valeur basée sur un qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="89ac1-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="89ac1-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="89ac1-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="89ac1-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="89ac1-136">CommentID</span></span>  <br/> |<span data-ttu-id="89ac1-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="89ac1-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="89ac1-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="89ac1-138">required</span></span>  <br/> |<span data-ttu-id="89ac1-139">Valeur unique qui identifie le commentaire dans une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="89ac1-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="89ac1-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="89ac1-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="89ac1-141">Date</span><span class="sxs-lookup"><span data-stu-id="89ac1-141">Date</span></span>  <br/> |<span data-ttu-id="89ac1-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="89ac1-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="89ac1-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="89ac1-143">required</span></span>  <br/> |<span data-ttu-id="89ac1-144">Indique quand un commentaire a été créé.</span><span class="sxs-lookup"><span data-stu-id="89ac1-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="89ac1-145">Valeurs du type xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="89ac1-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="89ac1-146">Terminé</span><span class="sxs-lookup"><span data-stu-id="89ac1-146">Done</span></span>  <br/> |<span data-ttu-id="89ac1-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="89ac1-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="89ac1-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="89ac1-148">optional</span></span>  <br/> |<span data-ttu-id="89ac1-149">Spécifie l’état actuel du commentaire.</span><span class="sxs-lookup"><span data-stu-id="89ac1-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="89ac1-150">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="89ac1-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="89ac1-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="89ac1-151">EditDate</span></span>  <br/> |<span data-ttu-id="89ac1-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="89ac1-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="89ac1-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="89ac1-153">optional</span></span>  <br/> |<span data-ttu-id="89ac1-154">Indique quand un commentaire a été modifié pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="89ac1-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="89ac1-155">Valeurs du type xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="89ac1-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="89ac1-156">PageID</span><span class="sxs-lookup"><span data-stu-id="89ac1-156">PageID</span></span>  <br/> |<span data-ttu-id="89ac1-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="89ac1-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="89ac1-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="89ac1-158">required</span></span>  <br/> |<span data-ttu-id="89ac1-159">Valeur qui identifie la page de dessin sur qui se trouve le commentaire.</span><span class="sxs-lookup"><span data-stu-id="89ac1-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="89ac1-160">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="89ac1-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="89ac1-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="89ac1-161">ShapeID</span></span>  <br/> |<span data-ttu-id="89ac1-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="89ac1-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="89ac1-163">facultatif</span><span class="sxs-lookup"><span data-stu-id="89ac1-163">optional</span></span>  <br/> |<span data-ttu-id="89ac1-164">Valeur qui identifie la forme sur quelle forme se trouve le commentaire.</span><span class="sxs-lookup"><span data-stu-id="89ac1-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="89ac1-165">Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="89ac1-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="89ac1-166">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="89ac1-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

