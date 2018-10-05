---
title: Élément CommentEntry (CommentList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Spécifie les propriétés permettant d’identifier un commentaire dans un dessin.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397043"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="8a4de-103">Élément CommentEntry (CommentList_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="8a4de-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8a4de-104">Spécifie les propriétés permettant d’identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="8a4de-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a4de-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="8a4de-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a4de-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="8a4de-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8a4de-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="8a4de-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8a4de-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="8a4de-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8a4de-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="8a4de-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8a4de-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8a4de-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8a4de-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="8a4de-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8a4de-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="8a4de-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8a4de-113">Définition</span><span class="sxs-lookup"><span data-stu-id="8a4de-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8a4de-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="8a4de-114">Elements and attributes</span></span>

<span data-ttu-id="8a4de-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="8a4de-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8a4de-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8a4de-116">Parent elements</span></span>

|<span data-ttu-id="8a4de-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8a4de-117">**Element**</span></span>|<span data-ttu-id="8a4de-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="8a4de-118">**Type**</span></span>|<span data-ttu-id="8a4de-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a4de-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8a4de-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="8a4de-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a4de-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="8a4de-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a4de-122">Spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="8a4de-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8a4de-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8a4de-123">Child elements</span></span>

<span data-ttu-id="8a4de-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8a4de-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a4de-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="8a4de-125">Attributes</span></span>

|<span data-ttu-id="8a4de-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8a4de-126">**Attribute**</span></span>|<span data-ttu-id="8a4de-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="8a4de-127">**Type**</span></span>|<span data-ttu-id="8a4de-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8a4de-128">**Required**</span></span>|<span data-ttu-id="8a4de-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a4de-129">**Description**</span></span>|<span data-ttu-id="8a4de-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a4de-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8a4de-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="8a4de-131">AuthorID</span></span>  <br/> |<span data-ttu-id="8a4de-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a4de-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a4de-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8a4de-133">required</span></span>  <br/> |<span data-ttu-id="8a4de-134">Une valeur de base 1 qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="8a4de-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="8a4de-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a4de-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8a4de-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="8a4de-136">CommentID</span></span>  <br/> |<span data-ttu-id="8a4de-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a4de-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a4de-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8a4de-138">required</span></span>  <br/> |<span data-ttu-id="8a4de-139">Valeur unique qui identifie le commentaire dans une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="8a4de-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="8a4de-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a4de-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8a4de-141">Date</span><span class="sxs-lookup"><span data-stu-id="8a4de-141">Date</span></span>  <br/> |<span data-ttu-id="8a4de-142">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="8a4de-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="8a4de-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8a4de-143">required</span></span>  <br/> |<span data-ttu-id="8a4de-144">Spécifie si un commentaire a été créé.</span><span class="sxs-lookup"><span data-stu-id="8a4de-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="8a4de-145">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="8a4de-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="8a4de-146">Terminé</span><span class="sxs-lookup"><span data-stu-id="8a4de-146">Done</span></span>  <br/> |<span data-ttu-id="8a4de-147">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="8a4de-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8a4de-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="8a4de-148">optional</span></span>  <br/> |<span data-ttu-id="8a4de-149">Spécifie l’état actuel du commentaire.</span><span class="sxs-lookup"><span data-stu-id="8a4de-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="8a4de-150">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="8a4de-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8a4de-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="8a4de-151">EditDate</span></span>  <br/> |<span data-ttu-id="8a4de-152">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="8a4de-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="8a4de-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="8a4de-153">optional</span></span>  <br/> |<span data-ttu-id="8a4de-154">Spécifie si un commentaire a été modifié pour la dernière.</span><span class="sxs-lookup"><span data-stu-id="8a4de-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="8a4de-155">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="8a4de-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="8a4de-156">PageID</span><span class="sxs-lookup"><span data-stu-id="8a4de-156">PageID</span></span>  <br/> |<span data-ttu-id="8a4de-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a4de-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a4de-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8a4de-158">required</span></span>  <br/> |<span data-ttu-id="8a4de-159">Une valeur qui identifie la page de dessin le commentaire est activé.</span><span class="sxs-lookup"><span data-stu-id="8a4de-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="8a4de-160">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a4de-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8a4de-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="8a4de-161">ShapeID</span></span>  <br/> |<span data-ttu-id="8a4de-162">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a4de-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a4de-163">facultatif</span><span class="sxs-lookup"><span data-stu-id="8a4de-163">optional</span></span>  <br/> |<span data-ttu-id="8a4de-164">Une valeur qui identifie la forme le commentaire est sur.</span><span class="sxs-lookup"><span data-stu-id="8a4de-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="8a4de-165">Si aucun ShapeID n’est spécifié, le commentaire fait référence à la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="8a4de-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="8a4de-166">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a4de-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

