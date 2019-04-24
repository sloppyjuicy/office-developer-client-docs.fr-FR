---
title: ComplexType DocumentSheet_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326137"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="1c0bd-102">ComplexType DocumentSheet_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1c0bd-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1c0bd-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1c0bd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c0bd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1c0bd-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1c0bd-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1c0bd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1c0bd-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1c0bd-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="1c0bd-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c0bd-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1c0bd-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1c0bd-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1c0bd-110">Elements and attributes</span></span>

<span data-ttu-id="1c0bd-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="1c0bd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1c0bd-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1c0bd-112">Child elements</span></span>

<span data-ttu-id="1c0bd-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1c0bd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c0bd-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1c0bd-114">Attributes</span></span>

|<span data-ttu-id="1c0bd-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-115">**Attribute**</span></span>|<span data-ttu-id="1c0bd-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-116">**Type**</span></span>|<span data-ttu-id="1c0bd-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-117">**Required**</span></span>|<span data-ttu-id="1c0bd-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-118">**Description**</span></span>|<span data-ttu-id="1c0bd-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1c0bd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c0bd-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="1c0bd-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="1c0bd-121">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="1c0bd-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1c0bd-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="1c0bd-122">optional</span></span>  <br/> ||<span data-ttu-id="1c0bd-123">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="1c0bd-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1c0bd-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="1c0bd-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="1c0bd-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="1c0bd-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1c0bd-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="1c0bd-126">optional</span></span>  <br/> ||<span data-ttu-id="1c0bd-127">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="1c0bd-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1c0bd-128">Nom</span><span class="sxs-lookup"><span data-stu-id="1c0bd-128">Name</span></span>  <br/> |<span data-ttu-id="1c0bd-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1c0bd-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1c0bd-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="1c0bd-130">optional</span></span>  <br/> ||<span data-ttu-id="1c0bd-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1c0bd-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c0bd-132">NameU</span><span class="sxs-lookup"><span data-stu-id="1c0bd-132">NameU</span></span>  <br/> |<span data-ttu-id="1c0bd-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1c0bd-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1c0bd-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="1c0bd-134">optional</span></span>  <br/> ||<span data-ttu-id="1c0bd-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1c0bd-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c0bd-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="1c0bd-136">UniqueID</span></span>  <br/> |<span data-ttu-id="1c0bd-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1c0bd-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1c0bd-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="1c0bd-138">optional</span></span>  <br/> ||<span data-ttu-id="1c0bd-139">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1c0bd-139">Values of the xsd:string type.</span></span>  <br/> |
   

