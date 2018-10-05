---
title: Type complexe Extensions_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7760e1b22a7d573d8f61cf08ed54789f601e9339
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398135"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="bfda3-102">Type complexe Extensions_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="bfda3-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bfda3-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="bfda3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfda3-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="bfda3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bfda3-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="bfda3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bfda3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bfda3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bfda3-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="bfda3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bfda3-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="bfda3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bfda3-109">Définition</span><span class="sxs-lookup"><span data-stu-id="bfda3-109">Definition</span></span>

```XML
          <xs:complexType name="Extensions_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="FunctionDef"  type="FunctionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="SectionDef"  type="SectionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bfda3-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="bfda3-110">Elements and attributes</span></span>

<span data-ttu-id="bfda3-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="bfda3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bfda3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bfda3-112">Child elements</span></span>

|<span data-ttu-id="bfda3-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="bfda3-113">**Element**</span></span>|<span data-ttu-id="bfda3-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="bfda3-114">**Type**</span></span>|<span data-ttu-id="bfda3-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="bfda3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfda3-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="bfda3-116">CellDef</span></span> <br/> |[<span data-ttu-id="bfda3-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="bfda3-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="bfda3-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="bfda3-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="bfda3-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="bfda3-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="bfda3-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="bfda3-120">SectionDef</span></span> <br/> |[<span data-ttu-id="bfda3-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="bfda3-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bfda3-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="bfda3-122">Attributes</span></span>

<span data-ttu-id="bfda3-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bfda3-123">None.</span></span>
  

