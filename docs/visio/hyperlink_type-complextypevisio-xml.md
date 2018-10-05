---
title: Type complexe Hyperlink_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 6c966447c13d90b05918138aeeafb11133e7bb5e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392031"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="28260-102">Type complexe Hyperlink_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="28260-102">Hyperlink_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="28260-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="28260-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28260-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="28260-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="28260-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="28260-105">**Schema file**</span></span> <br/> |<span data-ttu-id="28260-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="28260-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="28260-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="28260-107">**Extension base**</span></span> <br/> |<span data-ttu-id="28260-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="28260-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="28260-109">Définition</span><span class="sxs-lookup"><span data-stu-id="28260-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="28260-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="28260-110">Elements and attributes</span></span>

<span data-ttu-id="28260-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="28260-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="28260-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="28260-112">Child elements</span></span>

|<span data-ttu-id="28260-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="28260-113">**Element**</span></span>|<span data-ttu-id="28260-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="28260-114">**Type**</span></span>|<span data-ttu-id="28260-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="28260-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="28260-116">Row</span><span class="sxs-lookup"><span data-stu-id="28260-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="28260-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="28260-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="28260-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="28260-118">Attributes</span></span>

<span data-ttu-id="28260-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="28260-119">None.</span></span>
  

