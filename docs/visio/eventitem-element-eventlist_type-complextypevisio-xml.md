---
title: Élément EventItem (complexType EventList_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: EnCapsule un code d'événement.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337197"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="c92c6-103">Élément EventItem (complexType EventList_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c92c6-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c92c6-104">EnCapsule un code d'événement.</span><span class="sxs-lookup"><span data-stu-id="c92c6-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c92c6-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="c92c6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c92c6-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c92c6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c92c6-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="c92c6-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c92c6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c92c6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c92c6-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c92c6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c92c6-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c92c6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c92c6-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="c92c6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c92c6-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="c92c6-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c92c6-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c92c6-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c92c6-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c92c6-114">Elements and attributes</span></span>

<span data-ttu-id="c92c6-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="c92c6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c92c6-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c92c6-116">Parent elements</span></span>

|<span data-ttu-id="c92c6-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c92c6-117">**Element**</span></span>|<span data-ttu-id="c92c6-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="c92c6-118">**Type**</span></span>|<span data-ttu-id="c92c6-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c92c6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c92c6-120">EventList</span><span class="sxs-lookup"><span data-stu-id="c92c6-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c92c6-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="c92c6-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c92c6-122">Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="c92c6-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c92c6-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c92c6-123">Child elements</span></span>

<span data-ttu-id="c92c6-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c92c6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c92c6-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="c92c6-125">Attributes</span></span>

|<span data-ttu-id="c92c6-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c92c6-126">**Attribute**</span></span>|<span data-ttu-id="c92c6-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="c92c6-127">**Type**</span></span>|<span data-ttu-id="c92c6-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c92c6-128">**Required**</span></span>|<span data-ttu-id="c92c6-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="c92c6-129">**Description**</span></span>|<span data-ttu-id="c92c6-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c92c6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c92c6-131">Action</span><span class="sxs-lookup"><span data-stu-id="c92c6-131">Action</span></span>  <br/> |<span data-ttu-id="c92c6-132">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c92c6-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c92c6-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92c6-133">required</span></span>  <br/> |<span data-ttu-id="c92c6-134">Spécifie le code d'action de l'élément **EventItem** parent.</span><span class="sxs-lookup"><span data-stu-id="c92c6-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="c92c6-135">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c92c6-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c92c6-136">Activé</span><span class="sxs-lookup"><span data-stu-id="c92c6-136">Enabled</span></span>  <br/> |<span data-ttu-id="c92c6-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="c92c6-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c92c6-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="c92c6-138">optional</span></span>  <br/> |<span data-ttu-id="c92c6-139">Représente un indicateur qui indique si l'événement est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="c92c6-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="c92c6-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c92c6-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c92c6-141">CodeÉvénement</span><span class="sxs-lookup"><span data-stu-id="c92c6-141">EventCode</span></span>  <br/> |<span data-ttu-id="c92c6-142">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c92c6-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c92c6-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92c6-143">required</span></span>  <br/> |<span data-ttu-id="c92c6-144">Code indiquant l'événement qui déclenche le module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="c92c6-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="c92c6-145">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c92c6-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c92c6-146">ID</span><span class="sxs-lookup"><span data-stu-id="c92c6-146">ID</span></span>  <br/> |<span data-ttu-id="c92c6-147">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c92c6-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c92c6-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92c6-148">required</span></span>  <br/> |<span data-ttu-id="c92c6-149">ID de l'événement.</span><span class="sxs-lookup"><span data-stu-id="c92c6-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="c92c6-150">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c92c6-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c92c6-151">Target</span><span class="sxs-lookup"><span data-stu-id="c92c6-151">Target</span></span>  <br/> |<span data-ttu-id="c92c6-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c92c6-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c92c6-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92c6-153">required</span></span>  <br/> |<span data-ttu-id="c92c6-154">Spécifie la cible d'un événement.</span><span class="sxs-lookup"><span data-stu-id="c92c6-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="c92c6-155">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c92c6-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c92c6-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="c92c6-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="c92c6-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c92c6-157">xsd:string</span></span>  <br/> |<span data-ttu-id="c92c6-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92c6-158">required</span></span>  <br/> |<span data-ttu-id="c92c6-159">Spécifie une chaîne contenant des arguments à envoyer à la cible d'un événement.</span><span class="sxs-lookup"><span data-stu-id="c92c6-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="c92c6-160">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c92c6-160">Values of the xsd:string type.</span></span>  <br/> |
   

