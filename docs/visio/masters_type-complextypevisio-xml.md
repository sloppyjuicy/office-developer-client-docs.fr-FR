---
title: Type complexe Masters_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398492"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="eaae5-102">Type complexe Masters_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="eaae5-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="eaae5-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="eaae5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eaae5-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="eaae5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eaae5-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="eaae5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eaae5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="eaae5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eaae5-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="eaae5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eaae5-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="eaae5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eaae5-109">Définition</span><span class="sxs-lookup"><span data-stu-id="eaae5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="eaae5-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="eaae5-110">Elements and attributes</span></span>

<span data-ttu-id="eaae5-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="eaae5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eaae5-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eaae5-112">Child elements</span></span>

|<span data-ttu-id="eaae5-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="eaae5-113">**Element**</span></span>|<span data-ttu-id="eaae5-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="eaae5-114">**Type**</span></span>|<span data-ttu-id="eaae5-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="eaae5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eaae5-116">Forme de base</span><span class="sxs-lookup"><span data-stu-id="eaae5-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eaae5-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="eaae5-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="eaae5-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="eaae5-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eaae5-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="eaae5-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="eaae5-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="eaae5-120">Attributes</span></span>

<span data-ttu-id="eaae5-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eaae5-121">None.</span></span>
  

