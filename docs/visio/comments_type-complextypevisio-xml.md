---
title: Type complexe Comments_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: b2d40b1c8368945cfa27aad0e1d567beea694c28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393471"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="0c8b1-102">Type complexe Comments_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0c8b1-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0c8b1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="0c8b1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c8b1-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c8b1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c8b1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c8b1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c8b1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c8b1-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="0c8b1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c8b1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0c8b1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0c8b1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0c8b1-110">Elements and attributes</span></span>

<span data-ttu-id="0c8b1-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0c8b1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c8b1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0c8b1-112">Child elements</span></span>

|<span data-ttu-id="0c8b1-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-113">**Element**</span></span>|<span data-ttu-id="0c8b1-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-114">**Type**</span></span>|<span data-ttu-id="0c8b1-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0c8b1-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="0c8b1-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c8b1-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="0c8b1-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0c8b1-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="0c8b1-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c8b1-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="0c8b1-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0c8b1-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="0c8b1-120">Attributes</span></span>

|<span data-ttu-id="0c8b1-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-121">**Attribute**</span></span>|<span data-ttu-id="0c8b1-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-122">**Type**</span></span>|<span data-ttu-id="0c8b1-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-123">**Required**</span></span>|<span data-ttu-id="0c8b1-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-124">**Description**</span></span>|<span data-ttu-id="0c8b1-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0c8b1-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c8b1-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="0c8b1-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="0c8b1-127">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0c8b1-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c8b1-128">facultatif</span><span class="sxs-lookup"><span data-stu-id="0c8b1-128">optional</span></span>  <br/> ||<span data-ttu-id="0c8b1-129">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0c8b1-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

