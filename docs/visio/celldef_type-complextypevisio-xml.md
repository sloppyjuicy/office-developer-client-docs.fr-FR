---
title: CellDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 7b437e35aadfef0390908cb1337cc738668382e5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542295"
---
# <a name="celldef_type-complextype-visio-xml"></a><span data-ttu-id="1cacc-102">CellDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1cacc-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1cacc-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1cacc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cacc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1cacc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1cacc-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1cacc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1cacc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1cacc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1cacc-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1cacc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1cacc-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="1cacc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1cacc-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1cacc-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1cacc-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1cacc-110">Elements and attributes</span></span>

<span data-ttu-id="1cacc-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="1cacc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1cacc-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1cacc-112">Child elements</span></span>

<span data-ttu-id="1cacc-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1cacc-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1cacc-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1cacc-114">Attributes</span></span>

|<span data-ttu-id="1cacc-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1cacc-115">**Attribute**</span></span>|<span data-ttu-id="1cacc-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="1cacc-116">**Type**</span></span>|<span data-ttu-id="1cacc-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1cacc-117">**Required**</span></span>|<span data-ttu-id="1cacc-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="1cacc-118">**Description**</span></span>|<span data-ttu-id="1cacc-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1cacc-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1cacc-120">F</span><span class="sxs-lookup"><span data-stu-id="1cacc-120">F</span></span>  <br/> |<span data-ttu-id="1cacc-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cacc-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1cacc-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="1cacc-122">optional</span></span>  <br/> ||<span data-ttu-id="1cacc-123">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cacc-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cacc-124">IX</span><span class="sxs-lookup"><span data-stu-id="1cacc-124">IX</span></span>  <br/> |<span data-ttu-id="1cacc-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="1cacc-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1cacc-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="1cacc-126">optional</span></span>  <br/> ||<span data-ttu-id="1cacc-127">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="1cacc-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1cacc-128">N</span><span class="sxs-lookup"><span data-stu-id="1cacc-128">N</span></span>  <br/> |<span data-ttu-id="1cacc-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cacc-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1cacc-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1cacc-130">required</span></span>  <br/> ||<span data-ttu-id="1cacc-131">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cacc-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cacc-132">S</span><span class="sxs-lookup"><span data-stu-id="1cacc-132">S</span></span>  <br/> |<span data-ttu-id="1cacc-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="1cacc-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1cacc-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="1cacc-134">optional</span></span>  <br/> ||<span data-ttu-id="1cacc-135">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="1cacc-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1cacc-136">T</span><span class="sxs-lookup"><span data-stu-id="1cacc-136">T</span></span>  <br/> |<span data-ttu-id="1cacc-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="1cacc-137">xsd:token</span></span>  <br/> |<span data-ttu-id="1cacc-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1cacc-138">required</span></span>  <br/> ||<span data-ttu-id="1cacc-139">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="1cacc-139">Values of the xsd:token type.</span></span>  <br/> |
   

