---
title: Type complexe ScratchRow_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: 74f106f34596ca4ff2c200e0127155f4df54da28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391464"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="fdecf-102">Type complexe ScratchRow_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="fdecf-102">ScratchRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fdecf-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="fdecf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fdecf-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="fdecf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fdecf-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fdecf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fdecf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fdecf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fdecf-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="fdecf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fdecf-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="fdecf-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fdecf-109">Définition</span><span class="sxs-lookup"><span data-stu-id="fdecf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fdecf-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fdecf-110">Elements and attributes</span></span>

<span data-ttu-id="fdecf-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="fdecf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fdecf-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fdecf-112">Child elements</span></span>

|<span data-ttu-id="fdecf-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fdecf-113">**Element**</span></span>|<span data-ttu-id="fdecf-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="fdecf-114">**Type**</span></span>|<span data-ttu-id="fdecf-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="fdecf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fdecf-116">Cell</span><span class="sxs-lookup"><span data-stu-id="fdecf-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="fdecf-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fdecf-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fdecf-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="fdecf-118">Attributes</span></span>

<span data-ttu-id="fdecf-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fdecf-119">None.</span></span>
  

