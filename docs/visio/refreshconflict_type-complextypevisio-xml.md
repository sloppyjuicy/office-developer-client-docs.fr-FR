---
title: ComplexType RefreshConflict_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346479"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="aec3e-102">ComplexType RefreshConflict_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="aec3e-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="aec3e-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="aec3e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aec3e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aec3e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aec3e-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="aec3e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aec3e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="aec3e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aec3e-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="aec3e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aec3e-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="aec3e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aec3e-109">Définition</span><span class="sxs-lookup"><span data-stu-id="aec3e-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshConflict_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aec3e-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="aec3e-110">Elements and attributes</span></span>

<span data-ttu-id="aec3e-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="aec3e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aec3e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aec3e-112">Child elements</span></span>

<span data-ttu-id="aec3e-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="aec3e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aec3e-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="aec3e-114">Attributes</span></span>

|<span data-ttu-id="aec3e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aec3e-115">**Attribute**</span></span>|<span data-ttu-id="aec3e-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="aec3e-116">**Type**</span></span>|<span data-ttu-id="aec3e-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="aec3e-117">**Required**</span></span>|<span data-ttu-id="aec3e-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="aec3e-118">**Description**</span></span>|<span data-ttu-id="aec3e-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="aec3e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aec3e-120">PageID</span><span class="sxs-lookup"><span data-stu-id="aec3e-120">PageID</span></span>  <br/> |<span data-ttu-id="aec3e-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aec3e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aec3e-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="aec3e-122">required</span></span>  <br/> ||<span data-ttu-id="aec3e-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aec3e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aec3e-124">RowID</span><span class="sxs-lookup"><span data-stu-id="aec3e-124">RowID</span></span>  <br/> |<span data-ttu-id="aec3e-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aec3e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aec3e-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="aec3e-126">required</span></span>  <br/> ||<span data-ttu-id="aec3e-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aec3e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aec3e-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="aec3e-128">ShapeID</span></span>  <br/> |<span data-ttu-id="aec3e-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aec3e-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aec3e-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="aec3e-130">required</span></span>  <br/> ||<span data-ttu-id="aec3e-131">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aec3e-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

