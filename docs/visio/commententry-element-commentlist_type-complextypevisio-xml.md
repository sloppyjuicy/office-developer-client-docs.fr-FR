---
title: Élément CommentEntry (CommentList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Spécifie les propriétés permettant d’identifier un commentaire dans un dessin.
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788289"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="e9af8-103">Élément CommentEntry (CommentList_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e9af8-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e9af8-104">Spécifie les propriétés permettant d’identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="e9af8-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9af8-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="e9af8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9af8-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e9af8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e9af8-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="e9af8-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e9af8-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e9af8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e9af8-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e9af8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e9af8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e9af8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e9af8-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e9af8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e9af8-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="e9af8-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e9af8-113">Définition</span><span class="sxs-lookup"><span data-stu-id="e9af8-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e9af8-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e9af8-114">Elements and attributes</span></span>

<span data-ttu-id="e9af8-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e9af8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e9af8-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e9af8-116">Parent elements</span></span>

|<span data-ttu-id="e9af8-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e9af8-117">**Element**</span></span>|<span data-ttu-id="e9af8-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="e9af8-118">**Type**</span></span>|<span data-ttu-id="e9af8-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e9af8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e9af8-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="e9af8-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9af8-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="e9af8-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e9af8-122">Spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="e9af8-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e9af8-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e9af8-123">Child elements</span></span>

<span data-ttu-id="e9af8-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e9af8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9af8-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="e9af8-125">Attributes</span></span>

|<span data-ttu-id="e9af8-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e9af8-126">**Attribute**</span></span>|<span data-ttu-id="e9af8-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="e9af8-127">**Type**</span></span>|<span data-ttu-id="e9af8-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e9af8-128">**Required**</span></span>|<span data-ttu-id="e9af8-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="e9af8-129">**Description**</span></span>|<span data-ttu-id="e9af8-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e9af8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9af8-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="e9af8-131">AuthorID</span></span>  <br/> |<span data-ttu-id="e9af8-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9af8-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9af8-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e9af8-133">required</span></span>  <br/> |<span data-ttu-id="e9af8-134">Une valeur de base 1 qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="e9af8-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="e9af8-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9af8-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9af8-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="e9af8-136">CommentID</span></span>  <br/> |<span data-ttu-id="e9af8-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9af8-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9af8-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e9af8-138">required</span></span>  <br/> |<span data-ttu-id="e9af8-139">Valeur unique qui identifie le commentaire dans une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="e9af8-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="e9af8-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9af8-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9af8-141">Date</span><span class="sxs-lookup"><span data-stu-id="e9af8-141">Date</span></span>  <br/> |<span data-ttu-id="e9af8-142">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="e9af8-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="e9af8-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e9af8-143">required</span></span>  <br/> |<span data-ttu-id="e9af8-144">Spécifie si un commentaire a été créé.</span><span class="sxs-lookup"><span data-stu-id="e9af8-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="e9af8-145">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="e9af8-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="e9af8-146">Terminé</span><span class="sxs-lookup"><span data-stu-id="e9af8-146">Done</span></span>  <br/> |<span data-ttu-id="e9af8-147">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="e9af8-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e9af8-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="e9af8-148">optional</span></span>  <br/> |<span data-ttu-id="e9af8-149">Spécifie l’état actuel du commentaire.</span><span class="sxs-lookup"><span data-stu-id="e9af8-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="e9af8-150">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="e9af8-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e9af8-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="e9af8-151">EditDate</span></span>  <br/> |<span data-ttu-id="e9af8-152">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="e9af8-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="e9af8-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="e9af8-153">optional</span></span>  <br/> |<span data-ttu-id="e9af8-154">Spécifie si un commentaire a été modifié pour la dernière.</span><span class="sxs-lookup"><span data-stu-id="e9af8-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="e9af8-155">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="e9af8-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="e9af8-156">PageID</span><span class="sxs-lookup"><span data-stu-id="e9af8-156">PageID</span></span>  <br/> |<span data-ttu-id="e9af8-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9af8-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9af8-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e9af8-158">required</span></span>  <br/> |<span data-ttu-id="e9af8-159">Une valeur qui identifie la page de dessin le commentaire est activé.</span><span class="sxs-lookup"><span data-stu-id="e9af8-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="e9af8-160">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9af8-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9af8-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="e9af8-161">ShapeID</span></span>  <br/> |<span data-ttu-id="e9af8-162">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9af8-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9af8-163">facultatif</span><span class="sxs-lookup"><span data-stu-id="e9af8-163">optional</span></span>  <br/> |<span data-ttu-id="e9af8-164">Une valeur qui identifie la forme le commentaire est sur.</span><span class="sxs-lookup"><span data-stu-id="e9af8-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="e9af8-165">Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="e9af8-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="e9af8-166">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9af8-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

