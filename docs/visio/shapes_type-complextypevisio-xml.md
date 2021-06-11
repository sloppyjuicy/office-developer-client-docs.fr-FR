---
title: Shapes_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 798af3d68df6c430fffb318e5e19c83aea441ca0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542085"
---
# <a name="shapes_type-complextype-visio-xml"></a><span data-ttu-id="62a00-102">Shapes_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="62a00-102">Shapes_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="62a00-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="62a00-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62a00-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="62a00-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="62a00-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="62a00-105">**Schema file**</span></span> <br/> |<span data-ttu-id="62a00-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="62a00-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="62a00-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="62a00-107">**Extension base**</span></span> <br/> |<span data-ttu-id="62a00-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="62a00-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62a00-109">Définition</span><span class="sxs-lookup"><span data-stu-id="62a00-109">Definition</span></span>

```XML
          <xs:complexType name="Shapes_Type">
          
          <xs:sequence>
    <xs:element name="Shape"  type="ShapeSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62a00-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="62a00-110">Elements and attributes</span></span>

<span data-ttu-id="62a00-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="62a00-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="62a00-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="62a00-112">Child elements</span></span>

|<span data-ttu-id="62a00-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="62a00-113">**Element**</span></span>|<span data-ttu-id="62a00-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="62a00-114">**Type**</span></span>|<span data-ttu-id="62a00-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="62a00-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62a00-116">Forme</span><span class="sxs-lookup"><span data-stu-id="62a00-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62a00-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="62a00-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="62a00-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="62a00-118">Attributes</span></span>

<span data-ttu-id="62a00-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="62a00-119">None.</span></span>
  

