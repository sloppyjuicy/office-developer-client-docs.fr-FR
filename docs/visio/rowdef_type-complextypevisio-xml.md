---
title: Type complexe RowDef_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: e097e740b543661e5c49a81d75c047c8749ce1d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564254"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="ccb6c-102">Type complexe RowDef_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ccb6c-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ccb6c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccb6c-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ccb6c-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ccb6c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ccb6c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ccb6c-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ccb6c-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="ccb6c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ccb6c-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ccb6c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ccb6c-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ccb6c-110">Elements and attributes</span></span>

<span data-ttu-id="ccb6c-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ccb6c-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ccb6c-112">Child elements</span></span>

|<span data-ttu-id="ccb6c-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-113">**Element**</span></span>|<span data-ttu-id="ccb6c-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-114">**Type**</span></span>|<span data-ttu-id="ccb6c-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccb6c-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="ccb6c-116">CellDef</span></span> <br/> |[<span data-ttu-id="ccb6c-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="ccb6c-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ccb6c-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="ccb6c-118">Attributes</span></span>

<span data-ttu-id="ccb6c-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-119">None.</span></span>
  

