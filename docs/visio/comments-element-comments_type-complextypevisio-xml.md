---
title: Élément comments (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Spécifie les propriétés utilisées pour identifier les auteurs et les commentaires dans un dessin.
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359394"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="512f5-103">Élément comments (Comments_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="512f5-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="512f5-104">Spécifie les propriétés utilisées pour identifier les auteurs et les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="512f5-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="512f5-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="512f5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="512f5-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="512f5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="512f5-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="512f5-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="512f5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="512f5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="512f5-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="512f5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="512f5-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="512f5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="512f5-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="512f5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="512f5-112">Comments. Xml</span><span class="sxs-lookup"><span data-stu-id="512f5-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="512f5-113">Définition</span><span class="sxs-lookup"><span data-stu-id="512f5-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="512f5-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="512f5-114">Elements and attributes</span></span>

<span data-ttu-id="512f5-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="512f5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="512f5-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="512f5-116">Parent elements</span></span>

<span data-ttu-id="512f5-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="512f5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="512f5-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="512f5-118">Child elements</span></span>

|<span data-ttu-id="512f5-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="512f5-119">**Element**</span></span>|<span data-ttu-id="512f5-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="512f5-120">**Type**</span></span>|<span data-ttu-id="512f5-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="512f5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="512f5-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="512f5-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="512f5-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="512f5-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="512f5-124">Spécifie les auteurs d'un dessin.</span><span class="sxs-lookup"><span data-stu-id="512f5-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="512f5-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="512f5-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="512f5-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="512f5-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="512f5-127">Cette énumération spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="512f5-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="512f5-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="512f5-128">Attributes</span></span>

<span data-ttu-id="512f5-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="512f5-129">None.</span></span>
  

