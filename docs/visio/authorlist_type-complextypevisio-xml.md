---
title: ComplexType AuthorList_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 80a0dd01b3628bc44ed469ff7c236753d7677f51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338744"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="799b2-102">ComplexType AuthorList_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="799b2-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="799b2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="799b2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="799b2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="799b2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="799b2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="799b2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="799b2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="799b2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="799b2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="799b2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="799b2-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="799b2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="799b2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="799b2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="799b2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="799b2-110">Elements and attributes</span></span>

<span data-ttu-id="799b2-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="799b2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="799b2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="799b2-112">Child elements</span></span>

|<span data-ttu-id="799b2-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="799b2-113">**Element**</span></span>|<span data-ttu-id="799b2-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="799b2-114">**Type**</span></span>|<span data-ttu-id="799b2-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="799b2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="799b2-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="799b2-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="799b2-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="799b2-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="799b2-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="799b2-118">Attributes</span></span>

<span data-ttu-id="799b2-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="799b2-119">None.</span></span>
  

