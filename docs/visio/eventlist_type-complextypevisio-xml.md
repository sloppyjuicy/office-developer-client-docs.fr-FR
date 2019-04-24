---
title: ComplexType EventList_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351022"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="3cf9f-102">ComplexType EventList_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="3cf9f-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3cf9f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="3cf9f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cf9f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3cf9f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3cf9f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3cf9f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3cf9f-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="3cf9f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3cf9f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="3cf9f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3cf9f-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cf9f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3cf9f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="3cf9f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3cf9f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3cf9f-110">Elements and attributes</span></span>

<span data-ttu-id="3cf9f-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3cf9f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3cf9f-112">Child elements</span></span>

|<span data-ttu-id="3cf9f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3cf9f-113">**Element**</span></span>|<span data-ttu-id="3cf9f-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="3cf9f-114">**Type**</span></span>|<span data-ttu-id="3cf9f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="3cf9f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3cf9f-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="3cf9f-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3cf9f-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="3cf9f-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3cf9f-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="3cf9f-118">Attributes</span></span>

<span data-ttu-id="3cf9f-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-119">None.</span></span>
  

