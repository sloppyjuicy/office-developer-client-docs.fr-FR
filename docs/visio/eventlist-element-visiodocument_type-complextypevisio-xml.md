---
title: EventList, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contient un élément EventItem pour chaque événement auquel un objet doit répondre.
ms.openlocfilehash: e1033ae93ca272b8ea1d9855d08ad13a444612db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788568"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="c1cab-103">EventList, élément (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c1cab-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c1cab-104">Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="c1cab-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c1cab-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="c1cab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1cab-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c1cab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1cab-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="c1cab-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1cab-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c1cab-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1cab-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c1cab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1cab-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c1cab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1cab-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="c1cab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1cab-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="c1cab-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1cab-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c1cab-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1cab-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c1cab-114">Elements and attributes</span></span>

<span data-ttu-id="c1cab-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c1cab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1cab-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c1cab-116">Parent elements</span></span>

|<span data-ttu-id="c1cab-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c1cab-117">**Element**</span></span>|<span data-ttu-id="c1cab-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="c1cab-118">**Type**</span></span>|<span data-ttu-id="c1cab-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c1cab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1cab-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="c1cab-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="c1cab-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="c1cab-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1cab-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="c1cab-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1cab-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1cab-123">Child elements</span></span>

|<span data-ttu-id="c1cab-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c1cab-124">**Element**</span></span>|<span data-ttu-id="c1cab-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="c1cab-125">**Type**</span></span>|<span data-ttu-id="c1cab-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="c1cab-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1cab-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="c1cab-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1cab-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="c1cab-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1cab-129">Encapsule un code d’événement.</span><span class="sxs-lookup"><span data-stu-id="c1cab-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c1cab-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="c1cab-130">Attributes</span></span>

<span data-ttu-id="c1cab-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c1cab-131">None.</span></span>
  

