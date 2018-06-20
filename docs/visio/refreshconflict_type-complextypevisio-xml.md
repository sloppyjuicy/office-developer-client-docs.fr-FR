---
title: Type complexe RefreshConflict_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 44910cd305b484771ca3d4f4d49ef8a09a6fc2dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789424"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="9c550-102">Type complexe RefreshConflict_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9c550-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9c550-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9c550-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c550-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9c550-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9c550-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9c550-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9c550-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9c550-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9c550-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9c550-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9c550-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="9c550-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c550-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9c550-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9c550-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9c550-110">Elements and attributes</span></span>

<span data-ttu-id="9c550-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9c550-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9c550-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9c550-112">Child elements</span></span>

<span data-ttu-id="9c550-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9c550-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c550-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="9c550-114">Attributes</span></span>

|<span data-ttu-id="9c550-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9c550-115">**Attribute**</span></span>|<span data-ttu-id="9c550-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="9c550-116">**Type**</span></span>|<span data-ttu-id="9c550-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9c550-117">**Required**</span></span>|<span data-ttu-id="9c550-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c550-118">**Description**</span></span>|<span data-ttu-id="9c550-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9c550-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9c550-120">PageID</span><span class="sxs-lookup"><span data-stu-id="9c550-120">PageID</span></span>  <br/> |<span data-ttu-id="9c550-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c550-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c550-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9c550-122">required</span></span>  <br/> ||<span data-ttu-id="9c550-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c550-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c550-124">RowID</span><span class="sxs-lookup"><span data-stu-id="9c550-124">RowID</span></span>  <br/> |<span data-ttu-id="9c550-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c550-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c550-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9c550-126">required</span></span>  <br/> ||<span data-ttu-id="9c550-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c550-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c550-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="9c550-128">ShapeID</span></span>  <br/> |<span data-ttu-id="9c550-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c550-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c550-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9c550-130">required</span></span>  <br/> ||<span data-ttu-id="9c550-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c550-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

