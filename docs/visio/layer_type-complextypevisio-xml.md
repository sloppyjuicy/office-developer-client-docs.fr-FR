---
title: ComplexType Layer_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f92ac1cc-fad2-dab9-5507-838c006ed633
ms.openlocfilehash: 1614a2eb8606144d28fc0422d9fc2c44c48910d1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541287"
---
# <a name="layertype-complextype-visio-xml"></a><span data-ttu-id="bc0f3-102">ComplexType Layer_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bc0f3-102">Layer_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bc0f3-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="bc0f3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc0f3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bc0f3-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bc0f3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="bc0f3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bc0f3-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bc0f3-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="bc0f3-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bc0f3-109">Définition</span><span class="sxs-lookup"><span data-stu-id="bc0f3-109">Definition</span></span>

```XML
          <xs:complexType name="Layer_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LayerRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bc0f3-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="bc0f3-110">Elements and attributes</span></span>

<span data-ttu-id="bc0f3-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bc0f3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bc0f3-112">Child elements</span></span>

|<span data-ttu-id="bc0f3-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-113">**Element**</span></span>|<span data-ttu-id="bc0f3-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-114">**Type**</span></span>|<span data-ttu-id="bc0f3-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bc0f3-116">Row</span><span class="sxs-lookup"><span data-stu-id="bc0f3-116">Row</span></span>](row-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="bc0f3-117">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="bc0f3-117">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bc0f3-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="bc0f3-118">Attributes</span></span>

<span data-ttu-id="bc0f3-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-119">None.</span></span>
  

