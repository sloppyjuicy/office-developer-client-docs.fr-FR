---
title: ComplexType Masters_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341656"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="5126e-102">ComplexType Masters_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5126e-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5126e-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="5126e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5126e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5126e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5126e-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5126e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5126e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="5126e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5126e-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="5126e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5126e-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="5126e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5126e-109">Définition</span><span class="sxs-lookup"><span data-stu-id="5126e-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5126e-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5126e-110">Elements and attributes</span></span>

<span data-ttu-id="5126e-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="5126e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5126e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5126e-112">Child elements</span></span>

|<span data-ttu-id="5126e-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5126e-113">**Element**</span></span>|<span data-ttu-id="5126e-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="5126e-114">**Type**</span></span>|<span data-ttu-id="5126e-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="5126e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5126e-116">Master</span><span class="sxs-lookup"><span data-stu-id="5126e-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5126e-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="5126e-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5126e-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="5126e-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5126e-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="5126e-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5126e-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="5126e-120">Attributes</span></span>

<span data-ttu-id="5126e-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5126e-121">None.</span></span>
  

