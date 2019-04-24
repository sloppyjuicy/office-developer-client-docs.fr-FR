---
title: ComplexType Connect_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 158fad1f3ec18bbc9565229338f4710c145c17e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327082"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="689b3-102">ComplexType Connect_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="689b3-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="689b3-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="689b3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="689b3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="689b3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="689b3-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="689b3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="689b3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="689b3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="689b3-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="689b3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="689b3-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="689b3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="689b3-109">Définition</span><span class="sxs-lookup"><span data-stu-id="689b3-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="689b3-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="689b3-110">Elements and attributes</span></span>

<span data-ttu-id="689b3-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="689b3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="689b3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="689b3-112">Child elements</span></span>

<span data-ttu-id="689b3-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="689b3-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="689b3-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="689b3-114">Attributes</span></span>

|<span data-ttu-id="689b3-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="689b3-115">**Attribute**</span></span>|<span data-ttu-id="689b3-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="689b3-116">**Type**</span></span>|<span data-ttu-id="689b3-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="689b3-117">**Required**</span></span>|<span data-ttu-id="689b3-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="689b3-118">**Description**</span></span>|<span data-ttu-id="689b3-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="689b3-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="689b3-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="689b3-120">FromCell</span></span>  <br/> |<span data-ttu-id="689b3-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="689b3-121">xsd:string</span></span>  <br/> |<span data-ttu-id="689b3-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="689b3-122">optional</span></span>  <br/> ||<span data-ttu-id="689b3-123">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="689b3-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="689b3-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="689b3-124">FromPart</span></span>  <br/> |<span data-ttu-id="689b3-125">xsd: int</span><span class="sxs-lookup"><span data-stu-id="689b3-125">xsd:int</span></span>  <br/> |<span data-ttu-id="689b3-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="689b3-126">optional</span></span>  <br/> ||<span data-ttu-id="689b3-127">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="689b3-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="689b3-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="689b3-128">FromSheet</span></span>  <br/> |<span data-ttu-id="689b3-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="689b3-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="689b3-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="689b3-130">required</span></span>  <br/> ||<span data-ttu-id="689b3-131">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="689b3-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="689b3-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="689b3-132">ToCell</span></span>  <br/> |<span data-ttu-id="689b3-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="689b3-133">xsd:string</span></span>  <br/> |<span data-ttu-id="689b3-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="689b3-134">optional</span></span>  <br/> ||<span data-ttu-id="689b3-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="689b3-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="689b3-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="689b3-136">ToPart</span></span>  <br/> |<span data-ttu-id="689b3-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="689b3-137">xsd:int</span></span>  <br/> |<span data-ttu-id="689b3-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="689b3-138">optional</span></span>  <br/> ||<span data-ttu-id="689b3-139">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="689b3-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="689b3-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="689b3-140">ToSheet</span></span>  <br/> |<span data-ttu-id="689b3-141">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="689b3-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="689b3-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="689b3-142">required</span></span>  <br/> ||<span data-ttu-id="689b3-143">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="689b3-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

