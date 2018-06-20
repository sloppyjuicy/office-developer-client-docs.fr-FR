---
title: Type complexe Colors_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: 187d51c2102e9d13ffea15c6de2db849ef980fb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788262"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="c9342-102">Type complexe Colors_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c9342-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c9342-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c9342-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9342-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c9342-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c9342-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c9342-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c9342-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c9342-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c9342-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c9342-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c9342-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="c9342-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9342-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c9342-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c9342-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c9342-110">Elements and attributes</span></span>

<span data-ttu-id="c9342-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c9342-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c9342-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c9342-112">Child elements</span></span>

|<span data-ttu-id="c9342-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c9342-113">**Element**</span></span>|<span data-ttu-id="c9342-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c9342-114">**Type**</span></span>|<span data-ttu-id="c9342-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c9342-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c9342-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="c9342-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9342-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="c9342-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c9342-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c9342-118">Attributes</span></span>

<span data-ttu-id="c9342-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c9342-119">None.</span></span>
  

