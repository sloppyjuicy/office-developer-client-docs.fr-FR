---
title: Élément AuthorList (complexType Comments_Type) (XML Visio)
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
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="fcfbe-103">Élément AuthorList (complexType Comments_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="fcfbe-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fcfbe-104">Spécifie les auteurs de commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="fcfbe-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fcfbe-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="fcfbe-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcfbe-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fcfbe-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="fcfbe-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fcfbe-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fcfbe-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fcfbe-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fcfbe-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fcfbe-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fcfbe-112">Comments. Xml</span><span class="sxs-lookup"><span data-stu-id="fcfbe-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fcfbe-113">Définition</span><span class="sxs-lookup"><span data-stu-id="fcfbe-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fcfbe-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fcfbe-114">Elements and attributes</span></span>

<span data-ttu-id="fcfbe-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="fcfbe-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fcfbe-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fcfbe-116">Parent elements</span></span>

|<span data-ttu-id="fcfbe-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-117">**Element**</span></span>|<span data-ttu-id="fcfbe-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-118">**Type**</span></span>|<span data-ttu-id="fcfbe-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fcfbe-120">Commentaires</span><span class="sxs-lookup"><span data-stu-id="fcfbe-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fcfbe-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="fcfbe-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fcfbe-122">Cette énumération spécifie les commentaires dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="fcfbe-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fcfbe-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fcfbe-123">Child elements</span></span>

|<span data-ttu-id="fcfbe-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-124">**Element**</span></span>|<span data-ttu-id="fcfbe-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-125">**Type**</span></span>|<span data-ttu-id="fcfbe-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="fcfbe-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fcfbe-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="fcfbe-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fcfbe-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="fcfbe-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fcfbe-129">Spécifie les propriétés qui identifient l’auteur d’un commentaire dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="fcfbe-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fcfbe-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="fcfbe-130">Attributes</span></span>

<span data-ttu-id="fcfbe-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fcfbe-131">None.</span></span>
  

