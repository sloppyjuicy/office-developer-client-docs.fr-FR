---
title: ComplexType DataConnection_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344603"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="e66ec-102">ComplexType DataConnection_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e66ec-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e66ec-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e66ec-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e66ec-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e66ec-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e66ec-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e66ec-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e66ec-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e66ec-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e66ec-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e66ec-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e66ec-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="e66ec-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e66ec-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e66ec-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e66ec-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e66ec-110">Elements and attributes</span></span>

<span data-ttu-id="e66ec-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="e66ec-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e66ec-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e66ec-112">Child elements</span></span>

<span data-ttu-id="e66ec-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e66ec-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e66ec-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="e66ec-114">Attributes</span></span>

|<span data-ttu-id="e66ec-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e66ec-115">**Attribute**</span></span>|<span data-ttu-id="e66ec-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="e66ec-116">**Type**</span></span>|<span data-ttu-id="e66ec-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e66ec-117">**Required**</span></span>|<span data-ttu-id="e66ec-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="e66ec-118">**Description**</span></span>|<span data-ttu-id="e66ec-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e66ec-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e66ec-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="e66ec-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="e66ec-121">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="e66ec-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e66ec-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="e66ec-122">optional</span></span>  <br/> ||<span data-ttu-id="e66ec-123">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e66ec-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e66ec-124">Command</span><span class="sxs-lookup"><span data-stu-id="e66ec-124">Command</span></span>  <br/> |<span data-ttu-id="e66ec-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e66ec-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e66ec-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="e66ec-126">optional</span></span>  <br/> ||<span data-ttu-id="e66ec-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e66ec-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e66ec-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e66ec-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="e66ec-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e66ec-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e66ec-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="e66ec-130">optional</span></span>  <br/> ||<span data-ttu-id="e66ec-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e66ec-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e66ec-132">FileName</span><span class="sxs-lookup"><span data-stu-id="e66ec-132">FileName</span></span>  <br/> |<span data-ttu-id="e66ec-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e66ec-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e66ec-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e66ec-134">required</span></span>  <br/> ||<span data-ttu-id="e66ec-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e66ec-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e66ec-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e66ec-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="e66ec-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e66ec-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e66ec-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="e66ec-138">optional</span></span>  <br/> ||<span data-ttu-id="e66ec-139">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e66ec-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e66ec-140">ID</span><span class="sxs-lookup"><span data-stu-id="e66ec-140">ID</span></span>  <br/> |<span data-ttu-id="e66ec-141">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e66ec-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e66ec-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e66ec-142">required</span></span>  <br/> ||<span data-ttu-id="e66ec-143">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e66ec-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e66ec-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="e66ec-144">Timeout</span></span>  <br/> |<span data-ttu-id="e66ec-145">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e66ec-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e66ec-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="e66ec-146">optional</span></span>  <br/> ||<span data-ttu-id="e66ec-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e66ec-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

