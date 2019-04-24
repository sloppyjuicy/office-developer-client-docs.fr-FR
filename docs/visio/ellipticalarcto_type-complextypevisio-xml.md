---
title: ComplexType EllipticalArcTo_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: a6b10c60563a7923990cdb552b1d10fd5c43b97e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345632"
---
# <a name="ellipticalarctotype-complextype-visio-xml"></a><span data-ttu-id="63d3f-102">ComplexType EllipticalArcTo_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="63d3f-102">EllipticalArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="63d3f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="63d3f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63d3f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="63d3f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="63d3f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="63d3f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="63d3f-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="63d3f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="63d3f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="63d3f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="63d3f-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="63d3f-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63d3f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="63d3f-109">Definition</span></span>

```XML
          <xs:complexType name="EllipticalArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="63d3f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="63d3f-110">Elements and attributes</span></span>

<span data-ttu-id="63d3f-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="63d3f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="63d3f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63d3f-112">Child elements</span></span>

|<span data-ttu-id="63d3f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="63d3f-113">**Element**</span></span>|<span data-ttu-id="63d3f-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="63d3f-114">**Type**</span></span>|<span data-ttu-id="63d3f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="63d3f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63d3f-116">Cell</span><span class="sxs-lookup"><span data-stu-id="63d3f-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="63d3f-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="63d3f-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="63d3f-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="63d3f-118">Attributes</span></span>

<span data-ttu-id="63d3f-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="63d3f-119">None.</span></span>
  

