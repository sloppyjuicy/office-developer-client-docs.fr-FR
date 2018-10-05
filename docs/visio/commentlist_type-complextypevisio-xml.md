---
title: Type complexe CommentList_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: af23616556cecdbfa1157a8d4c49de1ca4b2fd88
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393095"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="9fdc8-102">Type complexe CommentList_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9fdc8-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9fdc8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9fdc8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fdc8-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9fdc8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9fdc8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9fdc8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9fdc8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9fdc8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9fdc8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9fdc8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9fdc8-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="9fdc8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fdc8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9fdc8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9fdc8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9fdc8-110">Elements and attributes</span></span>

<span data-ttu-id="9fdc8-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9fdc8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9fdc8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9fdc8-112">Child elements</span></span>

|<span data-ttu-id="9fdc8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9fdc8-113">**Element**</span></span>|<span data-ttu-id="9fdc8-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="9fdc8-114">**Type**</span></span>|<span data-ttu-id="9fdc8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9fdc8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fdc8-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="9fdc8-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdc8-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="9fdc8-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9fdc8-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9fdc8-118">Attributes</span></span>

<span data-ttu-id="9fdc8-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9fdc8-119">None.</span></span>
  

