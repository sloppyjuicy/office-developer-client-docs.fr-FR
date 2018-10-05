---
title: Type complexe Text_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: fe74af493983122c113e48ae5c0bb3b5b037ccef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384786"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="9511b-102">Type complexe Text_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9511b-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9511b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9511b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9511b-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9511b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9511b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9511b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9511b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9511b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9511b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9511b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9511b-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="9511b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9511b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9511b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9511b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9511b-110">Elements and attributes</span></span>

<span data-ttu-id="9511b-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9511b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9511b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9511b-112">Child elements</span></span>

|<span data-ttu-id="9511b-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9511b-113">**Element**</span></span>|<span data-ttu-id="9511b-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="9511b-114">**Type**</span></span>|<span data-ttu-id="9511b-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9511b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9511b-116">CP</span><span class="sxs-lookup"><span data-stu-id="9511b-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9511b-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="9511b-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9511b-118">chp</span><span class="sxs-lookup"><span data-stu-id="9511b-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9511b-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="9511b-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9511b-120">PP</span><span class="sxs-lookup"><span data-stu-id="9511b-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9511b-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="9511b-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9511b-122">TP</span><span class="sxs-lookup"><span data-stu-id="9511b-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9511b-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="9511b-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9511b-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="9511b-124">Attributes</span></span>

<span data-ttu-id="9511b-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9511b-125">None.</span></span>
  

