---
title: Élément EventItem (complexType EventList_Type) (XML Visio)
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
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="8c08b-103">Élément EventItem (complexType EventList_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="8c08b-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8c08b-104">Encapsule un code d’événement.</span><span class="sxs-lookup"><span data-stu-id="8c08b-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c08b-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="8c08b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c08b-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="8c08b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8c08b-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="8c08b-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8c08b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8c08b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8c08b-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="8c08b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8c08b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8c08b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8c08b-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="8c08b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8c08b-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="8c08b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8c08b-113">Définition</span><span class="sxs-lookup"><span data-stu-id="8c08b-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8c08b-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="8c08b-114">Elements and attributes</span></span>

<span data-ttu-id="8c08b-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="8c08b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8c08b-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8c08b-116">Parent elements</span></span>

|<span data-ttu-id="8c08b-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8c08b-117">**Element**</span></span>|<span data-ttu-id="8c08b-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="8c08b-118">**Type**</span></span>|<span data-ttu-id="8c08b-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="8c08b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c08b-120">EventList</span><span class="sxs-lookup"><span data-stu-id="8c08b-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c08b-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="8c08b-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8c08b-122">Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="8c08b-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8c08b-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8c08b-123">Child elements</span></span>

<span data-ttu-id="8c08b-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8c08b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c08b-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="8c08b-125">Attributes</span></span>

|<span data-ttu-id="8c08b-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8c08b-126">**Attribute**</span></span>|<span data-ttu-id="8c08b-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="8c08b-127">**Type**</span></span>|<span data-ttu-id="8c08b-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8c08b-128">**Required**</span></span>|<span data-ttu-id="8c08b-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="8c08b-129">**Description**</span></span>|<span data-ttu-id="8c08b-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8c08b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8c08b-131">Action</span><span class="sxs-lookup"><span data-stu-id="8c08b-131">Action</span></span>  <br/> |<span data-ttu-id="8c08b-132">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8c08b-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8c08b-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c08b-133">required</span></span>  <br/> |<span data-ttu-id="8c08b-134">Spécifie le code d’action de l’élément **EventItem** parent.</span><span class="sxs-lookup"><span data-stu-id="8c08b-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="8c08b-135">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8c08b-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8c08b-136">Activé</span><span class="sxs-lookup"><span data-stu-id="8c08b-136">Enabled</span></span>  <br/> |<span data-ttu-id="8c08b-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="8c08b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8c08b-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="8c08b-138">optional</span></span>  <br/> |<span data-ttu-id="8c08b-139">Représente un indicateur qui indique si l’événement est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="8c08b-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="8c08b-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8c08b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8c08b-141">CodeÉvénement</span><span class="sxs-lookup"><span data-stu-id="8c08b-141">EventCode</span></span>  <br/> |<span data-ttu-id="8c08b-142">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8c08b-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8c08b-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c08b-143">required</span></span>  <br/> |<span data-ttu-id="8c08b-144">Code indiquant l’événement qui déclenche le module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="8c08b-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="8c08b-145">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8c08b-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8c08b-146">ID</span><span class="sxs-lookup"><span data-stu-id="8c08b-146">ID</span></span>  <br/> |<span data-ttu-id="8c08b-147">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8c08b-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8c08b-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c08b-148">required</span></span>  <br/> |<span data-ttu-id="8c08b-149">ID de l’événement.</span><span class="sxs-lookup"><span data-stu-id="8c08b-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="8c08b-150">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8c08b-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8c08b-151">Target</span><span class="sxs-lookup"><span data-stu-id="8c08b-151">Target</span></span>  <br/> |<span data-ttu-id="8c08b-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8c08b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="8c08b-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c08b-153">required</span></span>  <br/> |<span data-ttu-id="8c08b-154">Spécifie la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="8c08b-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="8c08b-155">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8c08b-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8c08b-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="8c08b-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="8c08b-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8c08b-157">xsd:string</span></span>  <br/> |<span data-ttu-id="8c08b-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c08b-158">required</span></span>  <br/> |<span data-ttu-id="8c08b-159">Spécifie une chaîne contenant des arguments à envoyer à la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="8c08b-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="8c08b-160">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8c08b-160">Values of the xsd:string type.</span></span>  <br/> |
   

