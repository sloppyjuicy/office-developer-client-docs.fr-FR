---
title: StyleSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 6dcb6bbfd01c37b499dfca4d54d6cb0832e59b5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541980"
---
# <a name="stylesheet_type-complextype-visio-xml"></a><span data-ttu-id="8024a-102">StyleSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8024a-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8024a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="8024a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8024a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8024a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8024a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="8024a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8024a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8024a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8024a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="8024a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8024a-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="8024a-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8024a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="8024a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8024a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="8024a-110">Elements and attributes</span></span>

<span data-ttu-id="8024a-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="8024a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8024a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8024a-112">Child elements</span></span>

<span data-ttu-id="8024a-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8024a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8024a-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="8024a-114">Attributes</span></span>

|<span data-ttu-id="8024a-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8024a-115">**Attribute**</span></span>|<span data-ttu-id="8024a-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="8024a-116">**Type**</span></span>|<span data-ttu-id="8024a-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8024a-117">**Required**</span></span>|<span data-ttu-id="8024a-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="8024a-118">**Description**</span></span>|<span data-ttu-id="8024a-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8024a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8024a-120">ID</span><span class="sxs-lookup"><span data-stu-id="8024a-120">ID</span></span>  <br/> |<span data-ttu-id="8024a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8024a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8024a-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8024a-122">required</span></span>  <br/> ||<span data-ttu-id="8024a-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8024a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8024a-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="8024a-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="8024a-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8024a-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8024a-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="8024a-126">optional</span></span>  <br/> ||<span data-ttu-id="8024a-127">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8024a-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8024a-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="8024a-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="8024a-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8024a-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8024a-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="8024a-130">optional</span></span>  <br/> ||<span data-ttu-id="8024a-131">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8024a-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8024a-132">Nom</span><span class="sxs-lookup"><span data-stu-id="8024a-132">Name</span></span>  <br/> |<span data-ttu-id="8024a-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8024a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="8024a-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="8024a-134">optional</span></span>  <br/> ||<span data-ttu-id="8024a-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8024a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8024a-136">NameU</span><span class="sxs-lookup"><span data-stu-id="8024a-136">NameU</span></span>  <br/> |<span data-ttu-id="8024a-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8024a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8024a-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="8024a-138">optional</span></span>  <br/> ||<span data-ttu-id="8024a-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8024a-139">Values of the xsd:string type.</span></span>  <br/> |
   

