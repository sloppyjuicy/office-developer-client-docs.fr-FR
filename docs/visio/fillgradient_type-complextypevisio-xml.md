---
title: ComplexType FillGradient_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82545cdc-890d-1b2f-9c8f-4740f32d0ed7
ms.openlocfilehash: 83e8eef809f566bb2a69e5b2da1d1c5d932ce54c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539641"
---
# <a name="fillgradienttype-complextype-visio-xml"></a><span data-ttu-id="c4b40-102">ComplexType FillGradient_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c4b40-102">FillGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c4b40-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c4b40-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4b40-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c4b40-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c4b40-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c4b40-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c4b40-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c4b40-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c4b40-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c4b40-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c4b40-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c4b40-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4b40-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c4b40-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FillGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c4b40-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c4b40-110">Elements and attributes</span></span>

<span data-ttu-id="c4b40-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="c4b40-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4b40-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4b40-112">Child elements</span></span>

|<span data-ttu-id="c4b40-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c4b40-113">**Element**</span></span>|<span data-ttu-id="c4b40-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c4b40-114">**Type**</span></span>|<span data-ttu-id="c4b40-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4b40-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4b40-116">Row</span><span class="sxs-lookup"><span data-stu-id="c4b40-116">Row</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c4b40-117">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="c4b40-117">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c4b40-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c4b40-118">Attributes</span></span>

<span data-ttu-id="c4b40-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c4b40-119">None.</span></span>
  

