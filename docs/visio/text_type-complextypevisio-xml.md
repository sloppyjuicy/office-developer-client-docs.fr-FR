---
title: Type complexe Text_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: 3309184c47eaf6c6a8cb20d7c6485c21c5ec8c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789854"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="6f17a-102">Type complexe Text_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="6f17a-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6f17a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6f17a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f17a-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="6f17a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6f17a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6f17a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6f17a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6f17a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6f17a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6f17a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6f17a-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="6f17a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6f17a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6f17a-109">Definition</span></span>

```XML
          <xs:complexType name="Text_Type">
          
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="cp"  type="cp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="pp"  type="pp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="tp"  type="tp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="fld"  type="fld_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6f17a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6f17a-110">Elements and attributes</span></span>

<span data-ttu-id="6f17a-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="6f17a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6f17a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6f17a-112">Child elements</span></span>

|<span data-ttu-id="6f17a-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6f17a-113">**Element**</span></span>|<span data-ttu-id="6f17a-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="6f17a-114">**Type**</span></span>|<span data-ttu-id="6f17a-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6f17a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6f17a-116">CP</span><span class="sxs-lookup"><span data-stu-id="6f17a-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6f17a-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="6f17a-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6f17a-118">fld</span><span class="sxs-lookup"><span data-stu-id="6f17a-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6f17a-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="6f17a-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6f17a-120">PP</span><span class="sxs-lookup"><span data-stu-id="6f17a-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6f17a-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="6f17a-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6f17a-122">TP</span><span class="sxs-lookup"><span data-stu-id="6f17a-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6f17a-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="6f17a-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6f17a-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="6f17a-124">Attributes</span></span>

<span data-ttu-id="6f17a-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6f17a-125">None.</span></span>
  

