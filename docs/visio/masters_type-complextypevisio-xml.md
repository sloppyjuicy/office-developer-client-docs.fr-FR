---
title: Type complexe Masters_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: ee53a4c5ce07151b0ba58ebe08a4b69cca12d313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789073"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="b1594-102">Type complexe Masters_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="b1594-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b1594-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="b1594-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1594-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="b1594-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b1594-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b1594-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b1594-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b1594-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b1594-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="b1594-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b1594-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="b1594-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b1594-109">Définition</span><span class="sxs-lookup"><span data-stu-id="b1594-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b1594-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b1594-110">Elements and attributes</span></span>

<span data-ttu-id="b1594-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="b1594-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b1594-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b1594-112">Child elements</span></span>

|<span data-ttu-id="b1594-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b1594-113">**Element**</span></span>|<span data-ttu-id="b1594-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="b1594-114">**Type**</span></span>|<span data-ttu-id="b1594-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="b1594-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b1594-116">Forme de base</span><span class="sxs-lookup"><span data-stu-id="b1594-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1594-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="b1594-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b1594-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="b1594-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1594-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="b1594-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b1594-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="b1594-120">Attributes</span></span>

<span data-ttu-id="b1594-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b1594-121">None.</span></span>
  

