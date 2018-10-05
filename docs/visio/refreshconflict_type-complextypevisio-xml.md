---
title: Type complexe RefreshConflict_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383169"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="40531-102">Type complexe RefreshConflict_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="40531-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="40531-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="40531-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40531-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="40531-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="40531-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="40531-105">**Schema file**</span></span> <br/> |<span data-ttu-id="40531-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="40531-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="40531-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="40531-107">**Extension base**</span></span> <br/> |<span data-ttu-id="40531-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="40531-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40531-109">Définition</span><span class="sxs-lookup"><span data-stu-id="40531-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="40531-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="40531-110">Elements and attributes</span></span>

<span data-ttu-id="40531-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="40531-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="40531-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="40531-112">Child elements</span></span>

<span data-ttu-id="40531-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="40531-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40531-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="40531-114">Attributes</span></span>

|<span data-ttu-id="40531-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="40531-115">**Attribute**</span></span>|<span data-ttu-id="40531-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="40531-116">**Type**</span></span>|<span data-ttu-id="40531-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="40531-117">**Required**</span></span>|<span data-ttu-id="40531-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="40531-118">**Description**</span></span>|<span data-ttu-id="40531-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="40531-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="40531-120">PageID</span><span class="sxs-lookup"><span data-stu-id="40531-120">PageID</span></span>  <br/> |<span data-ttu-id="40531-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40531-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40531-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40531-122">required</span></span>  <br/> ||<span data-ttu-id="40531-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="40531-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="40531-124">RowID</span><span class="sxs-lookup"><span data-stu-id="40531-124">RowID</span></span>  <br/> |<span data-ttu-id="40531-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40531-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40531-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40531-126">required</span></span>  <br/> ||<span data-ttu-id="40531-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="40531-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="40531-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="40531-128">ShapeID</span></span>  <br/> |<span data-ttu-id="40531-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40531-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40531-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40531-130">required</span></span>  <br/> ||<span data-ttu-id="40531-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="40531-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

