---
title: Type complexe ActionTagRow_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d42c212-b068-84fa-e271-bbe1fae52a48
ms.openlocfilehash: 8caef77494efa99df8f681deb1268dfee95f03cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398996"
---
# <a name="actiontagrowtype-complextype-visio-xml"></a><span data-ttu-id="c8d1c-102">Type complexe ActionTagRow_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c8d1c-102">ActionTagRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c8d1c-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c8d1c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8d1c-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c8d1c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c8d1c-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c8d1c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c8d1c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c8d1c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c8d1c-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c8d1c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c8d1c-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="c8d1c-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8d1c-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c8d1c-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTagRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="c8d1c-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c8d1c-110">Elements and attributes</span></span>

<span data-ttu-id="c8d1c-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c8d1c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c8d1c-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c8d1c-112">Child elements</span></span>

|<span data-ttu-id="c8d1c-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c8d1c-113">**Element**</span></span>|<span data-ttu-id="c8d1c-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c8d1c-114">**Type**</span></span>|<span data-ttu-id="c8d1c-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8d1c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8d1c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c8d1c-116">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c8d1c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c8d1c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c8d1c-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c8d1c-118">Attributes</span></span>

<span data-ttu-id="c8d1c-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c8d1c-119">None.</span></span>
  

