---
title: Élément EventItem (EventList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsule un code d’événement.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394397"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="29386-103">Élément EventItem (EventList_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="29386-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="29386-104">Encapsule un code d’événement.</span><span class="sxs-lookup"><span data-stu-id="29386-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29386-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="29386-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29386-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="29386-106">**Element type**</span></span> <br/> |[<span data-ttu-id="29386-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="29386-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="29386-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="29386-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="29386-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="29386-109">**Schema file**</span></span> <br/> |<span data-ttu-id="29386-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="29386-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="29386-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="29386-111">**Document parts**</span></span> <br/> |<span data-ttu-id="29386-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="29386-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="29386-113">Définition</span><span class="sxs-lookup"><span data-stu-id="29386-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="29386-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="29386-114">Elements and attributes</span></span>

<span data-ttu-id="29386-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="29386-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="29386-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="29386-116">Parent elements</span></span>

|<span data-ttu-id="29386-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="29386-117">**Element**</span></span>|<span data-ttu-id="29386-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="29386-118">**Type**</span></span>|<span data-ttu-id="29386-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="29386-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29386-120">EventList</span><span class="sxs-lookup"><span data-stu-id="29386-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="29386-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="29386-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29386-122">Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="29386-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="29386-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="29386-123">Child elements</span></span>

<span data-ttu-id="29386-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="29386-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29386-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="29386-125">Attributes</span></span>

|<span data-ttu-id="29386-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="29386-126">**Attribute**</span></span>|<span data-ttu-id="29386-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="29386-127">**Type**</span></span>|<span data-ttu-id="29386-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="29386-128">**Required**</span></span>|<span data-ttu-id="29386-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="29386-129">**Description**</span></span>|<span data-ttu-id="29386-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="29386-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="29386-131">Opération</span><span class="sxs-lookup"><span data-stu-id="29386-131">Action</span></span>  <br/> |<span data-ttu-id="29386-132">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="29386-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="29386-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29386-133">required</span></span>  <br/> |<span data-ttu-id="29386-134">Spécifie le code d’action de l’élément de **EventItem** parent.</span><span class="sxs-lookup"><span data-stu-id="29386-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="29386-135">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="29386-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="29386-136">Activé</span><span class="sxs-lookup"><span data-stu-id="29386-136">Enabled</span></span>  <br/> |<span data-ttu-id="29386-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="29386-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="29386-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="29386-138">optional</span></span>  <br/> |<span data-ttu-id="29386-139">Représente un indicateur indiquant si l’événement est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="29386-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="29386-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="29386-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="29386-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="29386-141">EventCode</span></span>  <br/> |<span data-ttu-id="29386-142">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="29386-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="29386-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29386-143">required</span></span>  <br/> |<span data-ttu-id="29386-144">Un code indiquant l’événement qui déclenche le module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="29386-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="29386-145">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="29386-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="29386-146">ID</span><span class="sxs-lookup"><span data-stu-id="29386-146">ID</span></span>  <br/> |<span data-ttu-id="29386-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="29386-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29386-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29386-148">required</span></span>  <br/> |<span data-ttu-id="29386-149">ID de l’événement.</span><span class="sxs-lookup"><span data-stu-id="29386-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="29386-150">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="29386-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="29386-151">Cible</span><span class="sxs-lookup"><span data-stu-id="29386-151">Target</span></span>  <br/> |<span data-ttu-id="29386-152">XSD : String</span><span class="sxs-lookup"><span data-stu-id="29386-152">xsd:string</span></span>  <br/> |<span data-ttu-id="29386-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29386-153">required</span></span>  <br/> |<span data-ttu-id="29386-154">Spécifie la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="29386-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="29386-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="29386-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="29386-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="29386-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="29386-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="29386-157">xsd:string</span></span>  <br/> |<span data-ttu-id="29386-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="29386-158">required</span></span>  <br/> |<span data-ttu-id="29386-159">Spécifie une chaîne qui contient les arguments à envoyer à la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="29386-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="29386-160">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="29386-160">Values of the xsd:string type.</span></span>  <br/> |
   

