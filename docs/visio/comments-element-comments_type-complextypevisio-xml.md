---
title: Élément Comments (Comments_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Spécifie les propriétés permettant d’identifier les auteurs et les commentaires dans un dessin.
ms.openlocfilehash: 77695fb32aa88cb6c2b6ac5e9bff99fa12e262bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788290"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="7e4be-103">Élément Comments (Comments_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="7e4be-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7e4be-104">Spécifie les propriétés permettant d’identifier les auteurs et les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="7e4be-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e4be-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="7e4be-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e4be-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="7e4be-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7e4be-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="7e4be-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7e4be-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="7e4be-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7e4be-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7e4be-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7e4be-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7e4be-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7e4be-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="7e4be-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7e4be-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="7e4be-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7e4be-113">Définition</span><span class="sxs-lookup"><span data-stu-id="7e4be-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7e4be-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7e4be-114">Elements and attributes</span></span>

<span data-ttu-id="7e4be-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="7e4be-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7e4be-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7e4be-116">Parent elements</span></span>

<span data-ttu-id="7e4be-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7e4be-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e4be-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7e4be-118">Child elements</span></span>

|<span data-ttu-id="7e4be-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7e4be-119">**Element**</span></span>|<span data-ttu-id="7e4be-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="7e4be-120">**Type**</span></span>|<span data-ttu-id="7e4be-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e4be-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e4be-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="7e4be-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7e4be-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="7e4be-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7e4be-124">Spécifie les auteurs dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="7e4be-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="7e4be-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="7e4be-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7e4be-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="7e4be-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7e4be-127">Spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="7e4be-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7e4be-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="7e4be-128">Attributes</span></span>

<span data-ttu-id="7e4be-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7e4be-129">None.</span></span>
  

