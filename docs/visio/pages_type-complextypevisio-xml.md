---
title: ComplexType Pages_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: a03c5df25a28da40724178cf1c7f917ee4e723c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339766"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="1e770-102">ComplexType Pages_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1e770-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1e770-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1e770-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e770-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e770-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1e770-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1e770-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1e770-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1e770-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1e770-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1e770-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1e770-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="1e770-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e770-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1e770-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1e770-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1e770-110">Elements and attributes</span></span>

<span data-ttu-id="1e770-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="1e770-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1e770-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1e770-112">Child elements</span></span>

|<span data-ttu-id="1e770-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1e770-113">**Element**</span></span>|<span data-ttu-id="1e770-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="1e770-114">**Type**</span></span>|<span data-ttu-id="1e770-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="1e770-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e770-116">Page</span><span class="sxs-lookup"><span data-stu-id="1e770-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1e770-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="1e770-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1e770-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="1e770-118">Attributes</span></span>

<span data-ttu-id="1e770-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1e770-119">None.</span></span>
  

