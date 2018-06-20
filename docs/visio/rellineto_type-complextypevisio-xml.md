---
title: Type complexe RelLineTo_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e5504166-653d-15d2-75eb-9b36f376b788
ms.openlocfilehash: 953130a69e477aeef836aa8b95d3979e84e8ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789434"
---
# <a name="rellinetotype-complextype-visio-xml"></a><span data-ttu-id="1fbb2-102">Type complexe RelLineTo_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1fbb2-102">RelLineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1fbb2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1fbb2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fbb2-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1fbb2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1fbb2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1fbb2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1fbb2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1fbb2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1fbb2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1fbb2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1fbb2-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="1fbb2-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1fbb2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1fbb2-109">Definition</span></span>

```XML
          <xs:complexType name="RelLineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="1fbb2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1fbb2-110">Elements and attributes</span></span>

<span data-ttu-id="1fbb2-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1fbb2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1fbb2-112">Child elements</span></span>

|<span data-ttu-id="1fbb2-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1fbb2-113">**Element**</span></span>|<span data-ttu-id="1fbb2-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="1fbb2-114">**Type**</span></span>|<span data-ttu-id="1fbb2-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="1fbb2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1fbb2-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1fbb2-116">Cell</span></span>](cell-element-rellineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="1fbb2-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1fbb2-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1fbb2-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="1fbb2-118">Attributes</span></span>

<span data-ttu-id="1fbb2-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-119">None.</span></span>
  

