---
title: ComplexType CellDef_Type (Visio XML)
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
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="7ebdb-102">ComplexType CellDef_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7ebdb-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7ebdb-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7ebdb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ebdb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7ebdb-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7ebdb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7ebdb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7ebdb-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7ebdb-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="7ebdb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7ebdb-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7ebdb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7ebdb-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7ebdb-110">Elements and attributes</span></span>

<span data-ttu-id="7ebdb-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="7ebdb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7ebdb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7ebdb-112">Child elements</span></span>

<span data-ttu-id="7ebdb-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7ebdb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ebdb-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="7ebdb-114">Attributes</span></span>

|<span data-ttu-id="7ebdb-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-115">**Attribute**</span></span>|<span data-ttu-id="7ebdb-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-116">**Type**</span></span>|<span data-ttu-id="7ebdb-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-117">**Required**</span></span>|<span data-ttu-id="7ebdb-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-118">**Description**</span></span>|<span data-ttu-id="7ebdb-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7ebdb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7ebdb-120">F</span><span class="sxs-lookup"><span data-stu-id="7ebdb-120">F</span></span>  <br/> |<span data-ttu-id="7ebdb-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7ebdb-121">xsd:string</span></span>  <br/> |<span data-ttu-id="7ebdb-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="7ebdb-122">optional</span></span>  <br/> ||<span data-ttu-id="7ebdb-123">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7ebdb-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7ebdb-124">IX</span><span class="sxs-lookup"><span data-stu-id="7ebdb-124">IX</span></span>  <br/> |<span data-ttu-id="7ebdb-125">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7ebdb-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7ebdb-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="7ebdb-126">optional</span></span>  <br/> ||<span data-ttu-id="7ebdb-127">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7ebdb-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7ebdb-128">N</span><span class="sxs-lookup"><span data-stu-id="7ebdb-128">N</span></span>  <br/> |<span data-ttu-id="7ebdb-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7ebdb-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7ebdb-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ebdb-130">required</span></span>  <br/> ||<span data-ttu-id="7ebdb-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7ebdb-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7ebdb-132">S</span><span class="sxs-lookup"><span data-stu-id="7ebdb-132">S</span></span>  <br/> |<span data-ttu-id="7ebdb-133">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7ebdb-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7ebdb-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="7ebdb-134">optional</span></span>  <br/> ||<span data-ttu-id="7ebdb-135">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="7ebdb-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7ebdb-136">T</span><span class="sxs-lookup"><span data-stu-id="7ebdb-136">T</span></span>  <br/> |<span data-ttu-id="7ebdb-137">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="7ebdb-137">xsd:token</span></span>  <br/> |<span data-ttu-id="7ebdb-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7ebdb-138">required</span></span>  <br/> ||<span data-ttu-id="7ebdb-139">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="7ebdb-139">Values of the xsd:token type.</span></span>  <br/> |
   

