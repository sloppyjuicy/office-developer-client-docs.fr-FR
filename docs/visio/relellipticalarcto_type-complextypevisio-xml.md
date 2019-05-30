---
title: ComplexType RelEllipticalArcTo_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 45b2ff30-bca1-fbaa-cc9f-fe9b52b631c4
ms.openlocfilehash: 701676adcb82c2aeee63a975c2a35fc6c5256635
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542720"
---
# <a name="relellipticalarctotype-complextype-visio-xml"></a><span data-ttu-id="d6e73-102">ComplexType RelEllipticalArcTo_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d6e73-102">RelEllipticalArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d6e73-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="d6e73-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6e73-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d6e73-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d6e73-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d6e73-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d6e73-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="d6e73-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d6e73-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="d6e73-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d6e73-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="d6e73-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6e73-109">Définition</span><span class="sxs-lookup"><span data-stu-id="d6e73-109">Definition</span></span>

```XML
          <xs:complexType name="RelEllipticalArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="d6e73-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d6e73-110">Elements and attributes</span></span>

<span data-ttu-id="d6e73-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="d6e73-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d6e73-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d6e73-112">Child elements</span></span>

|<span data-ttu-id="d6e73-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d6e73-113">**Element**</span></span>|<span data-ttu-id="d6e73-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="d6e73-114">**Type**</span></span>|<span data-ttu-id="d6e73-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="d6e73-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6e73-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d6e73-116">Cell</span></span>](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="d6e73-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d6e73-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d6e73-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="d6e73-118">Attributes</span></span>

<span data-ttu-id="d6e73-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d6e73-119">None.</span></span>
  

