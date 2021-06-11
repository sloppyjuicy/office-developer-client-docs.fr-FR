---
title: LineGradient_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 6be5575336b3fb3ae014abd2685733ce4889f841
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541168"
---
# <a name="linegradient_type-complextype-visio-xml"></a><span data-ttu-id="407f8-102">LineGradient_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="407f8-102">LineGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="407f8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="407f8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="407f8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="407f8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="407f8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="407f8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="407f8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="407f8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="407f8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="407f8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="407f8-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="407f8-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="407f8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="407f8-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="407f8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="407f8-110">Elements and attributes</span></span>

<span data-ttu-id="407f8-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="407f8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="407f8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="407f8-112">Child elements</span></span>

|<span data-ttu-id="407f8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="407f8-113">**Element**</span></span>|<span data-ttu-id="407f8-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="407f8-114">**Type**</span></span>|<span data-ttu-id="407f8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="407f8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="407f8-116">Row</span><span class="sxs-lookup"><span data-stu-id="407f8-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="407f8-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="407f8-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="407f8-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="407f8-118">Attributes</span></span>

<span data-ttu-id="407f8-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="407f8-119">None.</span></span>
  

