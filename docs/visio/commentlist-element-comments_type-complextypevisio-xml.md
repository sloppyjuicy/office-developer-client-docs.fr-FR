---
title: Élément CommentList (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Spécifie les commentaires d’un dessin.
ms.openlocfilehash: fbbc7ea668686a8f075f3f11843b2d828c257363
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539247"
---
# <a name="commentlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="9d321-103">Élément CommentList (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9d321-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9d321-104">Spécifie les commentaires d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="9d321-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d321-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="9d321-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d321-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="9d321-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9d321-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="9d321-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9d321-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d321-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9d321-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9d321-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9d321-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9d321-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9d321-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="9d321-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9d321-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="9d321-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d321-113">Définition</span><span class="sxs-lookup"><span data-stu-id="9d321-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d321-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9d321-114">Elements and attributes</span></span>

<span data-ttu-id="9d321-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="9d321-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9d321-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9d321-116">Parent elements</span></span>

|<span data-ttu-id="9d321-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9d321-117">**Element**</span></span>|<span data-ttu-id="9d321-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9d321-118">**Type**</span></span>|<span data-ttu-id="9d321-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="9d321-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d321-120">Comments</span><span class="sxs-lookup"><span data-stu-id="9d321-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d321-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="9d321-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d321-122">Spécifie les propriétés utilisées pour identifier les auteurs et les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="9d321-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d321-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9d321-123">Child elements</span></span>

|<span data-ttu-id="9d321-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9d321-124">**Element**</span></span>|<span data-ttu-id="9d321-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9d321-125">**Type**</span></span>|<span data-ttu-id="9d321-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="9d321-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d321-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="9d321-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d321-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="9d321-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d321-129">Spécifie les propriétés utilisées pour identifier un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="9d321-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9d321-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="9d321-130">Attributes</span></span>

<span data-ttu-id="9d321-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9d321-131">None.</span></span>
  

