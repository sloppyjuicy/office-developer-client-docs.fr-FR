---
title: Élément EventList (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contient un élément EventItem pour chaque événement auquel un objet doit répondre.
ms.openlocfilehash: 7b1406f56dddd8507e330aa93d5cfe9f390caf21
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541798"
---
# <a name="eventlist-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="50453-103">Élément EventList (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="50453-103">EventList element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="50453-104">Contient un **élément EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="50453-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="50453-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="50453-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50453-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="50453-106">**Element type**</span></span> <br/> |[<span data-ttu-id="50453-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="50453-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="50453-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="50453-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="50453-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="50453-109">**Schema file**</span></span> <br/> |<span data-ttu-id="50453-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="50453-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="50453-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="50453-111">**Document parts**</span></span> <br/> |<span data-ttu-id="50453-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="50453-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="50453-113">Définition</span><span class="sxs-lookup"><span data-stu-id="50453-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="50453-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="50453-114">Elements and attributes</span></span>

<span data-ttu-id="50453-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="50453-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="50453-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="50453-116">Parent elements</span></span>

|<span data-ttu-id="50453-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="50453-117">**Element**</span></span>|<span data-ttu-id="50453-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="50453-118">**Type**</span></span>|<span data-ttu-id="50453-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="50453-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="50453-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="50453-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="50453-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="50453-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="50453-122">Élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="50453-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="50453-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="50453-123">Child elements</span></span>

|<span data-ttu-id="50453-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="50453-124">**Element**</span></span>|<span data-ttu-id="50453-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="50453-125">**Type**</span></span>|<span data-ttu-id="50453-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="50453-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="50453-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="50453-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50453-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="50453-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="50453-129">Encapsule un code d’événement.</span><span class="sxs-lookup"><span data-stu-id="50453-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="50453-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="50453-130">Attributes</span></span>

<span data-ttu-id="50453-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="50453-131">None.</span></span>
  

