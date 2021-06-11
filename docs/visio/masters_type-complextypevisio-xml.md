---
title: Masters_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 8f1c660899e9109d946d41426b09e03d73ee76dd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538080"
---
# <a name="masters_type-complextype-visio-xml"></a><span data-ttu-id="d4f21-102">Masters_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d4f21-102">Masters_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d4f21-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="d4f21-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4f21-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d4f21-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d4f21-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d4f21-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d4f21-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d4f21-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d4f21-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="d4f21-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d4f21-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="d4f21-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d4f21-109">Définition</span><span class="sxs-lookup"><span data-stu-id="d4f21-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d4f21-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d4f21-110">Elements and attributes</span></span>

<span data-ttu-id="d4f21-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="d4f21-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d4f21-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d4f21-112">Child elements</span></span>

|<span data-ttu-id="d4f21-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d4f21-113">**Element**</span></span>|<span data-ttu-id="d4f21-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d4f21-114">**Type**</span></span>|<span data-ttu-id="d4f21-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="d4f21-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d4f21-116">Master</span><span class="sxs-lookup"><span data-stu-id="d4f21-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d4f21-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="d4f21-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d4f21-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="d4f21-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d4f21-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="d4f21-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d4f21-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="d4f21-120">Attributes</span></span>

<span data-ttu-id="d4f21-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d4f21-121">None.</span></span>
  

