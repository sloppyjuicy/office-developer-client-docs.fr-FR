---
title: Élément AuthorEntry (AuthorList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788035"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="ae809-103">Élément AuthorEntry (AuthorList_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ae809-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ae809-104">Spécifie les propriétés utilisées pour identifier l’auteur d’un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="ae809-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae809-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="ae809-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae809-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ae809-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ae809-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="ae809-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ae809-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ae809-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ae809-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ae809-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ae809-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ae809-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ae809-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ae809-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ae809-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="ae809-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ae809-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ae809-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ae809-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ae809-114">Elements and attributes</span></span>

<span data-ttu-id="ae809-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ae809-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ae809-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ae809-116">Parent elements</span></span>

|<span data-ttu-id="ae809-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ae809-117">**Element**</span></span>|<span data-ttu-id="ae809-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ae809-118">**Type**</span></span>|<span data-ttu-id="ae809-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ae809-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae809-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="ae809-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae809-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="ae809-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae809-122">Spécifie les auteurs dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="ae809-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae809-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ae809-123">Child elements</span></span>

<span data-ttu-id="ae809-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ae809-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae809-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="ae809-125">Attributes</span></span>

|<span data-ttu-id="ae809-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ae809-126">**Attribute**</span></span>|<span data-ttu-id="ae809-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="ae809-127">**Type**</span></span>|<span data-ttu-id="ae809-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ae809-128">**Required**</span></span>|<span data-ttu-id="ae809-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="ae809-129">**Description**</span></span>|<span data-ttu-id="ae809-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ae809-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ae809-131">ID</span><span class="sxs-lookup"><span data-stu-id="ae809-131">ID</span></span>  <br/> |<span data-ttu-id="ae809-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae809-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae809-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ae809-133">required</span></span>  <br/> |<span data-ttu-id="ae809-134">Une valeur de base 1 qui identifie l’auteur.</span><span class="sxs-lookup"><span data-stu-id="ae809-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="ae809-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae809-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae809-136">Initiales</span><span class="sxs-lookup"><span data-stu-id="ae809-136">Initials</span></span>  <br/> |<span data-ttu-id="ae809-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ae809-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ae809-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="ae809-138">optional</span></span>  <br/> |<span data-ttu-id="ae809-139">Initiales de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="ae809-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="ae809-140">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ae809-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ae809-141">Nom</span><span class="sxs-lookup"><span data-stu-id="ae809-141">Name</span></span>  <br/> |<span data-ttu-id="ae809-142">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ae809-142">xsd:string</span></span>  <br/> |<span data-ttu-id="ae809-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="ae809-143">optional</span></span>  <br/> |<span data-ttu-id="ae809-144">Le nom de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="ae809-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="ae809-145">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ae809-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ae809-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="ae809-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="ae809-147">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ae809-147">xsd:string</span></span>  <br/> |<span data-ttu-id="ae809-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="ae809-148">optional</span></span>  <br/> |<span data-ttu-id="ae809-149">Identificateur unique de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="ae809-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="ae809-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ae809-150">Values of the xsd:string type.</span></span>  <br/> |
   

