---
title: ComplexType Hyperlink_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: ce9a1f5b9a6e402ec157d641f81a82c6df4b92e1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541553"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="9414b-102">ComplexType Hyperlink_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9414b-102">Hyperlink_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9414b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9414b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9414b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9414b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9414b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9414b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9414b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9414b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9414b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9414b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9414b-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9414b-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9414b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9414b-109">Definition</span></span>

```XML
          <xs:complexType name="Hyperlink_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="HyperlinkRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9414b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9414b-110">Elements and attributes</span></span>

<span data-ttu-id="9414b-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="9414b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9414b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9414b-112">Child elements</span></span>

|<span data-ttu-id="9414b-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9414b-113">**Element**</span></span>|<span data-ttu-id="9414b-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="9414b-114">**Type**</span></span>|<span data-ttu-id="9414b-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9414b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9414b-116">Row</span><span class="sxs-lookup"><span data-stu-id="9414b-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9414b-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="9414b-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9414b-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9414b-118">Attributes</span></span>

<span data-ttu-id="9414b-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9414b-119">None.</span></span>
  

