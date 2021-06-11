---
title: Pages_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: 4615f365448b96981088352f9f2d6e98255e4101
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538941"
---
# <a name="pages_type-complextype-visio-xml"></a><span data-ttu-id="dadf6-102">Pages_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dadf6-102">Pages_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dadf6-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="dadf6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dadf6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dadf6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dadf6-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="dadf6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dadf6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dadf6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dadf6-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="dadf6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dadf6-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="dadf6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dadf6-109">Définition</span><span class="sxs-lookup"><span data-stu-id="dadf6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dadf6-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="dadf6-110">Elements and attributes</span></span>

<span data-ttu-id="dadf6-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="dadf6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dadf6-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dadf6-112">Child elements</span></span>

|<span data-ttu-id="dadf6-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="dadf6-113">**Element**</span></span>|<span data-ttu-id="dadf6-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="dadf6-114">**Type**</span></span>|<span data-ttu-id="dadf6-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="dadf6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dadf6-116">Page</span><span class="sxs-lookup"><span data-stu-id="dadf6-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dadf6-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="dadf6-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="dadf6-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="dadf6-118">Attributes</span></span>

<span data-ttu-id="dadf6-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dadf6-119">None.</span></span>
  

