---
title: ComplexType PolylineTo_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: e1c6c6912105ba593467cd4bb4e4cb0ded460233
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540097"
---
# <a name="polylinetotype-complextype-visio-xml"></a><span data-ttu-id="7bff5-102">ComplexType PolylineTo_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7bff5-102">PolylineTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7bff5-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7bff5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bff5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7bff5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7bff5-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7bff5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7bff5-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7bff5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7bff5-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7bff5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7bff5-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="7bff5-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7bff5-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7bff5-109">Definition</span></span>

```XML
          <xs:complexType name="PolylineTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7bff5-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7bff5-110">Elements and attributes</span></span>

<span data-ttu-id="7bff5-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="7bff5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7bff5-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7bff5-112">Child elements</span></span>

|<span data-ttu-id="7bff5-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7bff5-113">**Element**</span></span>|<span data-ttu-id="7bff5-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="7bff5-114">**Type**</span></span>|<span data-ttu-id="7bff5-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7bff5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7bff5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="7bff5-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="7bff5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7bff5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7bff5-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="7bff5-118">Attributes</span></span>

<span data-ttu-id="7bff5-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7bff5-119">None.</span></span>
  

