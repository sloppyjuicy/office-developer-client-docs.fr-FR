---
title: AuthorEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 41279e9f4ffa0bba17d4f74eb2f40d724589c17d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537877"
---
# <a name="authorentry_type-complextype-visio-xml"></a><span data-ttu-id="661e1-102">AuthorEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="661e1-102">AuthorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="661e1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="661e1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="661e1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="661e1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="661e1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="661e1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="661e1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="661e1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="661e1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="661e1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="661e1-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="661e1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="661e1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="661e1-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="661e1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="661e1-110">Elements and attributes</span></span>

<span data-ttu-id="661e1-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="661e1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="661e1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="661e1-112">Child elements</span></span>

<span data-ttu-id="661e1-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="661e1-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="661e1-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="661e1-114">Attributes</span></span>

|<span data-ttu-id="661e1-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="661e1-115">**Attribute**</span></span>|<span data-ttu-id="661e1-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="661e1-116">**Type**</span></span>|<span data-ttu-id="661e1-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="661e1-117">**Required**</span></span>|<span data-ttu-id="661e1-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="661e1-118">**Description**</span></span>|<span data-ttu-id="661e1-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="661e1-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="661e1-120">ID</span><span class="sxs-lookup"><span data-stu-id="661e1-120">ID</span></span>  <br/> |<span data-ttu-id="661e1-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="661e1-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="661e1-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="661e1-122">required</span></span>  <br/> ||<span data-ttu-id="661e1-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="661e1-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="661e1-124">Initials</span><span class="sxs-lookup"><span data-stu-id="661e1-124">Initials</span></span>  <br/> |<span data-ttu-id="661e1-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="661e1-125">xsd:string</span></span>  <br/> |<span data-ttu-id="661e1-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="661e1-126">optional</span></span>  <br/> ||<span data-ttu-id="661e1-127">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="661e1-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="661e1-128">Nom</span><span class="sxs-lookup"><span data-stu-id="661e1-128">Name</span></span>  <br/> |<span data-ttu-id="661e1-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="661e1-129">xsd:string</span></span>  <br/> |<span data-ttu-id="661e1-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="661e1-130">optional</span></span>  <br/> ||<span data-ttu-id="661e1-131">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="661e1-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="661e1-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="661e1-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="661e1-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="661e1-133">xsd:string</span></span>  <br/> |<span data-ttu-id="661e1-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="661e1-134">optional</span></span>  <br/> ||<span data-ttu-id="661e1-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="661e1-135">Values of the xsd:string type.</span></span>  <br/> |
   

