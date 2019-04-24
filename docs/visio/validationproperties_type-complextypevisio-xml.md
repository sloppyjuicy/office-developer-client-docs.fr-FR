---
title: ComplexType ValidationProperties_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: 2fa6724ce6262886379f3ac22625927608184bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355978"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="0a6bf-102">ComplexType ValidationProperties_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0a6bf-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0a6bf-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="0a6bf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a6bf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0a6bf-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a6bf-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0a6bf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0a6bf-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a6bf-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="0a6bf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a6bf-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0a6bf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0a6bf-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0a6bf-110">Elements and attributes</span></span>

<span data-ttu-id="0a6bf-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="0a6bf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a6bf-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0a6bf-112">Child elements</span></span>

<span data-ttu-id="0a6bf-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0a6bf-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a6bf-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="0a6bf-114">Attributes</span></span>

|<span data-ttu-id="0a6bf-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-115">**Attribute**</span></span>|<span data-ttu-id="0a6bf-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-116">**Type**</span></span>|<span data-ttu-id="0a6bf-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-117">**Required**</span></span>|<span data-ttu-id="0a6bf-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-118">**Description**</span></span>|<span data-ttu-id="0a6bf-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0a6bf-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a6bf-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="0a6bf-120">LastValidated</span></span>  <br/> |<span data-ttu-id="0a6bf-121">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="0a6bf-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="0a6bf-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a6bf-122">required</span></span>  <br/> ||<span data-ttu-id="0a6bf-123">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="0a6bf-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="0a6bf-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="0a6bf-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="0a6bf-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="0a6bf-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0a6bf-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a6bf-126">required</span></span>  <br/> ||<span data-ttu-id="0a6bf-127">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0a6bf-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

