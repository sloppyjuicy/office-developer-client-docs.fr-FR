---
title: Type complexe RelCubBezTo_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 004dc563-d089-230f-0055-038b72eebbed
ms.openlocfilehash: 6ec426ef2c7afd913d904c8ceba938549727c799
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389448"
---
# <a name="relcubbeztotype-complextype-visio-xml"></a><span data-ttu-id="e51e3-102">Type complexe RelCubBezTo_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e51e3-102">RelCubBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e51e3-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e51e3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e51e3-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e51e3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e51e3-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e51e3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e51e3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e51e3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e51e3-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e51e3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e51e3-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="e51e3-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e51e3-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e51e3-109">Definition</span></span>

```XML
          <xs:complexType name="RelCubBezTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="e51e3-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e51e3-110">Elements and attributes</span></span>

<span data-ttu-id="e51e3-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e51e3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e51e3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e51e3-112">Child elements</span></span>

|<span data-ttu-id="e51e3-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e51e3-113">**Element**</span></span>|<span data-ttu-id="e51e3-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="e51e3-114">**Type**</span></span>|<span data-ttu-id="e51e3-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="e51e3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e51e3-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e51e3-116">Cell</span></span>](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="e51e3-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e51e3-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e51e3-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="e51e3-118">Attributes</span></span>

<span data-ttu-id="e51e3-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e51e3-119">None.</span></span>
  

