---
title: ComplexType LineGradientRow_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: e48172e8213359244a61716d208b8b98776429af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361130"
---
# <a name="linegradientrowtype-complextype-visio-xml"></a><span data-ttu-id="eb4d5-102">ComplexType LineGradientRow_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="eb4d5-102">LineGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="eb4d5-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="eb4d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb4d5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eb4d5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eb4d5-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="eb4d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eb4d5-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="eb4d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eb4d5-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="eb4d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eb4d5-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="eb4d5-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eb4d5-109">Définition</span><span class="sxs-lookup"><span data-stu-id="eb4d5-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="eb4d5-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="eb4d5-110">Elements and attributes</span></span>

<span data-ttu-id="eb4d5-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="eb4d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eb4d5-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eb4d5-112">Child elements</span></span>

|<span data-ttu-id="eb4d5-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="eb4d5-113">**Element**</span></span>|<span data-ttu-id="eb4d5-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="eb4d5-114">**Type**</span></span>|<span data-ttu-id="eb4d5-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="eb4d5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eb4d5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="eb4d5-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="eb4d5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="eb4d5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="eb4d5-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="eb4d5-118">Attributes</span></span>

<span data-ttu-id="eb4d5-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eb4d5-119">None.</span></span>
  

