---
title: ComplexType Extensions_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7fe070087afab9cdc6eac9e35a230b02ab7d62ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542372"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="a22e7-102">ComplexType Extensions_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a22e7-102">Extensions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a22e7-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a22e7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a22e7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a22e7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a22e7-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a22e7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a22e7-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a22e7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a22e7-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a22e7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a22e7-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="a22e7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a22e7-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a22e7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a22e7-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a22e7-110">Elements and attributes</span></span>

<span data-ttu-id="a22e7-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a22e7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a22e7-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a22e7-112">Child elements</span></span>

|<span data-ttu-id="a22e7-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a22e7-113">**Element**</span></span>|<span data-ttu-id="a22e7-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a22e7-114">**Type**</span></span>|<span data-ttu-id="a22e7-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a22e7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a22e7-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="a22e7-116">CellDef</span></span> <br/> |[<span data-ttu-id="a22e7-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="a22e7-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="a22e7-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="a22e7-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="a22e7-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="a22e7-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="a22e7-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="a22e7-120">SectionDef</span></span> <br/> |[<span data-ttu-id="a22e7-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="a22e7-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a22e7-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="a22e7-122">Attributes</span></span>

<span data-ttu-id="a22e7-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a22e7-123">None.</span></span>
  

