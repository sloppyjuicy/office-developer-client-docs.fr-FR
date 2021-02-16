---
title: RefBy_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 7970ae735f4933f05e71f1758912d3ecd382bf89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538276"
---
# <a name="refby_type-complextype-visio-xml"></a><span data-ttu-id="d8829-102">RefBy_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d8829-102">RefBy_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d8829-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="d8829-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8829-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8829-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8829-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d8829-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8829-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8829-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8829-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="d8829-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8829-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="d8829-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8829-109">Définition</span><span class="sxs-lookup"><span data-stu-id="d8829-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d8829-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d8829-110">Elements and attributes</span></span>

<span data-ttu-id="d8829-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="d8829-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8829-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d8829-112">Child elements</span></span>

<span data-ttu-id="d8829-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d8829-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8829-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="d8829-114">Attributes</span></span>

|<span data-ttu-id="d8829-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d8829-115">**Attribute**</span></span>|<span data-ttu-id="d8829-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="d8829-116">**Type**</span></span>|<span data-ttu-id="d8829-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d8829-117">**Required**</span></span>|<span data-ttu-id="d8829-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="d8829-118">**Description**</span></span>|<span data-ttu-id="d8829-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d8829-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8829-120">ID</span><span class="sxs-lookup"><span data-stu-id="d8829-120">ID</span></span>  <br/> |<span data-ttu-id="d8829-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8829-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8829-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d8829-122">required</span></span>  <br/> ||<span data-ttu-id="d8829-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8829-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8829-124">T</span><span class="sxs-lookup"><span data-stu-id="d8829-124">T</span></span>  <br/> |<span data-ttu-id="d8829-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8829-125">xsd:string</span></span>  <br/> |<span data-ttu-id="d8829-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d8829-126">required</span></span>  <br/> ||<span data-ttu-id="d8829-127">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d8829-127">Values of the xsd:string type.</span></span>  <br/> |
   

