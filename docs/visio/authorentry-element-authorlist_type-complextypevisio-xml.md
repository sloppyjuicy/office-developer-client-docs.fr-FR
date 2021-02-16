---
title: Élément AuthorEntry (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537905"
---
# <a name="authorentry-element-authorlist_type-complextype-visio-xml"></a><span data-ttu-id="e50be-103">Élément AuthorEntry (AuthorList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e50be-103">AuthorEntry element (AuthorList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e50be-104">Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="e50be-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e50be-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="e50be-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e50be-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e50be-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e50be-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="e50be-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e50be-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e50be-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e50be-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e50be-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e50be-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e50be-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e50be-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="e50be-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e50be-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="e50be-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e50be-113">Définition</span><span class="sxs-lookup"><span data-stu-id="e50be-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e50be-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e50be-114">Elements and attributes</span></span>

<span data-ttu-id="e50be-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="e50be-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e50be-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e50be-116">Parent elements</span></span>

|<span data-ttu-id="e50be-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e50be-117">**Element**</span></span>|<span data-ttu-id="e50be-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="e50be-118">**Type**</span></span>|<span data-ttu-id="e50be-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e50be-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e50be-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="e50be-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e50be-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="e50be-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e50be-122">Spécifie les auteurs d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="e50be-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e50be-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e50be-123">Child elements</span></span>

<span data-ttu-id="e50be-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e50be-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e50be-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="e50be-125">Attributes</span></span>

|<span data-ttu-id="e50be-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e50be-126">**Attribute**</span></span>|<span data-ttu-id="e50be-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="e50be-127">**Type**</span></span>|<span data-ttu-id="e50be-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e50be-128">**Required**</span></span>|<span data-ttu-id="e50be-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="e50be-129">**Description**</span></span>|<span data-ttu-id="e50be-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e50be-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e50be-131">ID</span><span class="sxs-lookup"><span data-stu-id="e50be-131">ID</span></span>  <br/> |<span data-ttu-id="e50be-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e50be-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e50be-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e50be-133">required</span></span>  <br/> |<span data-ttu-id="e50be-134">Valeur basée sur un qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="e50be-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="e50be-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e50be-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e50be-136">Initials</span><span class="sxs-lookup"><span data-stu-id="e50be-136">Initials</span></span>  <br/> |<span data-ttu-id="e50be-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e50be-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e50be-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="e50be-138">optional</span></span>  <br/> |<span data-ttu-id="e50be-139">Initiales de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="e50be-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="e50be-140">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e50be-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e50be-141">Nom</span><span class="sxs-lookup"><span data-stu-id="e50be-141">Name</span></span>  <br/> |<span data-ttu-id="e50be-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e50be-142">xsd:string</span></span>  <br/> |<span data-ttu-id="e50be-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="e50be-143">optional</span></span>  <br/> |<span data-ttu-id="e50be-144">Nom de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="e50be-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="e50be-145">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e50be-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e50be-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="e50be-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="e50be-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e50be-147">xsd:string</span></span>  <br/> |<span data-ttu-id="e50be-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="e50be-148">optional</span></span>  <br/> |<span data-ttu-id="e50be-149">Identificateur unique de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="e50be-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="e50be-150">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e50be-150">Values of the xsd:string type.</span></span>  <br/> |
   

