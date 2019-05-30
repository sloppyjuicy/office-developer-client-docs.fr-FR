---
title: Élément comments (Comments_Type XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Spécifie les propriétés utilisées pour identifier les auteurs et les commentaires dans un dessin.
ms.openlocfilehash: 93e75e47a203ee13385085c4b5e261fd3a724d4f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539219"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="0b91f-103">Élément comments (Comments_Type XML)</span><span class="sxs-lookup"><span data-stu-id="0b91f-103">Comments element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0b91f-104">Spécifie les propriétés utilisées pour identifier les auteurs et les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="0b91f-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b91f-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="0b91f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b91f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0b91f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0b91f-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="0b91f-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0b91f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0b91f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0b91f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0b91f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0b91f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0b91f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0b91f-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="0b91f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0b91f-112">Comments. Xml</span><span class="sxs-lookup"><span data-stu-id="0b91f-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0b91f-113">Définition</span><span class="sxs-lookup"><span data-stu-id="0b91f-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0b91f-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0b91f-114">Elements and attributes</span></span>

<span data-ttu-id="0b91f-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="0b91f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0b91f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0b91f-116">Parent elements</span></span>

<span data-ttu-id="0b91f-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="0b91f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b91f-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0b91f-118">Child elements</span></span>

|<span data-ttu-id="0b91f-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0b91f-119">**Element**</span></span>|<span data-ttu-id="0b91f-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="0b91f-120">**Type**</span></span>|<span data-ttu-id="0b91f-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="0b91f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0b91f-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="0b91f-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0b91f-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="0b91f-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0b91f-124">Spécifie les auteurs d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="0b91f-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="0b91f-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="0b91f-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0b91f-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="0b91f-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0b91f-127">Cette énumération spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="0b91f-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0b91f-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="0b91f-128">Attributes</span></span>

<span data-ttu-id="0b91f-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0b91f-129">None.</span></span>
  

