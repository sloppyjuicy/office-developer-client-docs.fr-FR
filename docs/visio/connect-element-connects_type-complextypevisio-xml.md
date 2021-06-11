---
title: Connecter’élément (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541994"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a><span data-ttu-id="4b913-103">Connecter’élément (Connects_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4b913-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4b913-104">Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.</span><span class="sxs-lookup"><span data-stu-id="4b913-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b913-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="4b913-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b913-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4b913-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4b913-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="4b913-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4b913-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4b913-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4b913-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4b913-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4b913-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4b913-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4b913-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="4b913-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4b913-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="4b913-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b913-113">Définition</span><span class="sxs-lookup"><span data-stu-id="4b913-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4b913-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4b913-114">Elements and attributes</span></span>

<span data-ttu-id="4b913-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="4b913-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4b913-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4b913-116">Parent elements</span></span>

|<span data-ttu-id="4b913-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4b913-117">**Element**</span></span>|<span data-ttu-id="4b913-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4b913-118">**Type**</span></span>|<span data-ttu-id="4b913-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b913-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b913-120">Connects</span><span class="sxs-lookup"><span data-stu-id="4b913-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b913-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="4b913-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b913-122">Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="4b913-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4b913-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4b913-123">Child elements</span></span>

<span data-ttu-id="4b913-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4b913-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b913-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="4b913-125">Attributes</span></span>

|<span data-ttu-id="4b913-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4b913-126">**Attribute**</span></span>|<span data-ttu-id="4b913-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="4b913-127">**Type**</span></span>|<span data-ttu-id="4b913-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4b913-128">**Required**</span></span>|<span data-ttu-id="4b913-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b913-129">**Description**</span></span>|<span data-ttu-id="4b913-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4b913-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b913-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="4b913-131">FromCell</span></span>  <br/> |<span data-ttu-id="4b913-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4b913-132">xsd:string</span></span>  <br/> |<span data-ttu-id="4b913-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b913-133">optional</span></span>  <br/> |<span data-ttu-id="4b913-134">Cellule d’où provient une connexion.</span><span class="sxs-lookup"><span data-stu-id="4b913-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="4b913-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4b913-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b913-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="4b913-136">FromPart</span></span>  <br/> |<span data-ttu-id="4b913-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="4b913-137">xsd:int</span></span>  <br/> |<span data-ttu-id="4b913-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b913-138">optional</span></span>  <br/> |<span data-ttu-id="4b913-139">Partie d’une forme d’où provient une connexion.</span><span class="sxs-lookup"><span data-stu-id="4b913-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="4b913-140">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="4b913-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="4b913-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="4b913-141">FromSheet</span></span>  <br/> |<span data-ttu-id="4b913-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b913-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b913-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4b913-143">required</span></span>  <br/> |<span data-ttu-id="4b913-144">ID de la forme d’où provient une ou plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="4b913-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="4b913-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b913-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b913-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="4b913-146">ToCell</span></span>  <br/> |<span data-ttu-id="4b913-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4b913-147">xsd:string</span></span>  <br/> |<span data-ttu-id="4b913-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b913-148">optional</span></span>  <br/> |<span data-ttu-id="4b913-149">Cellule à laquelle une connexion est réalisée.</span><span class="sxs-lookup"><span data-stu-id="4b913-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="4b913-150">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4b913-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b913-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="4b913-151">ToPart</span></span>  <br/> |<span data-ttu-id="4b913-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="4b913-152">xsd:int</span></span>  <br/> |<span data-ttu-id="4b913-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="4b913-153">optional</span></span>  <br/> |<span data-ttu-id="4b913-154">Partie d’une forme à laquelle une connexion est établir.</span><span class="sxs-lookup"><span data-stu-id="4b913-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="4b913-155">Valeurs du type xsd:Int.</span><span class="sxs-lookup"><span data-stu-id="4b913-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="4b913-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="4b913-156">ToSheet</span></span>  <br/> |<span data-ttu-id="4b913-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b913-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b913-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4b913-158">required</span></span>  <br/> |<span data-ttu-id="4b913-159">ID de la forme à laquelle une ou plusieurs connexions sont réalisées.</span><span class="sxs-lookup"><span data-stu-id="4b913-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="4b913-160">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b913-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

