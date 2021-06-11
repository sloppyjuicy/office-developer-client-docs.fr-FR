---
title: RowMap_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 8564f5a063ac2365de50919168df0b84e8ae100a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538773"
---
# <a name="rowmap_type-complextype-visio-xml"></a><span data-ttu-id="ba64d-102">RowMap_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ba64d-102">RowMap_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ba64d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ba64d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba64d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ba64d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ba64d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ba64d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ba64d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ba64d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ba64d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ba64d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ba64d-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="ba64d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ba64d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ba64d-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ba64d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ba64d-110">Elements and attributes</span></span>

<span data-ttu-id="ba64d-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="ba64d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ba64d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ba64d-112">Child elements</span></span>

<span data-ttu-id="ba64d-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ba64d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba64d-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="ba64d-114">Attributes</span></span>

|<span data-ttu-id="ba64d-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ba64d-115">**Attribute**</span></span>|<span data-ttu-id="ba64d-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="ba64d-116">**Type**</span></span>|<span data-ttu-id="ba64d-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ba64d-117">**Required**</span></span>|<span data-ttu-id="ba64d-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="ba64d-118">**Description**</span></span>|<span data-ttu-id="ba64d-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ba64d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ba64d-120">PageID</span><span class="sxs-lookup"><span data-stu-id="ba64d-120">PageID</span></span>  <br/> |<span data-ttu-id="ba64d-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ba64d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ba64d-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ba64d-122">required</span></span>  <br/> ||<span data-ttu-id="ba64d-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ba64d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ba64d-124">RowID</span><span class="sxs-lookup"><span data-stu-id="ba64d-124">RowID</span></span>  <br/> |<span data-ttu-id="ba64d-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ba64d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ba64d-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ba64d-126">required</span></span>  <br/> ||<span data-ttu-id="ba64d-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ba64d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ba64d-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="ba64d-128">ShapeID</span></span>  <br/> |<span data-ttu-id="ba64d-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ba64d-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ba64d-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ba64d-130">required</span></span>  <br/> ||<span data-ttu-id="ba64d-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ba64d-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

