---
title: ValidationProperties_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: d83a1ce8e7ad89155726200de2950da755e5d3db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538514"
---
# <a name="validationproperties_type-complextype-visio-xml"></a><span data-ttu-id="183cd-102">ValidationProperties_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="183cd-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="183cd-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="183cd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="183cd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="183cd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="183cd-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="183cd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="183cd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="183cd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="183cd-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="183cd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="183cd-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="183cd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="183cd-109">Définition</span><span class="sxs-lookup"><span data-stu-id="183cd-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="183cd-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="183cd-110">Elements and attributes</span></span>

<span data-ttu-id="183cd-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="183cd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="183cd-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="183cd-112">Child elements</span></span>

<span data-ttu-id="183cd-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="183cd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="183cd-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="183cd-114">Attributes</span></span>

|<span data-ttu-id="183cd-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="183cd-115">**Attribute**</span></span>|<span data-ttu-id="183cd-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="183cd-116">**Type**</span></span>|<span data-ttu-id="183cd-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="183cd-117">**Required**</span></span>|<span data-ttu-id="183cd-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="183cd-118">**Description**</span></span>|<span data-ttu-id="183cd-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="183cd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="183cd-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="183cd-120">LastValidated</span></span>  <br/> |<span data-ttu-id="183cd-121">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="183cd-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="183cd-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="183cd-122">required</span></span>  <br/> ||<span data-ttu-id="183cd-123">Valeurs du type xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="183cd-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="183cd-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="183cd-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="183cd-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="183cd-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="183cd-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="183cd-126">required</span></span>  <br/> ||<span data-ttu-id="183cd-127">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="183cd-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

