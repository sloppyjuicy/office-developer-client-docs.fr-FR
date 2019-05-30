---
title: ComplexType Property_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: 1eb2d9f11a264138f5d1a325d31e17789d1c9483
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540734"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="9dba2-102">ComplexType Property_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9dba2-102">Property_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9dba2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9dba2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dba2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9dba2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9dba2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9dba2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9dba2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9dba2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9dba2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9dba2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9dba2-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9dba2-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9dba2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9dba2-109">Definition</span></span>

```XML
          <xs:complexType name="Property_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="PropertyRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9dba2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9dba2-110">Elements and attributes</span></span>

<span data-ttu-id="9dba2-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="9dba2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9dba2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9dba2-112">Child elements</span></span>

|<span data-ttu-id="9dba2-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9dba2-113">**Element**</span></span>|<span data-ttu-id="9dba2-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="9dba2-114">**Type**</span></span>|<span data-ttu-id="9dba2-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9dba2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9dba2-116">Row</span><span class="sxs-lookup"><span data-stu-id="9dba2-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9dba2-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="9dba2-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9dba2-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9dba2-118">Attributes</span></span>

<span data-ttu-id="9dba2-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9dba2-119">None.</span></span>
  

