---
title: ComplexType ScratchRow_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: c2fec0107bba66809536a1cf8bf43fb616a9ef81
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539025"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="ebe28-102">ComplexType ScratchRow_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ebe28-102">ScratchRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ebe28-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ebe28-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebe28-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ebe28-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ebe28-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ebe28-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ebe28-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ebe28-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ebe28-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ebe28-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ebe28-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="ebe28-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ebe28-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ebe28-109">Definition</span></span>

```XML
          <xs:complexType name="ScratchRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="ebe28-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ebe28-110">Elements and attributes</span></span>

<span data-ttu-id="ebe28-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ebe28-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ebe28-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ebe28-112">Child elements</span></span>

|<span data-ttu-id="ebe28-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ebe28-113">**Element**</span></span>|<span data-ttu-id="ebe28-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ebe28-114">**Type**</span></span>|<span data-ttu-id="ebe28-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ebe28-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ebe28-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ebe28-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ebe28-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ebe28-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ebe28-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="ebe28-118">Attributes</span></span>

<span data-ttu-id="ebe28-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ebe28-119">None.</span></span>
  

