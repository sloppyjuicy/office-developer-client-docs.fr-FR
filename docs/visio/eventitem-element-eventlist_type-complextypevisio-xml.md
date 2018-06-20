---
title: Élément EventItem (EventList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsule un code d’événement.
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788572"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="67a68-103">Élément EventItem (EventList_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="67a68-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="67a68-104">Encapsule un code d’événement.</span><span class="sxs-lookup"><span data-stu-id="67a68-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67a68-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="67a68-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67a68-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="67a68-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67a68-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="67a68-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67a68-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="67a68-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67a68-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="67a68-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67a68-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="67a68-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67a68-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="67a68-111">**Document parts**</span></span> <br/> |<span data-ttu-id="67a68-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="67a68-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67a68-113">Définition</span><span class="sxs-lookup"><span data-stu-id="67a68-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67a68-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="67a68-114">Elements and attributes</span></span>

<span data-ttu-id="67a68-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="67a68-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67a68-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="67a68-116">Parent elements</span></span>

|<span data-ttu-id="67a68-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="67a68-117">**Element**</span></span>|<span data-ttu-id="67a68-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="67a68-118">**Type**</span></span>|<span data-ttu-id="67a68-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="67a68-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67a68-120">EventList</span><span class="sxs-lookup"><span data-stu-id="67a68-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67a68-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="67a68-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67a68-122">Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="67a68-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67a68-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="67a68-123">Child elements</span></span>

<span data-ttu-id="67a68-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="67a68-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67a68-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="67a68-125">Attributes</span></span>

|<span data-ttu-id="67a68-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="67a68-126">**Attribute**</span></span>|<span data-ttu-id="67a68-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="67a68-127">**Type**</span></span>|<span data-ttu-id="67a68-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="67a68-128">**Required**</span></span>|<span data-ttu-id="67a68-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="67a68-129">**Description**</span></span>|<span data-ttu-id="67a68-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="67a68-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67a68-131">Action</span><span class="sxs-lookup"><span data-stu-id="67a68-131">Action</span></span>  <br/> |<span data-ttu-id="67a68-132">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="67a68-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="67a68-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="67a68-133">required</span></span>  <br/> |<span data-ttu-id="67a68-134">Spécifie le code d’action de l’élément de **EventItem** parent.</span><span class="sxs-lookup"><span data-stu-id="67a68-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="67a68-135">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="67a68-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="67a68-136">Activé</span><span class="sxs-lookup"><span data-stu-id="67a68-136">Enabled</span></span>  <br/> |<span data-ttu-id="67a68-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="67a68-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="67a68-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="67a68-138">optional</span></span>  <br/> |<span data-ttu-id="67a68-139">Représente un indicateur indiquant si l’événement est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="67a68-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="67a68-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="67a68-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="67a68-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="67a68-141">EventCode</span></span>  <br/> |<span data-ttu-id="67a68-142">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="67a68-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="67a68-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="67a68-143">required</span></span>  <br/> |<span data-ttu-id="67a68-144">Un code indiquant l’événement qui déclenche le module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="67a68-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="67a68-145">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="67a68-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="67a68-146">ID</span><span class="sxs-lookup"><span data-stu-id="67a68-146">ID</span></span>  <br/> |<span data-ttu-id="67a68-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67a68-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67a68-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="67a68-148">required</span></span>  <br/> |<span data-ttu-id="67a68-149">ID de l’événement.</span><span class="sxs-lookup"><span data-stu-id="67a68-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="67a68-150">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="67a68-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="67a68-151">Cible</span><span class="sxs-lookup"><span data-stu-id="67a68-151">Target</span></span>  <br/> |<span data-ttu-id="67a68-152">XSD : String</span><span class="sxs-lookup"><span data-stu-id="67a68-152">xsd:string</span></span>  <br/> |<span data-ttu-id="67a68-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="67a68-153">required</span></span>  <br/> |<span data-ttu-id="67a68-154">Spécifie la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="67a68-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="67a68-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="67a68-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67a68-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="67a68-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="67a68-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="67a68-157">xsd:string</span></span>  <br/> |<span data-ttu-id="67a68-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="67a68-158">required</span></span>  <br/> |<span data-ttu-id="67a68-159">Spécifie une chaîne qui contient les arguments à envoyer à la cible d’un événement.</span><span class="sxs-lookup"><span data-stu-id="67a68-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="67a68-160">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="67a68-160">Values of the xsd:string type.</span></span>  <br/> |
   

