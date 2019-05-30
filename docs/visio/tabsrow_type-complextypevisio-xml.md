---
title: ComplexType TabsRow_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b9258a0-05fa-b0b0-90ed-dc1c4faa288a
ms.openlocfilehash: d7119cc1fef637992213ce49b250291d15b66c9f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541931"
---
# <a name="tabsrowtype-complextype-visio-xml"></a><span data-ttu-id="491d4-102">ComplexType TabsRow_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="491d4-102">TabsRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="491d4-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="491d4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="491d4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="491d4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="491d4-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="491d4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="491d4-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="491d4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="491d4-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="491d4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="491d4-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="491d4-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="491d4-109">Définition</span><span class="sxs-lookup"><span data-stu-id="491d4-109">Definition</span></span>

```XML
          <xs:complexType name="TabsRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="491d4-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="491d4-110">Elements and attributes</span></span>

<span data-ttu-id="491d4-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="491d4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="491d4-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="491d4-112">Child elements</span></span>

|<span data-ttu-id="491d4-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="491d4-113">**Element**</span></span>|<span data-ttu-id="491d4-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="491d4-114">**Type**</span></span>|<span data-ttu-id="491d4-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="491d4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="491d4-116">Cell</span><span class="sxs-lookup"><span data-stu-id="491d4-116">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="491d4-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="491d4-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="491d4-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="491d4-118">Attributes</span></span>

<span data-ttu-id="491d4-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="491d4-119">None.</span></span>
  

