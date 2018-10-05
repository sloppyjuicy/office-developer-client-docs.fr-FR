---
title: Type complexe DataConnection_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389140"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="a3a2f-102">Type complexe DataConnection_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a3a2f-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a3a2f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a3a2f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3a2f-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a3a2f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a3a2f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a3a2f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a3a2f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a3a2f-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="a3a2f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3a2f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a3a2f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a3a2f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a3a2f-110">Elements and attributes</span></span>

<span data-ttu-id="a3a2f-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a3a2f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a3a2f-112">Child elements</span></span>

<span data-ttu-id="a3a2f-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3a2f-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="a3a2f-114">Attributes</span></span>

|<span data-ttu-id="a3a2f-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-115">**Attribute**</span></span>|<span data-ttu-id="a3a2f-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-116">**Type**</span></span>|<span data-ttu-id="a3a2f-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-117">**Required**</span></span>|<span data-ttu-id="a3a2f-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-118">**Description**</span></span>|<span data-ttu-id="a3a2f-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a3a2f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3a2f-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="a3a2f-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="a3a2f-121">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="a3a2f-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a3a2f-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="a3a2f-122">optional</span></span>  <br/> ||<span data-ttu-id="a3a2f-123">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a3a2f-124">Commande</span><span class="sxs-lookup"><span data-stu-id="a3a2f-124">Command</span></span>  <br/> |<span data-ttu-id="a3a2f-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a3a2f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="a3a2f-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="a3a2f-126">optional</span></span>  <br/> ||<span data-ttu-id="a3a2f-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3a2f-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a3a2f-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="a3a2f-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a3a2f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="a3a2f-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="a3a2f-130">optional</span></span>  <br/> ||<span data-ttu-id="a3a2f-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3a2f-132">FileName</span><span class="sxs-lookup"><span data-stu-id="a3a2f-132">FileName</span></span>  <br/> |<span data-ttu-id="a3a2f-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a3a2f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a3a2f-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3a2f-134">required</span></span>  <br/> ||<span data-ttu-id="a3a2f-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3a2f-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a3a2f-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="a3a2f-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a3a2f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a3a2f-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="a3a2f-138">optional</span></span>  <br/> ||<span data-ttu-id="a3a2f-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3a2f-140">ID</span><span class="sxs-lookup"><span data-stu-id="a3a2f-140">ID</span></span>  <br/> |<span data-ttu-id="a3a2f-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3a2f-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3a2f-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3a2f-142">required</span></span>  <br/> ||<span data-ttu-id="a3a2f-143">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a3a2f-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="a3a2f-144">Timeout</span></span>  <br/> |<span data-ttu-id="a3a2f-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3a2f-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3a2f-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="a3a2f-146">optional</span></span>  <br/> ||<span data-ttu-id="a3a2f-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

