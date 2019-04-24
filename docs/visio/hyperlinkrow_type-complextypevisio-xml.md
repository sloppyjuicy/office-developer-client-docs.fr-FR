---
title: ComplexType HyperlinkRow_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f8ded1a6-3bbd-0d59-c9f0-ab84341888cd
ms.openlocfilehash: 0056c87f4926f440ffcfd85619fd5ab7cba308db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344834"
---
# <a name="hyperlinkrowtype-complextype-visio-xml"></a><span data-ttu-id="c931a-102">ComplexType HyperlinkRow_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c931a-102">HyperlinkRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c931a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c931a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c931a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c931a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c931a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c931a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c931a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c931a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c931a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c931a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c931a-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="c931a-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c931a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c931a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c931a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c931a-110">Elements and attributes</span></span>

<span data-ttu-id="c931a-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="c931a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c931a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c931a-112">Child elements</span></span>

|<span data-ttu-id="c931a-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c931a-113">**Element**</span></span>|<span data-ttu-id="c931a-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c931a-114">**Type**</span></span>|<span data-ttu-id="c931a-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c931a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c931a-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c931a-116">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="c931a-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c931a-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c931a-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c931a-118">Attributes</span></span>

<span data-ttu-id="c931a-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c931a-119">None.</span></span>
  

