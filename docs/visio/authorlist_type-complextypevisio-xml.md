---
title: Type complexe AuthorList_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: e4cee87a5060580e8b7f1efc7970091d56fd310f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788017"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="4a937-102">Type complexe AuthorList_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="4a937-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4a937-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="4a937-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a937-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4a937-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4a937-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4a937-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4a937-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4a937-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4a937-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="4a937-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4a937-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="4a937-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a937-109">Définition</span><span class="sxs-lookup"><span data-stu-id="4a937-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a937-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4a937-110">Elements and attributes</span></span>

<span data-ttu-id="4a937-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4a937-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4a937-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4a937-112">Child elements</span></span>

|<span data-ttu-id="4a937-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4a937-113">**Element**</span></span>|<span data-ttu-id="4a937-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="4a937-114">**Type**</span></span>|<span data-ttu-id="4a937-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="4a937-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a937-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="4a937-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a937-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="4a937-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4a937-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="4a937-118">Attributes</span></span>

<span data-ttu-id="4a937-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4a937-119">None.</span></span>
  

