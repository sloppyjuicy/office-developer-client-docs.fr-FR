---
title: HyperlinkRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f8ded1a6-3bbd-0d59-c9f0-ab84341888cd
ms.openlocfilehash: 64705604ce12f032f49827b28fa3e61e879f2162
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541504"
---
# <a name="hyperlinkrow_type-complextype-visio-xml"></a><span data-ttu-id="658eb-102">HyperlinkRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="658eb-102">HyperlinkRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="658eb-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="658eb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="658eb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="658eb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="658eb-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="658eb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="658eb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="658eb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="658eb-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="658eb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="658eb-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="658eb-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="658eb-109">Définition</span><span class="sxs-lookup"><span data-stu-id="658eb-109">Definition</span></span>

```XML
          <xs:complexType name="HyperlinkRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="658eb-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="658eb-110">Elements and attributes</span></span>

<span data-ttu-id="658eb-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="658eb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="658eb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="658eb-112">Child elements</span></span>

|<span data-ttu-id="658eb-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="658eb-113">**Element**</span></span>|<span data-ttu-id="658eb-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="658eb-114">**Type**</span></span>|<span data-ttu-id="658eb-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="658eb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="658eb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="658eb-116">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="658eb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="658eb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="658eb-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="658eb-118">Attributes</span></span>

<span data-ttu-id="658eb-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="658eb-119">None.</span></span>
  

