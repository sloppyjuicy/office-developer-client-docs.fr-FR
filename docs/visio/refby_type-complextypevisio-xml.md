---
title: ComplexType RefBy_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348320"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="80a1e-102">ComplexType RefBy_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="80a1e-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="80a1e-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="80a1e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80a1e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="80a1e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="80a1e-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="80a1e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="80a1e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="80a1e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="80a1e-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="80a1e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="80a1e-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="80a1e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80a1e-109">Définition</span><span class="sxs-lookup"><span data-stu-id="80a1e-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="80a1e-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="80a1e-110">Elements and attributes</span></span>

<span data-ttu-id="80a1e-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="80a1e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="80a1e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="80a1e-112">Child elements</span></span>

<span data-ttu-id="80a1e-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="80a1e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80a1e-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="80a1e-114">Attributes</span></span>

|<span data-ttu-id="80a1e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="80a1e-115">**Attribute**</span></span>|<span data-ttu-id="80a1e-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="80a1e-116">**Type**</span></span>|<span data-ttu-id="80a1e-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="80a1e-117">**Required**</span></span>|<span data-ttu-id="80a1e-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="80a1e-118">**Description**</span></span>|<span data-ttu-id="80a1e-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="80a1e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80a1e-120">ID</span><span class="sxs-lookup"><span data-stu-id="80a1e-120">ID</span></span>  <br/> |<span data-ttu-id="80a1e-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="80a1e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="80a1e-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="80a1e-122">required</span></span>  <br/> ||<span data-ttu-id="80a1e-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="80a1e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="80a1e-124">T</span><span class="sxs-lookup"><span data-stu-id="80a1e-124">T</span></span>  <br/> |<span data-ttu-id="80a1e-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="80a1e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="80a1e-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="80a1e-126">required</span></span>  <br/> ||<span data-ttu-id="80a1e-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="80a1e-127">Values of the xsd:string type.</span></span>  <br/> |
   

