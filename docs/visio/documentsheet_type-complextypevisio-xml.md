---
title: DocumentSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 18e7f064b1b6c9ac8e084c96011c1b18a646aecb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540006"
---
# <a name="documentsheet_type-complextype-visio-xml"></a><span data-ttu-id="11245-102">DocumentSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="11245-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="11245-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="11245-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11245-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11245-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="11245-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="11245-105">**Schema file**</span></span> <br/> |<span data-ttu-id="11245-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="11245-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="11245-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="11245-107">**Extension base**</span></span> <br/> |<span data-ttu-id="11245-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="11245-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11245-109">Définition</span><span class="sxs-lookup"><span data-stu-id="11245-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11245-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="11245-110">Elements and attributes</span></span>

<span data-ttu-id="11245-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="11245-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="11245-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="11245-112">Child elements</span></span>

<span data-ttu-id="11245-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="11245-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11245-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="11245-114">Attributes</span></span>

|<span data-ttu-id="11245-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="11245-115">**Attribute**</span></span>|<span data-ttu-id="11245-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="11245-116">**Type**</span></span>|<span data-ttu-id="11245-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="11245-117">**Required**</span></span>|<span data-ttu-id="11245-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="11245-118">**Description**</span></span>|<span data-ttu-id="11245-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="11245-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="11245-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="11245-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="11245-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="11245-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="11245-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="11245-122">optional</span></span>  <br/> ||<span data-ttu-id="11245-123">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="11245-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="11245-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="11245-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="11245-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="11245-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="11245-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="11245-126">optional</span></span>  <br/> ||<span data-ttu-id="11245-127">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="11245-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="11245-128">Nom</span><span class="sxs-lookup"><span data-stu-id="11245-128">Name</span></span>  <br/> |<span data-ttu-id="11245-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="11245-129">xsd:string</span></span>  <br/> |<span data-ttu-id="11245-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="11245-130">optional</span></span>  <br/> ||<span data-ttu-id="11245-131">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="11245-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="11245-132">NameU</span><span class="sxs-lookup"><span data-stu-id="11245-132">NameU</span></span>  <br/> |<span data-ttu-id="11245-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="11245-133">xsd:string</span></span>  <br/> |<span data-ttu-id="11245-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="11245-134">optional</span></span>  <br/> ||<span data-ttu-id="11245-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="11245-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="11245-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="11245-136">UniqueID</span></span>  <br/> |<span data-ttu-id="11245-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="11245-137">xsd:string</span></span>  <br/> |<span data-ttu-id="11245-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="11245-138">optional</span></span>  <br/> ||<span data-ttu-id="11245-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="11245-139">Values of the xsd:string type.</span></span>  <br/> |
   

