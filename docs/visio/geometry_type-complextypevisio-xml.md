---
title: Geometry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 1b16a32462f997ab80b0b6ef64df8eb202740c47
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542288"
---
# <a name="geometry_type-complextype-visio-xml"></a><span data-ttu-id="cd182-102">Geometry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cd182-102">Geometry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cd182-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="cd182-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd182-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cd182-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cd182-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="cd182-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cd182-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cd182-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cd182-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="cd182-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cd182-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="cd182-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cd182-109">Définition</span><span class="sxs-lookup"><span data-stu-id="cd182-109">Definition</span></span>

```XML
          <xs:complexType name="Geometry_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="GeometryRow_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cd182-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="cd182-110">Elements and attributes</span></span>

<span data-ttu-id="cd182-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="cd182-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cd182-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cd182-112">Child elements</span></span>

|<span data-ttu-id="cd182-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="cd182-113">**Element**</span></span>|<span data-ttu-id="cd182-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="cd182-114">**Type**</span></span>|<span data-ttu-id="cd182-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="cd182-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cd182-116">Cell</span><span class="sxs-lookup"><span data-stu-id="cd182-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="cd182-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="cd182-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cd182-118">Ligne</span><span class="sxs-lookup"><span data-stu-id="cd182-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="cd182-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="cd182-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cd182-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="cd182-120">Attributes</span></span>

<span data-ttu-id="cd182-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cd182-121">None.</span></span>
  

