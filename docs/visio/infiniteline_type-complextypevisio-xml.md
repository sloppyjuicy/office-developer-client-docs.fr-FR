---
title: Type complexe InfiniteLine_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4463d388-f5dd-4c43-71d4-82ba216d8d39
ms.openlocfilehash: 9e2b9146a875ecd32ccdc99e566a455aa36c2bf7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788841"
---
# <a name="infinitelinetype-complextype-visio-xml"></a><span data-ttu-id="23560-102">Type complexe InfiniteLine_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="23560-102">InfiniteLine_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="23560-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="23560-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23560-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="23560-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23560-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="23560-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23560-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23560-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23560-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="23560-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23560-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="23560-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23560-109">Définition</span><span class="sxs-lookup"><span data-stu-id="23560-109">Definition</span></span>

```XML
          <xs:complexType name="InfiniteLine_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="23560-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="23560-110">Elements and attributes</span></span>

<span data-ttu-id="23560-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="23560-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23560-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="23560-112">Child elements</span></span>

|<span data-ttu-id="23560-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="23560-113">**Element**</span></span>|<span data-ttu-id="23560-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="23560-114">**Type**</span></span>|<span data-ttu-id="23560-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="23560-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23560-116">Cell</span><span class="sxs-lookup"><span data-stu-id="23560-116">Cell</span></span>](cell-element-infiniteline-rowvisio-xml.md) <br/> |[<span data-ttu-id="23560-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="23560-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23560-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="23560-118">Attributes</span></span>

<span data-ttu-id="23560-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="23560-119">None.</span></span>
  

