---
title: ComplexType PageContents_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: 70f28182d8c82b9283e793856f7944c9a4823bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334495"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="7fd36-102">ComplexType PageContents_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7fd36-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7fd36-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7fd36-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fd36-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7fd36-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7fd36-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7fd36-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7fd36-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7fd36-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7fd36-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7fd36-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7fd36-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="7fd36-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7fd36-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7fd36-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7fd36-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7fd36-110">Elements and attributes</span></span>

<span data-ttu-id="7fd36-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="7fd36-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7fd36-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7fd36-112">Child elements</span></span>

|<span data-ttu-id="7fd36-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7fd36-113">**Element**</span></span>|<span data-ttu-id="7fd36-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="7fd36-114">**Type**</span></span>|<span data-ttu-id="7fd36-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7fd36-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7fd36-116">Connects</span><span class="sxs-lookup"><span data-stu-id="7fd36-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7fd36-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="7fd36-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7fd36-118">Shapes</span><span class="sxs-lookup"><span data-stu-id="7fd36-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7fd36-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="7fd36-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7fd36-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="7fd36-120">Attributes</span></span>

<span data-ttu-id="7fd36-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7fd36-121">None.</span></span>
  

