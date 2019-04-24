---
title: Connect, élément (Connects_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346507"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="08de2-103">Connect, élément (Connects_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="08de2-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="08de2-104">Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.</span><span class="sxs-lookup"><span data-stu-id="08de2-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08de2-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="08de2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08de2-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="08de2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="08de2-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="08de2-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="08de2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08de2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="08de2-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="08de2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="08de2-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="08de2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="08de2-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="08de2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="08de2-112">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="08de2-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08de2-113">Définition</span><span class="sxs-lookup"><span data-stu-id="08de2-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="08de2-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="08de2-114">Elements and attributes</span></span>

<span data-ttu-id="08de2-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="08de2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="08de2-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="08de2-116">Parent elements</span></span>

|<span data-ttu-id="08de2-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="08de2-117">**Element**</span></span>|<span data-ttu-id="08de2-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="08de2-118">**Type**</span></span>|<span data-ttu-id="08de2-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="08de2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08de2-120">Connects</span><span class="sxs-lookup"><span data-stu-id="08de2-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="08de2-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="08de2-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="08de2-122">Contient un élément **Connect** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="08de2-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="08de2-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="08de2-123">Child elements</span></span>

<span data-ttu-id="08de2-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="08de2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08de2-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="08de2-125">Attributes</span></span>

|<span data-ttu-id="08de2-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="08de2-126">**Attribute**</span></span>|<span data-ttu-id="08de2-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="08de2-127">**Type**</span></span>|<span data-ttu-id="08de2-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="08de2-128">**Required**</span></span>|<span data-ttu-id="08de2-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="08de2-129">**Description**</span></span>|<span data-ttu-id="08de2-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="08de2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="08de2-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="08de2-131">FromCell</span></span>  <br/> |<span data-ttu-id="08de2-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="08de2-132">xsd:string</span></span>  <br/> |<span data-ttu-id="08de2-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="08de2-133">optional</span></span>  <br/> |<span data-ttu-id="08de2-134">Cellule à l'origine de la connexion.</span><span class="sxs-lookup"><span data-stu-id="08de2-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="08de2-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="08de2-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="08de2-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="08de2-136">FromPart</span></span>  <br/> |<span data-ttu-id="08de2-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="08de2-137">xsd:int</span></span>  <br/> |<span data-ttu-id="08de2-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="08de2-138">optional</span></span>  <br/> |<span data-ttu-id="08de2-139">Partie d'une forme à l'origine d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="08de2-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="08de2-140">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="08de2-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="08de2-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="08de2-141">FromSheet</span></span>  <br/> |<span data-ttu-id="08de2-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="08de2-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="08de2-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="08de2-143">required</span></span>  <br/> |<span data-ttu-id="08de2-144">ID de la forme à partir de laquelle une ou des connexions sont à l'origine de la connexion.</span><span class="sxs-lookup"><span data-stu-id="08de2-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="08de2-145">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="08de2-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="08de2-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="08de2-146">ToCell</span></span>  <br/> |<span data-ttu-id="08de2-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="08de2-147">xsd:string</span></span>  <br/> |<span data-ttu-id="08de2-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="08de2-148">optional</span></span>  <br/> |<span data-ttu-id="08de2-149">Cellule vers laquelle une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="08de2-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="08de2-150">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="08de2-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="08de2-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="08de2-151">ToPart</span></span>  <br/> |<span data-ttu-id="08de2-152">xsd: int</span><span class="sxs-lookup"><span data-stu-id="08de2-152">xsd:int</span></span>  <br/> |<span data-ttu-id="08de2-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="08de2-153">optional</span></span>  <br/> |<span data-ttu-id="08de2-154">Partie d'une forme à laquelle une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="08de2-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="08de2-155">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="08de2-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="08de2-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="08de2-156">ToSheet</span></span>  <br/> |<span data-ttu-id="08de2-157">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="08de2-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="08de2-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="08de2-158">required</span></span>  <br/> |<span data-ttu-id="08de2-159">ID de la forme à laquelle une ou plusieurs connexions sont établies.</span><span class="sxs-lookup"><span data-stu-id="08de2-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="08de2-160">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="08de2-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

