---
title: Élément activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: L'élément activityDetails stocke les données brutes pour un élément de flux d'activité unique. Chaque élément de flux d'activité doit disposer de son propre élément activityDetails. Les données de l'élément activityDetails sont référencées dans les modèles d'activité à l'aide d'éléments Name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434871"
---
# <a name="activitydetails-element"></a><span data-ttu-id="ffdd8-105">Élément activityDetails</span><span class="sxs-lookup"><span data-stu-id="ffdd8-105">activityDetails Element</span></span>

<span data-ttu-id="ffdd8-106">L'élément **activityDetails** stocke les données brutes pour un élément de flux d'activité unique.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="ffdd8-107">Chaque élément de flux d'activité doit disposer de son propre élément **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="ffdd8-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="ffdd8-108">Les données de l'élément **activityDetails** sont référencées dans les modèles d'activité à l'aide d'éléments **Name** .</span><span class="sxs-lookup"><span data-stu-id="ffdd8-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="ffdd8-109">Chaque élément de données dans l'élément **activityDetails** doit avoir un élément **Name** .</span><span class="sxs-lookup"><span data-stu-id="ffdd8-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="ffdd8-110">Le tableau suivant décrit les six éléments requis par l'élément **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="ffdd8-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="ffdd8-111">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-111">**Element**</span></span>|<span data-ttu-id="ffdd8-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffdd8-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-113">**ownerID**</span></span> <br/> |<span data-ttu-id="ffdd8-114">ID de l'utilisateur sur le réseau social qui a généré cet élément de flux d'activité.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="ffdd8-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-115">**objectID**</span></span> <br/> |<span data-ttu-id="ffdd8-116">Une chaîne unique pour l'élément de flux d'activités afin de détecter les éléments de flux en double.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="ffdd8-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-117">**applicationId**</span></span> <br/> |<span data-ttu-id="ffdd8-118">Un des deux ID uniques qui sont utilisés pour faire correspondre l'élément de flux d'activités avec son modèle.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="ffdd8-119">Si vous avez plusieurs applications ou autres groupements, il peut être utilisé en tant qu'organisateur de modèles de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="ffdd8-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-120">**templateId**</span></span> <br/> |<span data-ttu-id="ffdd8-121">Deuxième ID unique utilisé pour faire correspondre l'élément de flux d'activités avec son modèle.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="ffdd8-122">Il peut être utilisé en tant qu'organisateur de modèles de second niveau.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="ffdd8-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-123">**publishDate**</span></span> <br/> |<span data-ttu-id="ffdd8-124">Date et heure de publication de l'élément de flux d'activités.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="ffdd8-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="ffdd8-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="ffdd8-126">Les données à utiliser dans les jetons pour le modèle d'élément de flux d'activités.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="ffdd8-127">Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML de flux d'activités](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="ffdd8-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ffdd8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffdd8-128">See also</span></span>

- [<span data-ttu-id="ffdd8-129">Vue d'ensemble du code XML pour un élément de flux d'activité</span><span class="sxs-lookup"><span data-stu-id="ffdd8-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="ffdd8-130">Élément activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="ffdd8-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="ffdd8-131">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="ffdd8-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="ffdd8-132">Instructions pour afficher correctement les activités</span><span class="sxs-lookup"><span data-stu-id="ffdd8-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="ffdd8-133">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="ffdd8-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="ffdd8-134">Schéma XML du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="ffdd8-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="ffdd8-135">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="ffdd8-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

