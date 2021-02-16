---
title: SplineStart_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4395e39c-51bb-b232-bd8a-c5e53ae95169
ms.openlocfilehash: 11357b653ba8f4677a087ea269ed0975a9303f80
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541385"
---
# <a name="splinestart_type-complextype-visio-xml"></a><span data-ttu-id="f569b-102">SplineStart_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f569b-102">SplineStart_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f569b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f569b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f569b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f569b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f569b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f569b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f569b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f569b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f569b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f569b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f569b-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="f569b-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f569b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f569b-109">Definition</span></span>

```XML
          <xs:complexType name="SplineStart_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="f569b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f569b-110">Elements and attributes</span></span>

<span data-ttu-id="f569b-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="f569b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f569b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f569b-112">Child elements</span></span>

|<span data-ttu-id="f569b-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f569b-113">**Element**</span></span>|<span data-ttu-id="f569b-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f569b-114">**Type**</span></span>|<span data-ttu-id="f569b-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f569b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f569b-116">Cell</span><span class="sxs-lookup"><span data-stu-id="f569b-116">Cell</span></span>](cell-element-splinestart-rowvisio-xml.md) <br/> |[<span data-ttu-id="f569b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f569b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f569b-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="f569b-118">Attributes</span></span>

<span data-ttu-id="f569b-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f569b-119">None.</span></span>
  

