---
title: ComplexType StyleSheet_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329824"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="025e4-102">ComplexType StyleSheet_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="025e4-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="025e4-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="025e4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="025e4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="025e4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="025e4-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="025e4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="025e4-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="025e4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="025e4-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="025e4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="025e4-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="025e4-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="025e4-109">Définition</span><span class="sxs-lookup"><span data-stu-id="025e4-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="025e4-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="025e4-110">Elements and attributes</span></span>

<span data-ttu-id="025e4-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="025e4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="025e4-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="025e4-112">Child elements</span></span>

<span data-ttu-id="025e4-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="025e4-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="025e4-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="025e4-114">Attributes</span></span>

|<span data-ttu-id="025e4-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="025e4-115">**Attribute**</span></span>|<span data-ttu-id="025e4-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="025e4-116">**Type**</span></span>|<span data-ttu-id="025e4-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="025e4-117">**Required**</span></span>|<span data-ttu-id="025e4-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="025e4-118">**Description**</span></span>|<span data-ttu-id="025e4-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="025e4-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="025e4-120">ID</span><span class="sxs-lookup"><span data-stu-id="025e4-120">ID</span></span>  <br/> |<span data-ttu-id="025e4-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="025e4-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="025e4-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="025e4-122">required</span></span>  <br/> ||<span data-ttu-id="025e4-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="025e4-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="025e4-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="025e4-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="025e4-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="025e4-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="025e4-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="025e4-126">optional</span></span>  <br/> ||<span data-ttu-id="025e4-127">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="025e4-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="025e4-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="025e4-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="025e4-129">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="025e4-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="025e4-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="025e4-130">optional</span></span>  <br/> ||<span data-ttu-id="025e4-131">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="025e4-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="025e4-132">Nom</span><span class="sxs-lookup"><span data-stu-id="025e4-132">Name</span></span>  <br/> |<span data-ttu-id="025e4-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="025e4-133">xsd:string</span></span>  <br/> |<span data-ttu-id="025e4-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="025e4-134">optional</span></span>  <br/> ||<span data-ttu-id="025e4-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="025e4-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="025e4-136">NameU</span><span class="sxs-lookup"><span data-stu-id="025e4-136">NameU</span></span>  <br/> |<span data-ttu-id="025e4-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="025e4-137">xsd:string</span></span>  <br/> |<span data-ttu-id="025e4-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="025e4-138">optional</span></span>  <br/> ||<span data-ttu-id="025e4-139">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="025e4-139">Values of the xsd:string type.</span></span>  <br/> |
   

