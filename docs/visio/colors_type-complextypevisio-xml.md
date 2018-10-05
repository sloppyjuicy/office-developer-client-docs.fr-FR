---
title: Type complexe Colors_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: e447ceb6fc0e6b79ec6e62b5f3b73a32cec589d9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400914"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="2e747-102">Type complexe Colors_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="2e747-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2e747-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="2e747-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e747-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2e747-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2e747-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2e747-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2e747-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2e747-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2e747-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="2e747-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2e747-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="2e747-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2e747-109">Définition</span><span class="sxs-lookup"><span data-stu-id="2e747-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2e747-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2e747-110">Elements and attributes</span></span>

<span data-ttu-id="2e747-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2e747-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2e747-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2e747-112">Child elements</span></span>

|<span data-ttu-id="2e747-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2e747-113">**Element**</span></span>|<span data-ttu-id="2e747-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="2e747-114">**Type**</span></span>|<span data-ttu-id="2e747-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e747-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2e747-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="2e747-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2e747-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="2e747-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2e747-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="2e747-118">Attributes</span></span>

<span data-ttu-id="2e747-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2e747-119">None.</span></span>
  

