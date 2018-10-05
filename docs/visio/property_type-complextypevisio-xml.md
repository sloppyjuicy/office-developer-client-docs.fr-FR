---
title: Type complexe Property_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: ada20c601fcd42bf551a0aea63787aac96062816
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383771"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="b9595-102">Type complexe Property_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="b9595-102">Property_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b9595-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="b9595-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9595-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="b9595-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b9595-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b9595-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b9595-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b9595-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b9595-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="b9595-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b9595-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b9595-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b9595-109">Définition</span><span class="sxs-lookup"><span data-stu-id="b9595-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b9595-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b9595-110">Elements and attributes</span></span>

<span data-ttu-id="b9595-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="b9595-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b9595-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b9595-112">Child elements</span></span>

|<span data-ttu-id="b9595-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b9595-113">**Element**</span></span>|<span data-ttu-id="b9595-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="b9595-114">**Type**</span></span>|<span data-ttu-id="b9595-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="b9595-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b9595-116">Row</span><span class="sxs-lookup"><span data-stu-id="b9595-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b9595-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="b9595-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b9595-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="b9595-118">Attributes</span></span>

<span data-ttu-id="b9595-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b9595-119">None.</span></span>
  

