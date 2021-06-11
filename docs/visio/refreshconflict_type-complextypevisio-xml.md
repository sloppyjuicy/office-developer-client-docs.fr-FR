---
title: RefreshConflict_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 7b52bc87af213e9c26f4bc359adf6cf900b34957
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542827"
---
# <a name="refreshconflict_type-complextype-visio-xml"></a><span data-ttu-id="dcb48-102">RefreshConflict_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dcb48-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dcb48-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="dcb48-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcb48-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dcb48-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dcb48-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="dcb48-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dcb48-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dcb48-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dcb48-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="dcb48-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dcb48-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="dcb48-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dcb48-109">Définition</span><span class="sxs-lookup"><span data-stu-id="dcb48-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dcb48-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="dcb48-110">Elements and attributes</span></span>

<span data-ttu-id="dcb48-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="dcb48-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dcb48-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dcb48-112">Child elements</span></span>

<span data-ttu-id="dcb48-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dcb48-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcb48-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="dcb48-114">Attributes</span></span>

|<span data-ttu-id="dcb48-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dcb48-115">**Attribute**</span></span>|<span data-ttu-id="dcb48-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="dcb48-116">**Type**</span></span>|<span data-ttu-id="dcb48-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="dcb48-117">**Required**</span></span>|<span data-ttu-id="dcb48-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="dcb48-118">**Description**</span></span>|<span data-ttu-id="dcb48-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="dcb48-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dcb48-120">PageID</span><span class="sxs-lookup"><span data-stu-id="dcb48-120">PageID</span></span>  <br/> |<span data-ttu-id="dcb48-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dcb48-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dcb48-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dcb48-122">required</span></span>  <br/> ||<span data-ttu-id="dcb48-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dcb48-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dcb48-124">RowID</span><span class="sxs-lookup"><span data-stu-id="dcb48-124">RowID</span></span>  <br/> |<span data-ttu-id="dcb48-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dcb48-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dcb48-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dcb48-126">required</span></span>  <br/> ||<span data-ttu-id="dcb48-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dcb48-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dcb48-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="dcb48-128">ShapeID</span></span>  <br/> |<span data-ttu-id="dcb48-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dcb48-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dcb48-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dcb48-130">required</span></span>  <br/> ||<span data-ttu-id="dcb48-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dcb48-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

