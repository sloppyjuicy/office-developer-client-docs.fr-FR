---
title: Élément CommentList (Comments_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Spécifie les commentaires dans un dessin.
ms.openlocfilehash: 5773b4553185fbc99718be495c48a478ae72000c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788294"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="a8643-103">Élément CommentList (Comments_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a8643-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a8643-104">Spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="a8643-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8643-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="a8643-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8643-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a8643-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a8643-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="a8643-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a8643-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a8643-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a8643-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a8643-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a8643-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a8643-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a8643-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="a8643-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a8643-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="a8643-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8643-113">Définition</span><span class="sxs-lookup"><span data-stu-id="a8643-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8643-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a8643-114">Elements and attributes</span></span>

<span data-ttu-id="a8643-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a8643-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a8643-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a8643-116">Parent elements</span></span>

|<span data-ttu-id="a8643-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a8643-117">**Element**</span></span>|<span data-ttu-id="a8643-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8643-118">**Type**</span></span>|<span data-ttu-id="a8643-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8643-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8643-120">Comments</span><span class="sxs-lookup"><span data-stu-id="a8643-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a8643-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="a8643-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8643-122">Spécifie les propriétés permettant d’identifier les auteurs et les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="a8643-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a8643-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8643-123">Child elements</span></span>

|<span data-ttu-id="a8643-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a8643-124">**Element**</span></span>|<span data-ttu-id="a8643-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8643-125">**Type**</span></span>|<span data-ttu-id="a8643-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8643-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8643-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="a8643-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a8643-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="a8643-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8643-129">Spécifie les propriétés permettant d’identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="a8643-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a8643-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8643-130">Attributes</span></span>

<span data-ttu-id="a8643-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a8643-131">None.</span></span>
  

