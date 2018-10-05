---
title: Élément AuthorEntry (AuthorList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386329"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="22dbf-103">Élément AuthorEntry (AuthorList_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="22dbf-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="22dbf-104">Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="22dbf-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22dbf-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="22dbf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22dbf-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="22dbf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="22dbf-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="22dbf-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="22dbf-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="22dbf-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="22dbf-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="22dbf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="22dbf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="22dbf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="22dbf-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="22dbf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="22dbf-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="22dbf-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="22dbf-113">Définition</span><span class="sxs-lookup"><span data-stu-id="22dbf-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="22dbf-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="22dbf-114">Elements and attributes</span></span>

<span data-ttu-id="22dbf-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="22dbf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="22dbf-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="22dbf-116">Parent elements</span></span>

|<span data-ttu-id="22dbf-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="22dbf-117">**Element**</span></span>|<span data-ttu-id="22dbf-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="22dbf-118">**Type**</span></span>|<span data-ttu-id="22dbf-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="22dbf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="22dbf-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="22dbf-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="22dbf-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="22dbf-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22dbf-122">Spécifie les auteurs dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="22dbf-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="22dbf-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="22dbf-123">Child elements</span></span>

<span data-ttu-id="22dbf-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="22dbf-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22dbf-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="22dbf-125">Attributes</span></span>

|<span data-ttu-id="22dbf-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="22dbf-126">**Attribute**</span></span>|<span data-ttu-id="22dbf-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="22dbf-127">**Type**</span></span>|<span data-ttu-id="22dbf-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="22dbf-128">**Required**</span></span>|<span data-ttu-id="22dbf-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="22dbf-129">**Description**</span></span>|<span data-ttu-id="22dbf-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="22dbf-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="22dbf-131">ID</span><span class="sxs-lookup"><span data-stu-id="22dbf-131">ID</span></span>  <br/> |<span data-ttu-id="22dbf-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="22dbf-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="22dbf-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22dbf-133">required</span></span>  <br/> |<span data-ttu-id="22dbf-134">Une valeur de base 1 qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="22dbf-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="22dbf-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="22dbf-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="22dbf-136">Initials</span><span class="sxs-lookup"><span data-stu-id="22dbf-136">Initials</span></span>  <br/> |<span data-ttu-id="22dbf-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="22dbf-137">xsd:string</span></span>  <br/> |<span data-ttu-id="22dbf-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="22dbf-138">optional</span></span>  <br/> |<span data-ttu-id="22dbf-139">Initiales de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="22dbf-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="22dbf-140">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="22dbf-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="22dbf-141">Nom</span><span class="sxs-lookup"><span data-stu-id="22dbf-141">Name</span></span>  <br/> |<span data-ttu-id="22dbf-142">XSD : String</span><span class="sxs-lookup"><span data-stu-id="22dbf-142">xsd:string</span></span>  <br/> |<span data-ttu-id="22dbf-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="22dbf-143">optional</span></span>  <br/> |<span data-ttu-id="22dbf-144">Le nom de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="22dbf-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="22dbf-145">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="22dbf-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="22dbf-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="22dbf-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="22dbf-147">XSD : String</span><span class="sxs-lookup"><span data-stu-id="22dbf-147">xsd:string</span></span>  <br/> |<span data-ttu-id="22dbf-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="22dbf-148">optional</span></span>  <br/> |<span data-ttu-id="22dbf-149">Identificateur unique de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="22dbf-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="22dbf-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="22dbf-150">Values of the xsd:string type.</span></span>  <br/> |
   

