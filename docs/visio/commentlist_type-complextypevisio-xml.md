---
title: CommentList_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 9b85a3731cfde30307084c65da1d23aa86280afd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542050"
---
# <a name="commentlist_type-complextype-visio-xml"></a><span data-ttu-id="63e32-102">CommentList_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="63e32-102">CommentList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="63e32-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="63e32-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63e32-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="63e32-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="63e32-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="63e32-105">**Schema file**</span></span> <br/> |<span data-ttu-id="63e32-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="63e32-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="63e32-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="63e32-107">**Extension base**</span></span> <br/> |<span data-ttu-id="63e32-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="63e32-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63e32-109">Définition</span><span class="sxs-lookup"><span data-stu-id="63e32-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="63e32-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="63e32-110">Elements and attributes</span></span>

<span data-ttu-id="63e32-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="63e32-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="63e32-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63e32-112">Child elements</span></span>

|<span data-ttu-id="63e32-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="63e32-113">**Element**</span></span>|<span data-ttu-id="63e32-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="63e32-114">**Type**</span></span>|<span data-ttu-id="63e32-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="63e32-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63e32-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="63e32-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63e32-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="63e32-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="63e32-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="63e32-118">Attributes</span></span>

<span data-ttu-id="63e32-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="63e32-119">None.</span></span>
  

