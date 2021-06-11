---
title: CharacterRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61c99712-d451-408a-de15-fb088605b07c
ms.openlocfilehash: 3d54921ca571ff3ba4643b2e1d18ee9d7d1bc8c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540195"
---
# <a name="characterrow_type-complextype-visio-xml"></a><span data-ttu-id="abfd2-102">CharacterRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="abfd2-102">CharacterRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="abfd2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="abfd2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abfd2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="abfd2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="abfd2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="abfd2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="abfd2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="abfd2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="abfd2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="abfd2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="abfd2-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="abfd2-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="abfd2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="abfd2-109">Definition</span></span>

```XML
          <xs:complexType name="CharacterRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="abfd2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="abfd2-110">Elements and attributes</span></span>

<span data-ttu-id="abfd2-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="abfd2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="abfd2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="abfd2-112">Child elements</span></span>

|<span data-ttu-id="abfd2-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="abfd2-113">**Element**</span></span>|<span data-ttu-id="abfd2-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="abfd2-114">**Type**</span></span>|<span data-ttu-id="abfd2-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="abfd2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="abfd2-116">Cell</span><span class="sxs-lookup"><span data-stu-id="abfd2-116">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="abfd2-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="abfd2-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="abfd2-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="abfd2-118">Attributes</span></span>

<span data-ttu-id="abfd2-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="abfd2-119">None.</span></span>
  

