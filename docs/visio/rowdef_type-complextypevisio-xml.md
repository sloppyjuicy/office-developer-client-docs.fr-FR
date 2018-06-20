---
title: Type complexe RowDef_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 4d751df50d4239263947a917cb16f2305cb06170
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789543"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="6f733-102">Type complexe RowDef_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="6f733-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6f733-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6f733-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f733-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="6f733-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6f733-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6f733-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6f733-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6f733-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6f733-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6f733-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6f733-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="6f733-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6f733-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6f733-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6f733-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6f733-110">Elements and attributes</span></span>

<span data-ttu-id="6f733-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="6f733-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6f733-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6f733-112">Child elements</span></span>

|<span data-ttu-id="6f733-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6f733-113">**Element**</span></span>|<span data-ttu-id="6f733-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="6f733-114">**Type**</span></span>|<span data-ttu-id="6f733-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6f733-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6f733-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="6f733-116">CellDef</span></span>](http://msdn.microsoft.com/library/f94c8227-020a-f613-3715-96a5eaaf14fb%28Office.15%29.aspx) <br/> |[<span data-ttu-id="6f733-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="6f733-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6f733-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="6f733-118">Attributes</span></span>

<span data-ttu-id="6f733-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6f733-119">None.</span></span>
  

