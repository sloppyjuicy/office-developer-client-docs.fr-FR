---
title: ComplexType RowMap_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355733"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="f219f-102">ComplexType RowMap_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f219f-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f219f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f219f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f219f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f219f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f219f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f219f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f219f-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f219f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f219f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f219f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f219f-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="f219f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f219f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f219f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f219f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f219f-110">Elements and attributes</span></span>

<span data-ttu-id="f219f-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="f219f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f219f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f219f-112">Child elements</span></span>

<span data-ttu-id="f219f-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f219f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f219f-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="f219f-114">Attributes</span></span>

|<span data-ttu-id="f219f-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f219f-115">**Attribute**</span></span>|<span data-ttu-id="f219f-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="f219f-116">**Type**</span></span>|<span data-ttu-id="f219f-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f219f-117">**Required**</span></span>|<span data-ttu-id="f219f-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="f219f-118">**Description**</span></span>|<span data-ttu-id="f219f-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f219f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f219f-120">PageID</span><span class="sxs-lookup"><span data-stu-id="f219f-120">PageID</span></span>  <br/> |<span data-ttu-id="f219f-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f219f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f219f-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f219f-122">required</span></span>  <br/> ||<span data-ttu-id="f219f-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f219f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f219f-124">RowID</span><span class="sxs-lookup"><span data-stu-id="f219f-124">RowID</span></span>  <br/> |<span data-ttu-id="f219f-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f219f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f219f-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f219f-126">required</span></span>  <br/> ||<span data-ttu-id="f219f-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f219f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f219f-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="f219f-128">ShapeID</span></span>  <br/> |<span data-ttu-id="f219f-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f219f-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f219f-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f219f-130">required</span></span>  <br/> ||<span data-ttu-id="f219f-131">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f219f-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

