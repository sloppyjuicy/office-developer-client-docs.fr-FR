---
title: Type complexe Pages_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: a03c5df25a28da40724178cf1c7f917ee4e723c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400158"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="a776f-102">Type complexe Pages_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a776f-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a776f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a776f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a776f-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a776f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a776f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a776f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a776f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a776f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a776f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a776f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a776f-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="a776f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a776f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a776f-109">Definition</span></span>

```XML
          <xs:complexType name="Pages_Type">
          
          <xs:sequence>
    <xs:element name="Page"  type="Page_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a776f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a776f-110">Elements and attributes</span></span>

<span data-ttu-id="a776f-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a776f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a776f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a776f-112">Child elements</span></span>

|<span data-ttu-id="a776f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a776f-113">**Element**</span></span>|<span data-ttu-id="a776f-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a776f-114">**Type**</span></span>|<span data-ttu-id="a776f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a776f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a776f-116">Page</span><span class="sxs-lookup"><span data-stu-id="a776f-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a776f-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="a776f-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a776f-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="a776f-118">Attributes</span></span>

<span data-ttu-id="a776f-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a776f-119">None.</span></span>
  

