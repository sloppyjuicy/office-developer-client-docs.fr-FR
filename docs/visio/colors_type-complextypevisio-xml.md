---
title: Colors_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: bddcb93451bfb6d1b519720040a9e3875dc2ec5c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540139"
---
# <a name="colors_type-complextype-visio-xml"></a><span data-ttu-id="cc0d9-102">Colors_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cc0d9-102">Colors_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cc0d9-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="cc0d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc0d9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc0d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cc0d9-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="cc0d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cc0d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cc0d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cc0d9-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="cc0d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cc0d9-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="cc0d9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc0d9-109">Définition</span><span class="sxs-lookup"><span data-stu-id="cc0d9-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc0d9-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="cc0d9-110">Elements and attributes</span></span>

<span data-ttu-id="cc0d9-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="cc0d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cc0d9-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cc0d9-112">Child elements</span></span>

|<span data-ttu-id="cc0d9-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="cc0d9-113">**Element**</span></span>|<span data-ttu-id="cc0d9-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="cc0d9-114">**Type**</span></span>|<span data-ttu-id="cc0d9-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc0d9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc0d9-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="cc0d9-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc0d9-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="cc0d9-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cc0d9-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="cc0d9-118">Attributes</span></span>

<span data-ttu-id="cc0d9-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cc0d9-119">None.</span></span>
  

