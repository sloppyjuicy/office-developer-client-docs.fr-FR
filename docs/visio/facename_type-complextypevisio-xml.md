---
title: ComplexType FaceName_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322553"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="e5706-102">ComplexType FaceName_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e5706-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e5706-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e5706-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5706-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e5706-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e5706-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e5706-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e5706-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e5706-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e5706-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e5706-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e5706-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="e5706-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5706-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e5706-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e5706-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e5706-110">Elements and attributes</span></span>

<span data-ttu-id="e5706-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="e5706-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e5706-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e5706-112">Child elements</span></span>

<span data-ttu-id="e5706-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e5706-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5706-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="e5706-114">Attributes</span></span>

|<span data-ttu-id="e5706-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e5706-115">**Attribute**</span></span>|<span data-ttu-id="e5706-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="e5706-116">**Type**</span></span>|<span data-ttu-id="e5706-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e5706-117">**Required**</span></span>|<span data-ttu-id="e5706-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5706-118">**Description**</span></span>|<span data-ttu-id="e5706-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e5706-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e5706-120">Jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="e5706-120">CharSets</span></span>  <br/> |<span data-ttu-id="e5706-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5706-121">xsd:string</span></span>  <br/> |<span data-ttu-id="e5706-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5706-122">optional</span></span>  <br/> ||<span data-ttu-id="e5706-123">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5706-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5706-124">Flags</span><span class="sxs-lookup"><span data-stu-id="e5706-124">Flags</span></span>  <br/> |<span data-ttu-id="e5706-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e5706-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e5706-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5706-126">optional</span></span>  <br/> ||<span data-ttu-id="e5706-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e5706-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e5706-128">NameU</span><span class="sxs-lookup"><span data-stu-id="e5706-128">NameU</span></span>  <br/> |<span data-ttu-id="e5706-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5706-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e5706-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5706-130">required</span></span>  <br/> ||<span data-ttu-id="e5706-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5706-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5706-132">Panos</span><span class="sxs-lookup"><span data-stu-id="e5706-132">Panos</span></span>  <br/> |<span data-ttu-id="e5706-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5706-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e5706-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5706-134">optional</span></span>  <br/> ||<span data-ttu-id="e5706-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5706-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5706-136">PaNose</span><span class="sxs-lookup"><span data-stu-id="e5706-136">Panose</span></span>  <br/> |<span data-ttu-id="e5706-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5706-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e5706-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5706-138">optional</span></span>  <br/> ||<span data-ttu-id="e5706-139">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5706-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5706-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="e5706-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="e5706-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e5706-141">xsd:string</span></span>  <br/> |<span data-ttu-id="e5706-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="e5706-142">optional</span></span>  <br/> ||<span data-ttu-id="e5706-143">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e5706-143">Values of the xsd:string type.</span></span>  <br/> |
   

