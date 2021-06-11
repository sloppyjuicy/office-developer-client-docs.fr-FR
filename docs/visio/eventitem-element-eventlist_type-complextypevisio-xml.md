---
title: Élément EventItem (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsule un code d’événement.
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541840"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a><span data-ttu-id="29089-103">Élément EventItem (EventList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="29089-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="29089-104">Encapsule un code d’événement.</span><span class="sxs-lookup"><span data-stu-id="29089-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29089-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="29089-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29089-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="29089-106">**Element type**</span></span> <br/> |[<span data-ttu-id="29089-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="29089-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="29089-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="29089-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="29089-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="29089-109">**Schema file**</span></span> <br/> |<span data-ttu-id="29089-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="29089-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="29089-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="29089-111">**Document parts**</span></span> <br/> |<span data-ttu-id="29089-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="29089-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="29089-113">Définition</span><span class="sxs-lookup"><span data-stu-id="29089-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="29089-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="29089-114">Elements and attributes</span></span>

<span data-ttu-id="29089-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="29089-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="29089-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="29089-116">Parent elements</span></span>

|<span data-ttu-id="29089-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="29089-117">**Element**</span></span>|<span data-ttu-id="29089-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="29089-118">**Type**</span></span>|<span data-ttu-id="29089-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="29089-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29089-120">EventList</span><span class="sxs-lookup"><span data-stu-id="29089-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="29089-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="29089-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29089-122">Contient un **élément EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="29089-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="29089-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="29089-123">Child elements</span></span>

<span data-ttu-id="29089-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="29089-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29089-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="29089-125">Attributes</span></span>

|<span data-ttu-id="29089-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="29089-126">**Attribute**</span></span>|<span data-ttu-id="29089-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="29089-127">**Type**</span></span>|<span data-ttu-id="29089-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="29089-128">**Required**</span></span>|<span data-ttu-id="29089-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="29089-129">**Description**</span></span>|<span data-ttu-id="29089-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="29089-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="29089-131">Action</span><span class="sxs-lookup"><span data-stu-id="29089-131">Action</span></span>  <br/> |<span data-ttu-id="29089-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="29089-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="29089-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29089-133">required</span></span>  <br/> |<span data-ttu-id="29089-134">Spécifie le code d’action de **l’élément EventItem** parent.</span><span class="sxs-lookup"><span data-stu-id="29089-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="29089-135">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="29089-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="29089-136">Activé</span><span class="sxs-lookup"><span data-stu-id="29089-136">Enabled</span></span>  <br/> |<span data-ttu-id="29089-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="29089-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="29089-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="29089-138">optional</span></span>  <br/> |<span data-ttu-id="29089-139">Représente un indicateur indiquant si l’événement est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="29089-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="29089-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="29089-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="29089-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="29089-141">EventCode</span></span>  <br/> |<span data-ttu-id="29089-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="29089-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="29089-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29089-143">required</span></span>  <br/> |<span data-ttu-id="29089-144">Code indiquant l’événement qui déclenche l’module.</span><span class="sxs-lookup"><span data-stu-id="29089-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="29089-145">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="29089-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="29089-146">ID</span><span class="sxs-lookup"><span data-stu-id="29089-146">ID</span></span>  <br/> |<span data-ttu-id="29089-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="29089-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29089-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29089-148">required</span></span>  <br/> |<span data-ttu-id="29089-149">ID de l’événement.</span><span class="sxs-lookup"><span data-stu-id="29089-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="29089-150">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="29089-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="29089-151">Target</span><span class="sxs-lookup"><span data-stu-id="29089-151">Target</span></span>  <br/> |<span data-ttu-id="29089-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="29089-152">xsd:string</span></span>  <br/> |<span data-ttu-id="29089-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29089-153">required</span></span>  <br/> |<span data-ttu-id="29089-154">Spécifie la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="29089-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="29089-155">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="29089-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="29089-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="29089-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="29089-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="29089-157">xsd:string</span></span>  <br/> |<span data-ttu-id="29089-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29089-158">required</span></span>  <br/> |<span data-ttu-id="29089-159">Spécifie une chaîne contenant des arguments à envoyer à la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="29089-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="29089-160">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="29089-160">Values of the xsd:string type.</span></span>  <br/> |
   

