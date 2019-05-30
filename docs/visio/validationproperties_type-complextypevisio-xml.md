---
title: ComplexType ValidationProperties_Type (Visio XML)
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
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="ab37e-102">ComplexType ValidationProperties_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ab37e-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ab37e-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ab37e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab37e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ab37e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ab37e-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ab37e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ab37e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ab37e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ab37e-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ab37e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ab37e-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="ab37e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab37e-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ab37e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ab37e-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ab37e-110">Elements and attributes</span></span>

<span data-ttu-id="ab37e-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ab37e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ab37e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ab37e-112">Child elements</span></span>

<span data-ttu-id="ab37e-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ab37e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab37e-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="ab37e-114">Attributes</span></span>

|<span data-ttu-id="ab37e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ab37e-115">**Attribute**</span></span>|<span data-ttu-id="ab37e-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="ab37e-116">**Type**</span></span>|<span data-ttu-id="ab37e-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ab37e-117">**Required**</span></span>|<span data-ttu-id="ab37e-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab37e-118">**Description**</span></span>|<span data-ttu-id="ab37e-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ab37e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab37e-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="ab37e-120">LastValidated</span></span>  <br/> |<span data-ttu-id="ab37e-121">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="ab37e-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="ab37e-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ab37e-122">required</span></span>  <br/> ||<span data-ttu-id="ab37e-123">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="ab37e-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="ab37e-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="ab37e-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="ab37e-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="ab37e-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ab37e-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ab37e-126">required</span></span>  <br/> ||<span data-ttu-id="ab37e-127">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ab37e-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

