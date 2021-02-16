---
title: NURBSTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7ae8a1d-5bb7-a92f-79d6-5a358d879c32
ms.openlocfilehash: 090df2487eb6fabfba4b3917c7d938fe4f841147
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540916"
---
# <a name="nurbsto_type-complextype-visio-xml"></a><span data-ttu-id="460fb-102">NURBSTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="460fb-102">NURBSTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="460fb-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="460fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="460fb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="460fb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="460fb-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="460fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="460fb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="460fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="460fb-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="460fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="460fb-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="460fb-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="460fb-109">Définition</span><span class="sxs-lookup"><span data-stu-id="460fb-109">Definition</span></span>

```XML
          <xs:complexType name="NURBSTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="460fb-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="460fb-110">Elements and attributes</span></span>

<span data-ttu-id="460fb-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="460fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="460fb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="460fb-112">Child elements</span></span>

|<span data-ttu-id="460fb-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="460fb-113">**Element**</span></span>|<span data-ttu-id="460fb-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="460fb-114">**Type**</span></span>|<span data-ttu-id="460fb-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="460fb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="460fb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="460fb-116">Cell</span></span>](cell-element-nurbsto-rowvisio-xml.md) <br/> |[<span data-ttu-id="460fb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="460fb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="460fb-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="460fb-118">Attributes</span></span>

<span data-ttu-id="460fb-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="460fb-119">None.</span></span>
  

