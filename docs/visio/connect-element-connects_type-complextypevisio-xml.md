---
title: Se connecter, élément (Connects_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.\n"
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399318"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="c1879-103">Se connecter, élément (Connects_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c1879-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c1879-104">
			Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
</span><span class="sxs-lookup"><span data-stu-id="c1879-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1879-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="c1879-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1879-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c1879-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1879-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="c1879-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1879-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c1879-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1879-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c1879-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1879-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c1879-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1879-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="c1879-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1879-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="c1879-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1879-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c1879-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1879-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c1879-114">Elements and attributes</span></span>

<span data-ttu-id="c1879-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c1879-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1879-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c1879-116">Parent elements</span></span>

|<span data-ttu-id="c1879-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c1879-117">**Element**</span></span>|<span data-ttu-id="c1879-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="c1879-118">**Type**</span></span>|<span data-ttu-id="c1879-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c1879-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1879-120">Connects</span><span class="sxs-lookup"><span data-stu-id="c1879-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1879-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="c1879-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1879-122">Contient un élément de **connexion** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="c1879-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1879-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1879-123">Child elements</span></span>

<span data-ttu-id="c1879-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c1879-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1879-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="c1879-125">Attributes</span></span>

|<span data-ttu-id="c1879-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c1879-126">**Attribute**</span></span>|<span data-ttu-id="c1879-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="c1879-127">**Type**</span></span>|<span data-ttu-id="c1879-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c1879-128">**Required**</span></span>|<span data-ttu-id="c1879-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="c1879-129">**Description**</span></span>|<span data-ttu-id="c1879-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c1879-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c1879-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="c1879-131">FromCell</span></span>  <br/> |<span data-ttu-id="c1879-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c1879-132">xsd:string</span></span>  <br/> |<span data-ttu-id="c1879-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="c1879-133">optional</span></span>  <br/> |<span data-ttu-id="c1879-134">La cellule à l’origine une connexion.</span><span class="sxs-lookup"><span data-stu-id="c1879-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="c1879-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c1879-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1879-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="c1879-136">FromPart</span></span>  <br/> |<span data-ttu-id="c1879-137">XSD : int</span><span class="sxs-lookup"><span data-stu-id="c1879-137">xsd:int</span></span>  <br/> |<span data-ttu-id="c1879-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="c1879-138">optional</span></span>  <br/> |<span data-ttu-id="c1879-139">La partie de la forme à partir de laquelle une connexion.</span><span class="sxs-lookup"><span data-stu-id="c1879-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="c1879-140">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="c1879-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="c1879-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="c1879-141">FromSheet</span></span>  <br/> |<span data-ttu-id="c1879-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c1879-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c1879-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c1879-143">required</span></span>  <br/> |<span data-ttu-id="c1879-144">L’ID de la forme à partir de laquelle une connexion ou proviennent.</span><span class="sxs-lookup"><span data-stu-id="c1879-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="c1879-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c1879-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c1879-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="c1879-146">ToCell</span></span>  <br/> |<span data-ttu-id="c1879-147">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c1879-147">xsd:string</span></span>  <br/> |<span data-ttu-id="c1879-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="c1879-148">optional</span></span>  <br/> |<span data-ttu-id="c1879-149">La cellule avec laquelle une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="c1879-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="c1879-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c1879-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1879-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="c1879-151">ToPart</span></span>  <br/> |<span data-ttu-id="c1879-152">XSD : int</span><span class="sxs-lookup"><span data-stu-id="c1879-152">xsd:int</span></span>  <br/> |<span data-ttu-id="c1879-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="c1879-153">optional</span></span>  <br/> |<span data-ttu-id="c1879-154">La partie de la forme avec laquelle une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="c1879-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="c1879-155">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="c1879-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="c1879-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="c1879-156">ToSheet</span></span>  <br/> |<span data-ttu-id="c1879-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c1879-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c1879-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c1879-158">required</span></span>  <br/> |<span data-ttu-id="c1879-159">L’ID de la forme à laquelle une ou plusieurs connexions sont effectuées.</span><span class="sxs-lookup"><span data-stu-id="c1879-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="c1879-160">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c1879-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

