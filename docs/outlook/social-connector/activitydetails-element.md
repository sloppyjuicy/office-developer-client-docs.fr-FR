---
title: activityDetails, élément
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: L’élément activityDetails stocke les données brutes pour une seule activité de flux d’élément. Chaque activité flux élément doit avoir son propre élément activityDetails. Les données dans l’élément activityDetails sont référencées dans les modèles d’activité à l’aide des éléments de nom.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787579"
---
# <a name="activitydetails-element"></a><span data-ttu-id="85a03-105">activityDetails, élément</span><span class="sxs-lookup"><span data-stu-id="85a03-105">activityDetails Element</span></span>

<span data-ttu-id="85a03-106">L’élément **activityDetails** stocke les données brutes pour une seule activité de flux d’élément.</span><span class="sxs-lookup"><span data-stu-id="85a03-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="85a03-107">Chaque activité flux élément doit avoir son propre élément **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="85a03-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="85a03-108">Les données dans l’élément **activityDetails** sont référencées dans les modèles d’activité à l’aide des éléments de **nom** .</span><span class="sxs-lookup"><span data-stu-id="85a03-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="85a03-109">Chaque élément de données dans l’élément **activityDetails** doit avoir un élément de **nom** .</span><span class="sxs-lookup"><span data-stu-id="85a03-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="85a03-110">Le tableau suivant décrit les six éléments nécessitant l’élément **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="85a03-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="85a03-111">**Élément**</span><span class="sxs-lookup"><span data-stu-id="85a03-111">**Element**</span></span>|<span data-ttu-id="85a03-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="85a03-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85a03-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="85a03-113">**ownerID**</span></span> <br/> |<span data-ttu-id="85a03-114">L’ID de l’utilisateur sur le réseau social qui a généré cette activité de flux d’élément.</span><span class="sxs-lookup"><span data-stu-id="85a03-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="85a03-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="85a03-115">**objectID**</span></span> <br/> |<span data-ttu-id="85a03-116">Une chaîne unique pour l’activité de flux de l’élément pour détecter les éléments d’alimentation en double.</span><span class="sxs-lookup"><span data-stu-id="85a03-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="85a03-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="85a03-117">**applicationId**</span></span> <br/> |<span data-ttu-id="85a03-118">Une des deux identificateurs uniques qui sont utilisés pour la correspondance de l’activité de flux élément avec son modèle.</span><span class="sxs-lookup"><span data-stu-id="85a03-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="85a03-119">Si vous disposez de plusieurs applications ou autres groupes, il peut servir en tant qu’un organisateur de modèle de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="85a03-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="85a03-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="85a03-120">**templateId**</span></span> <br/> |<span data-ttu-id="85a03-121">Le second ID unique qui est utilisé pour la correspondance de l’activité de flux élément avec son modèle.</span><span class="sxs-lookup"><span data-stu-id="85a03-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="85a03-122">Cela peut servir d’un organisateur de modèle de second niveau.</span><span class="sxs-lookup"><span data-stu-id="85a03-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="85a03-123">**date de publication**</span><span class="sxs-lookup"><span data-stu-id="85a03-123">**publishDate**</span></span> <br/> |<span data-ttu-id="85a03-124">La date et l’heure de l’activité de flux d’élément a été publié.</span><span class="sxs-lookup"><span data-stu-id="85a03-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="85a03-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="85a03-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="85a03-126">Les données à utiliser dans les jetons de l’activité de flux de modèle d’élément.</span><span class="sxs-lookup"><span data-stu-id="85a03-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="85a03-127">Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="85a03-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="85a03-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85a03-128">See also</span></span>

- [<span data-ttu-id="85a03-129">Vue d’ensemble du code XML pour une activité de flux d’élément</span><span class="sxs-lookup"><span data-stu-id="85a03-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="85a03-130">activityTemplateContainer, élément</span><span class="sxs-lookup"><span data-stu-id="85a03-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="85a03-131">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="85a03-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="85a03-132">Conseils pour l’affichage correctement les activités</span><span class="sxs-lookup"><span data-stu-id="85a03-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="85a03-133">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="85a03-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="85a03-134">Fournisseur Outlook Social Connector schéma XML</span><span class="sxs-lookup"><span data-stu-id="85a03-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="85a03-135">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="85a03-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

