---
title: Comments_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: cce19353343190225efedec7f0a5c7bc0f026705
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542015"
---
# <a name="comments_type-complextype-visio-xml"></a><span data-ttu-id="26d5b-102">Comments_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="26d5b-102">Comments_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="26d5b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="26d5b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26d5b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26d5b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="26d5b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="26d5b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="26d5b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="26d5b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="26d5b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="26d5b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="26d5b-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="26d5b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26d5b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="26d5b-109">Definition</span></span>

```XML
          <xs:complexType name="Comments_Type">
          
          <xs:sequence>
    <xs:element name="AuthorList"  type="AuthorList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CommentList"  type="CommentList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ShowCommentTags"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26d5b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="26d5b-110">Elements and attributes</span></span>

<span data-ttu-id="26d5b-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="26d5b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="26d5b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="26d5b-112">Child elements</span></span>

|<span data-ttu-id="26d5b-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="26d5b-113">**Element**</span></span>|<span data-ttu-id="26d5b-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="26d5b-114">**Type**</span></span>|<span data-ttu-id="26d5b-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="26d5b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26d5b-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="26d5b-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26d5b-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="26d5b-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="26d5b-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="26d5b-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26d5b-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="26d5b-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="26d5b-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="26d5b-120">Attributes</span></span>

|<span data-ttu-id="26d5b-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="26d5b-121">**Attribute**</span></span>|<span data-ttu-id="26d5b-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="26d5b-122">**Type**</span></span>|<span data-ttu-id="26d5b-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="26d5b-123">**Required**</span></span>|<span data-ttu-id="26d5b-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="26d5b-124">**Description**</span></span>|<span data-ttu-id="26d5b-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="26d5b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26d5b-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="26d5b-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="26d5b-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="26d5b-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="26d5b-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="26d5b-128">optional</span></span>  <br/> ||<span data-ttu-id="26d5b-129">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="26d5b-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

