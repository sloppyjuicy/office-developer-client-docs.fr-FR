---
title: DataConnection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539648"
---
# <a name="dataconnection_type-complextype-visio-xml"></a><span data-ttu-id="9e8da-102">DataConnection_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9e8da-102">DataConnection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9e8da-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9e8da-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e8da-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9e8da-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9e8da-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9e8da-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9e8da-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9e8da-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9e8da-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9e8da-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9e8da-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="9e8da-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9e8da-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9e8da-109">Definition</span></span>

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9e8da-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9e8da-110">Elements and attributes</span></span>

<span data-ttu-id="9e8da-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="9e8da-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9e8da-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9e8da-112">Child elements</span></span>

<span data-ttu-id="9e8da-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9e8da-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e8da-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="9e8da-114">Attributes</span></span>

|<span data-ttu-id="9e8da-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9e8da-115">**Attribute**</span></span>|<span data-ttu-id="9e8da-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="9e8da-116">**Type**</span></span>|<span data-ttu-id="9e8da-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9e8da-117">**Required**</span></span>|<span data-ttu-id="9e8da-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="9e8da-118">**Description**</span></span>|<span data-ttu-id="9e8da-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9e8da-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9e8da-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="9e8da-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="9e8da-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9e8da-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9e8da-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="9e8da-122">optional</span></span>  <br/> ||<span data-ttu-id="9e8da-123">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9e8da-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9e8da-124">Commande</span><span class="sxs-lookup"><span data-stu-id="9e8da-124">Command</span></span>  <br/> |<span data-ttu-id="9e8da-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9e8da-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9e8da-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="9e8da-126">optional</span></span>  <br/> ||<span data-ttu-id="9e8da-127">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9e8da-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9e8da-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9e8da-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="9e8da-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9e8da-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9e8da-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="9e8da-130">optional</span></span>  <br/> ||<span data-ttu-id="9e8da-131">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9e8da-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9e8da-132">FileName</span><span class="sxs-lookup"><span data-stu-id="9e8da-132">FileName</span></span>  <br/> |<span data-ttu-id="9e8da-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9e8da-133">xsd:string</span></span>  <br/> |<span data-ttu-id="9e8da-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9e8da-134">required</span></span>  <br/> ||<span data-ttu-id="9e8da-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9e8da-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9e8da-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9e8da-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="9e8da-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9e8da-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9e8da-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="9e8da-138">optional</span></span>  <br/> ||<span data-ttu-id="9e8da-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9e8da-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9e8da-140">ID</span><span class="sxs-lookup"><span data-stu-id="9e8da-140">ID</span></span>  <br/> |<span data-ttu-id="9e8da-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9e8da-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9e8da-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9e8da-142">required</span></span>  <br/> ||<span data-ttu-id="9e8da-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9e8da-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9e8da-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="9e8da-144">Timeout</span></span>  <br/> |<span data-ttu-id="9e8da-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9e8da-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9e8da-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="9e8da-146">optional</span></span>  <br/> ||<span data-ttu-id="9e8da-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9e8da-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

