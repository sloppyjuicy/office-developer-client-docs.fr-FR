---
title: Élément AuthorList (Comments_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Spécifie les auteurs de commentaires dans un dessin.
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387740"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="b36ef-103">Élément AuthorList (Comments_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="b36ef-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b36ef-104">Spécifie les auteurs de commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="b36ef-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b36ef-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="b36ef-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b36ef-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="b36ef-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b36ef-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="b36ef-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b36ef-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="b36ef-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b36ef-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b36ef-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b36ef-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b36ef-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b36ef-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="b36ef-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b36ef-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="b36ef-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b36ef-113">Définition</span><span class="sxs-lookup"><span data-stu-id="b36ef-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b36ef-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b36ef-114">Elements and attributes</span></span>

<span data-ttu-id="b36ef-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="b36ef-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b36ef-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b36ef-116">Parent elements</span></span>

|<span data-ttu-id="b36ef-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b36ef-117">**Element**</span></span>|<span data-ttu-id="b36ef-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="b36ef-118">**Type**</span></span>|<span data-ttu-id="b36ef-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="b36ef-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b36ef-120">Comments</span><span class="sxs-lookup"><span data-stu-id="b36ef-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b36ef-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="b36ef-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b36ef-122">Spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="b36ef-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b36ef-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b36ef-123">Child elements</span></span>

|<span data-ttu-id="b36ef-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b36ef-124">**Element**</span></span>|<span data-ttu-id="b36ef-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="b36ef-125">**Type**</span></span>|<span data-ttu-id="b36ef-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="b36ef-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b36ef-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="b36ef-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b36ef-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="b36ef-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b36ef-129">Spécifie les propriétés qui identifient l’auteur d’un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="b36ef-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b36ef-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="b36ef-130">Attributes</span></span>

<span data-ttu-id="b36ef-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b36ef-131">None.</span></span>
  

