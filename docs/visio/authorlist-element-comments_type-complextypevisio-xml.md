---
title: Élément AuthorList (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Spécifie les auteurs de commentaires dans un dessin.
ms.openlocfilehash: c6e94c985d2728ba704a9159ec9bf3c4a2a72e95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537856"
---
# <a name="authorlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="66fbc-103">Élément AuthorList (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="66fbc-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="66fbc-104">Spécifie les auteurs de commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="66fbc-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66fbc-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="66fbc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66fbc-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="66fbc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66fbc-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="66fbc-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66fbc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="66fbc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66fbc-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="66fbc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66fbc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="66fbc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66fbc-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="66fbc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66fbc-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="66fbc-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66fbc-113">Définition</span><span class="sxs-lookup"><span data-stu-id="66fbc-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66fbc-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="66fbc-114">Elements and attributes</span></span>

<span data-ttu-id="66fbc-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="66fbc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66fbc-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="66fbc-116">Parent elements</span></span>

|<span data-ttu-id="66fbc-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="66fbc-117">**Element**</span></span>|<span data-ttu-id="66fbc-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="66fbc-118">**Type**</span></span>|<span data-ttu-id="66fbc-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="66fbc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66fbc-120">Comments</span><span class="sxs-lookup"><span data-stu-id="66fbc-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66fbc-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="66fbc-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66fbc-122">Spécifie les commentaires d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="66fbc-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66fbc-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66fbc-123">Child elements</span></span>

|<span data-ttu-id="66fbc-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="66fbc-124">**Element**</span></span>|<span data-ttu-id="66fbc-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="66fbc-125">**Type**</span></span>|<span data-ttu-id="66fbc-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="66fbc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66fbc-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="66fbc-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66fbc-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="66fbc-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66fbc-129">Spécifie les propriétés qui identifient l’auteur d’un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="66fbc-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="66fbc-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="66fbc-130">Attributes</span></span>

<span data-ttu-id="66fbc-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="66fbc-131">None.</span></span>
  

