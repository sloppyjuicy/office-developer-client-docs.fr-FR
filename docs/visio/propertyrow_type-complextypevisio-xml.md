---
title: ComplexType PropertyRow_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 813d6dee-b113-c0c9-3f53-c5bfd05b92f2
ms.openlocfilehash: fc59e95c8bb95932dd181b40a2e60dc6a3dac485
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326844"
---
# <a name="propertyrowtype-complextype-visio-xml"></a><span data-ttu-id="31d34-102">ComplexType PropertyRow_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="31d34-102">PropertyRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="31d34-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="31d34-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31d34-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="31d34-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="31d34-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="31d34-105">**Schema file**</span></span> <br/> |<span data-ttu-id="31d34-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="31d34-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="31d34-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="31d34-107">**Extension base**</span></span> <br/> |<span data-ttu-id="31d34-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="31d34-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31d34-109">Définition</span><span class="sxs-lookup"><span data-stu-id="31d34-109">Definition</span></span>

```XML
          <xs:complexType name="PropertyRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="31d34-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="31d34-110">Elements and attributes</span></span>

<span data-ttu-id="31d34-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="31d34-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="31d34-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31d34-112">Child elements</span></span>

|<span data-ttu-id="31d34-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="31d34-113">**Element**</span></span>|<span data-ttu-id="31d34-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="31d34-114">**Type**</span></span>|<span data-ttu-id="31d34-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="31d34-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="31d34-116">Cell</span><span class="sxs-lookup"><span data-stu-id="31d34-116">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="31d34-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="31d34-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="31d34-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="31d34-118">Attributes</span></span>

<span data-ttu-id="31d34-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="31d34-119">None.</span></span>
  

