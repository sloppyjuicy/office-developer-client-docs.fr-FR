---
title: Type complexe EventList_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392080"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="73858-102">Type complexe EventList_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="73858-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="73858-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="73858-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73858-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="73858-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="73858-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="73858-105">**Schema file**</span></span> <br/> |<span data-ttu-id="73858-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="73858-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="73858-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="73858-107">**Extension base**</span></span> <br/> |<span data-ttu-id="73858-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="73858-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73858-109">Définition</span><span class="sxs-lookup"><span data-stu-id="73858-109">Definition</span></span>

```XML
          <xs:complexType name="EventList_Type">
          
          <xs:sequence>
    <xs:element name="EventItem"  type="EventItem_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="73858-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="73858-110">Elements and attributes</span></span>

<span data-ttu-id="73858-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="73858-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="73858-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="73858-112">Child elements</span></span>

|<span data-ttu-id="73858-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="73858-113">**Element**</span></span>|<span data-ttu-id="73858-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="73858-114">**Type**</span></span>|<span data-ttu-id="73858-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="73858-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="73858-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="73858-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="73858-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="73858-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="73858-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="73858-118">Attributes</span></span>

<span data-ttu-id="73858-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="73858-119">None.</span></span>
  

