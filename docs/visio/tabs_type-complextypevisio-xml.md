---
title: ComplexType Tabs_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b97155ce-f0d2-e35c-bc58-e288f653ce2c
ms.openlocfilehash: ea55169051c66f7434a1e1ba11ff5a23dee0e9c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358862"
---
# <a name="tabstype-complextype-visio-xml"></a><span data-ttu-id="31e82-102">ComplexType Tabs_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="31e82-102">Tabs_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="31e82-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="31e82-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31e82-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="31e82-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="31e82-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="31e82-105">**Schema file**</span></span> <br/> |<span data-ttu-id="31e82-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="31e82-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="31e82-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="31e82-107">**Extension base**</span></span> <br/> |<span data-ttu-id="31e82-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="31e82-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31e82-109">Définition</span><span class="sxs-lookup"><span data-stu-id="31e82-109">Definition</span></span>

```XML
          <xs:complexType name="Tabs_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="TabsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="31e82-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="31e82-110">Elements and attributes</span></span>

<span data-ttu-id="31e82-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="31e82-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="31e82-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31e82-112">Child elements</span></span>

|<span data-ttu-id="31e82-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="31e82-113">**Element**</span></span>|<span data-ttu-id="31e82-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="31e82-114">**Type**</span></span>|<span data-ttu-id="31e82-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="31e82-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="31e82-116">Row</span><span class="sxs-lookup"><span data-stu-id="31e82-116">Row</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="31e82-117">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="31e82-117">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="31e82-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="31e82-118">Attributes</span></span>

<span data-ttu-id="31e82-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="31e82-119">None.</span></span>
  

