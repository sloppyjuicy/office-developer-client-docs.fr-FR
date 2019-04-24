---
title: Élément CommentList (complexType Comments_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Cette énumération spécifie les commentaires dans un dessin.
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359429"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="1678a-103">Élément CommentList (complexType Comments_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1678a-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1678a-104">Cette énumération spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="1678a-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1678a-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="1678a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1678a-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="1678a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1678a-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="1678a-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1678a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1678a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1678a-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1678a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1678a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="1678a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1678a-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="1678a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1678a-112">Comments. Xml</span><span class="sxs-lookup"><span data-stu-id="1678a-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1678a-113">Définition</span><span class="sxs-lookup"><span data-stu-id="1678a-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1678a-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1678a-114">Elements and attributes</span></span>

<span data-ttu-id="1678a-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="1678a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1678a-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1678a-116">Parent elements</span></span>

|<span data-ttu-id="1678a-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1678a-117">**Element**</span></span>|<span data-ttu-id="1678a-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="1678a-118">**Type**</span></span>|<span data-ttu-id="1678a-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="1678a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1678a-120">Comments</span><span class="sxs-lookup"><span data-stu-id="1678a-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1678a-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="1678a-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1678a-122">Spécifie les propriétés utilisées pour identifier les auteurs et les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="1678a-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1678a-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1678a-123">Child elements</span></span>

|<span data-ttu-id="1678a-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1678a-124">**Element**</span></span>|<span data-ttu-id="1678a-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="1678a-125">**Type**</span></span>|<span data-ttu-id="1678a-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="1678a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1678a-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="1678a-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1678a-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="1678a-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1678a-129">Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="1678a-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1678a-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="1678a-130">Attributes</span></span>

<span data-ttu-id="1678a-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1678a-131">None.</span></span>
  

