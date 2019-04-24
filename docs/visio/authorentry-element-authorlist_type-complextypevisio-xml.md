---
title: Élément AuthorEntry (complexType AuthorList_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Spécifie les propriétés utilisées pour identifier l'auteur d'un commentaire dans un dessin.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338625"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="f3436-103">Élément AuthorEntry (complexType AuthorList_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f3436-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f3436-104">Spécifie les propriétés utilisées pour identifier l'auteur d'un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="f3436-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3436-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="f3436-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3436-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="f3436-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f3436-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="f3436-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f3436-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f3436-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f3436-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f3436-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f3436-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f3436-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f3436-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="f3436-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f3436-112">Comments. Xml</span><span class="sxs-lookup"><span data-stu-id="f3436-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3436-113">Définition</span><span class="sxs-lookup"><span data-stu-id="f3436-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f3436-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f3436-114">Elements and attributes</span></span>

<span data-ttu-id="f3436-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="f3436-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f3436-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f3436-116">Parent elements</span></span>

|<span data-ttu-id="f3436-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f3436-117">**Element**</span></span>|<span data-ttu-id="f3436-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="f3436-118">**Type**</span></span>|<span data-ttu-id="f3436-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="f3436-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f3436-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="f3436-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3436-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="f3436-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f3436-122">Spécifie les auteurs d'un dessin.</span><span class="sxs-lookup"><span data-stu-id="f3436-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f3436-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f3436-123">Child elements</span></span>

<span data-ttu-id="f3436-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f3436-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3436-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="f3436-125">Attributes</span></span>

|<span data-ttu-id="f3436-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f3436-126">**Attribute**</span></span>|<span data-ttu-id="f3436-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="f3436-127">**Type**</span></span>|<span data-ttu-id="f3436-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f3436-128">**Required**</span></span>|<span data-ttu-id="f3436-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="f3436-129">**Description**</span></span>|<span data-ttu-id="f3436-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3436-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3436-131">ID</span><span class="sxs-lookup"><span data-stu-id="f3436-131">ID</span></span>  <br/> |<span data-ttu-id="f3436-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3436-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3436-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f3436-133">required</span></span>  <br/> |<span data-ttu-id="f3436-134">Une valeur basée sur un qui identifie l'auteur.</span><span class="sxs-lookup"><span data-stu-id="f3436-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="f3436-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3436-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3436-136">Initiales</span><span class="sxs-lookup"><span data-stu-id="f3436-136">Initials</span></span>  <br/> |<span data-ttu-id="f3436-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3436-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f3436-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="f3436-138">optional</span></span>  <br/> |<span data-ttu-id="f3436-139">Initiales de l'auteur.</span><span class="sxs-lookup"><span data-stu-id="f3436-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="f3436-140">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3436-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3436-141">Nom</span><span class="sxs-lookup"><span data-stu-id="f3436-141">Name</span></span>  <br/> |<span data-ttu-id="f3436-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3436-142">xsd:string</span></span>  <br/> |<span data-ttu-id="f3436-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="f3436-143">optional</span></span>  <br/> |<span data-ttu-id="f3436-144">Nom de l'auteur.</span><span class="sxs-lookup"><span data-stu-id="f3436-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="f3436-145">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3436-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3436-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="f3436-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="f3436-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f3436-147">xsd:string</span></span>  <br/> |<span data-ttu-id="f3436-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="f3436-148">optional</span></span>  <br/> |<span data-ttu-id="f3436-149">Identificateur unique de l'auteur.</span><span class="sxs-lookup"><span data-stu-id="f3436-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="f3436-150">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3436-150">Values of the xsd:string type.</span></span>  <br/> |
   

