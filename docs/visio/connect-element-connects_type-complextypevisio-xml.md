---
title: Se connecter, élément (Connects_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788336"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="ed2f4-103">Se connecter, élément (Connects_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ed2f4-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ed2f4-104">Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed2f4-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="ed2f4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed2f4-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ed2f4-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="ed2f4-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ed2f4-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ed2f4-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ed2f4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ed2f4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ed2f4-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ed2f4-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="ed2f4-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ed2f4-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ed2f4-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ed2f4-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ed2f4-114">Elements and attributes</span></span>

<span data-ttu-id="ed2f4-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ed2f4-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ed2f4-116">Parent elements</span></span>

|<span data-ttu-id="ed2f4-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-117">**Element**</span></span>|<span data-ttu-id="ed2f4-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-118">**Type**</span></span>|<span data-ttu-id="ed2f4-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ed2f4-120">Se connecte</span><span class="sxs-lookup"><span data-stu-id="ed2f4-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ed2f4-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="ed2f4-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ed2f4-122">Contient un élément de **connexion** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ed2f4-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ed2f4-123">Child elements</span></span>

<span data-ttu-id="ed2f4-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed2f4-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="ed2f4-125">Attributes</span></span>

|<span data-ttu-id="ed2f4-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-126">**Attribute**</span></span>|<span data-ttu-id="ed2f4-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-127">**Type**</span></span>|<span data-ttu-id="ed2f4-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-128">**Required**</span></span>|<span data-ttu-id="ed2f4-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-129">**Description**</span></span>|<span data-ttu-id="ed2f4-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ed2f4-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="ed2f4-131">FromCell</span></span>  <br/> |<span data-ttu-id="ed2f4-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ed2f4-132">xsd:string</span></span>  <br/> |<span data-ttu-id="ed2f4-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="ed2f4-133">optional</span></span>  <br/> |<span data-ttu-id="ed2f4-134">La cellule à l’origine une connexion.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="ed2f4-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ed2f4-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="ed2f4-136">FromPart</span></span>  <br/> |<span data-ttu-id="ed2f4-137">XSD : int</span><span class="sxs-lookup"><span data-stu-id="ed2f4-137">xsd:int</span></span>  <br/> |<span data-ttu-id="ed2f4-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="ed2f4-138">optional</span></span>  <br/> |<span data-ttu-id="ed2f4-139">La partie de la forme à partir de laquelle une connexion.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="ed2f4-140">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ed2f4-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="ed2f4-141">FromSheet</span></span>  <br/> |<span data-ttu-id="ed2f4-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ed2f4-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ed2f4-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ed2f4-143">required</span></span>  <br/> |<span data-ttu-id="ed2f4-144">L’ID de la forme à partir de laquelle une connexion ou proviennent.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="ed2f4-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ed2f4-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="ed2f4-146">ToCell</span></span>  <br/> |<span data-ttu-id="ed2f4-147">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ed2f4-147">xsd:string</span></span>  <br/> |<span data-ttu-id="ed2f4-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="ed2f4-148">optional</span></span>  <br/> |<span data-ttu-id="ed2f4-149">La cellule avec laquelle une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="ed2f4-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ed2f4-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="ed2f4-151">ToPart</span></span>  <br/> |<span data-ttu-id="ed2f4-152">XSD : int</span><span class="sxs-lookup"><span data-stu-id="ed2f4-152">xsd:int</span></span>  <br/> |<span data-ttu-id="ed2f4-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="ed2f4-153">optional</span></span>  <br/> |<span data-ttu-id="ed2f4-154">La partie de la forme avec laquelle une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="ed2f4-155">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="ed2f4-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="ed2f4-156">ToSheet</span></span>  <br/> |<span data-ttu-id="ed2f4-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ed2f4-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ed2f4-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ed2f4-158">required</span></span>  <br/> |<span data-ttu-id="ed2f4-159">L’ID de la forme à laquelle une ou plusieurs connexions sont effectuées.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="ed2f4-160">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

