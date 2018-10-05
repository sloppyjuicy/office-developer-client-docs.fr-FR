---
title: Type complexe AuthorList_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 80a0dd01b3628bc44ed469ff7c236753d7677f51
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394551"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="c4ebe-102">Type complexe AuthorList_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c4ebe-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c4ebe-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c4ebe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4ebe-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c4ebe-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c4ebe-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c4ebe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c4ebe-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c4ebe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c4ebe-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c4ebe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c4ebe-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="c4ebe-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4ebe-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c4ebe-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c4ebe-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c4ebe-110">Elements and attributes</span></span>

<span data-ttu-id="c4ebe-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c4ebe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4ebe-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4ebe-112">Child elements</span></span>

|<span data-ttu-id="c4ebe-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c4ebe-113">**Element**</span></span>|<span data-ttu-id="c4ebe-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c4ebe-114">**Type**</span></span>|<span data-ttu-id="c4ebe-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4ebe-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4ebe-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="c4ebe-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c4ebe-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="c4ebe-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c4ebe-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c4ebe-118">Attributes</span></span>

<span data-ttu-id="c4ebe-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c4ebe-119">None.</span></span>
  

