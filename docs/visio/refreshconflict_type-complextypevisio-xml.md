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
# <a name="refreshconflict_type-complextype-visio-xml"></a><span data-ttu-id="01b4a-102">RefreshConflict_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="01b4a-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="01b4a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="01b4a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01b4a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="01b4a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="01b4a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="01b4a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="01b4a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="01b4a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="01b4a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="01b4a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="01b4a-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="01b4a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="01b4a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="01b4a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="01b4a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="01b4a-110">Elements and attributes</span></span>

<span data-ttu-id="01b4a-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="01b4a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="01b4a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="01b4a-112">Child elements</span></span>

<span data-ttu-id="01b4a-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="01b4a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01b4a-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="01b4a-114">Attributes</span></span>

|<span data-ttu-id="01b4a-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="01b4a-115">**Attribute**</span></span>|<span data-ttu-id="01b4a-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="01b4a-116">**Type**</span></span>|<span data-ttu-id="01b4a-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="01b4a-117">**Required**</span></span>|<span data-ttu-id="01b4a-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="01b4a-118">**Description**</span></span>|<span data-ttu-id="01b4a-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="01b4a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="01b4a-120">PageID</span><span class="sxs-lookup"><span data-stu-id="01b4a-120">PageID</span></span>  <br/> |<span data-ttu-id="01b4a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="01b4a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01b4a-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="01b4a-122">required</span></span>  <br/> ||<span data-ttu-id="01b4a-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="01b4a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01b4a-124">RowID</span><span class="sxs-lookup"><span data-stu-id="01b4a-124">RowID</span></span>  <br/> |<span data-ttu-id="01b4a-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="01b4a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01b4a-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="01b4a-126">required</span></span>  <br/> ||<span data-ttu-id="01b4a-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="01b4a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01b4a-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="01b4a-128">ShapeID</span></span>  <br/> |<span data-ttu-id="01b4a-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="01b4a-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01b4a-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="01b4a-130">required</span></span>  <br/> ||<span data-ttu-id="01b4a-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="01b4a-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

