---
title: ComplexType ParagraphRow_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32bb67e1-8db8-fe28-f173-028a20bb136c
ms.openlocfilehash: 942d29516e5277fc9b0e68319118c309d9555648
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540580"
---
# <a name="paragraphrowtype-complextype-visio-xml"></a><span data-ttu-id="ef573-102">ComplexType ParagraphRow_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ef573-102">ParagraphRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ef573-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ef573-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef573-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef573-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ef573-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ef573-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ef573-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ef573-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ef573-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ef573-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ef573-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="ef573-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef573-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ef573-109">Definition</span></span>

```XML
          <xs:complexType name="ParagraphRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="ef573-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ef573-110">Elements and attributes</span></span>

<span data-ttu-id="ef573-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ef573-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ef573-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef573-112">Child elements</span></span>

|<span data-ttu-id="ef573-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ef573-113">**Element**</span></span>|<span data-ttu-id="ef573-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ef573-114">**Type**</span></span>|<span data-ttu-id="ef573-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef573-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef573-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ef573-116">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ef573-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ef573-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ef573-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef573-118">Attributes</span></span>

<span data-ttu-id="ef573-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ef573-119">None.</span></span>
  

