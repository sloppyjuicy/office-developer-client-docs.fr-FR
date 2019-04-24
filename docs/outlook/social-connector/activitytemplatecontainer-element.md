---
title: Élément activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un élément activityTemplateContainer est un modèle qui vous permet de mettre en forme vos éléments de flux d'activités et de réutiliser du code XML qui spécifie une mise en page.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281119"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="12030-103">Élément activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="12030-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="12030-104">Un élément **activityTemplateContainer** est un modèle qui vous permet de mettre en forme vos éléments de flux d'activités et de réutiliser du code XML qui spécifie une mise en page.</span><span class="sxs-lookup"><span data-stu-id="12030-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="12030-105">Utilisez les ID (**ApplicationID** et **TemplateID**) pour faire correspondre un élément de flux (**activityDetails**) à un modèle (**activityTemplateContainer**).</span><span class="sxs-lookup"><span data-stu-id="12030-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="12030-106">Stockez les données de disposition dans le cadre de l'élément **ActivityTemplate** .</span><span class="sxs-lookup"><span data-stu-id="12030-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="12030-107">Pour référencer des données qui sont extraites de l'élément de flux d'activités individuel, utilisez des variables de modèle comme espaces réservés pour des informations telles que des personnes, des liens et du texte.</span><span class="sxs-lookup"><span data-stu-id="12030-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="12030-108">Le tableau suivant décrit les trois éléments requis par l'élément **activityTemplateContainer** .</span><span class="sxs-lookup"><span data-stu-id="12030-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="12030-109">**Élément**</span><span class="sxs-lookup"><span data-stu-id="12030-109">**Element**</span></span>|<span data-ttu-id="12030-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="12030-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12030-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="12030-111">**applicationID**</span></span> <br/> |<span data-ttu-id="12030-112">Un des deux ID uniques qui sont utilisés pour faire correspondre l'élément de flux à son modèle.</span><span class="sxs-lookup"><span data-stu-id="12030-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="12030-113">Si vous avez plusieurs applications ou autres groupements, il peut être utilisé en tant qu'organisateur de modèles de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="12030-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="12030-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="12030-114">**templateID**</span></span> <br/> |<span data-ttu-id="12030-115">Deuxième ID unique utilisé pour faire correspondre l'élément de flux à son modèle.</span><span class="sxs-lookup"><span data-stu-id="12030-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="12030-116">Il peut être utilisé en tant qu'organisateur de modèles de second niveau.</span><span class="sxs-lookup"><span data-stu-id="12030-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="12030-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="12030-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="12030-118">La disposition du modèle (**icône**, **titre**et éléments de **données** ) et le type d'activité (élément**type** ).</span><span class="sxs-lookup"><span data-stu-id="12030-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="12030-119">Le tableau suivant décrit les éléments enfants de **ActivityTemplate**, qui décrivent la mise en page et le type d'un modèle.</span><span class="sxs-lookup"><span data-stu-id="12030-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="12030-120">**Élément**</span><span class="sxs-lookup"><span data-stu-id="12030-120">**Element**</span></span>|<span data-ttu-id="12030-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="12030-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12030-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="12030-122">**icon**</span></span> <br/> |<span data-ttu-id="12030-123">Un jeton de liaison, qui fait référence à l'URL de l'icône de cet élément de flux.</span><span class="sxs-lookup"><span data-stu-id="12030-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="12030-124">**title**</span><span class="sxs-lookup"><span data-stu-id="12030-124">**title**</span></span> <br/> |<span data-ttu-id="12030-125">Informations requises pour l'élément de flux.</span><span class="sxs-lookup"><span data-stu-id="12030-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="12030-126">**type**</span><span class="sxs-lookup"><span data-stu-id="12030-126">**type**</span></span> <br/> |<span data-ttu-id="12030-127">Type d'activité, par exemple une mise à jour de l'État, de la photo ou du document.</span><span class="sxs-lookup"><span data-stu-id="12030-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="12030-128">**data**</span><span class="sxs-lookup"><span data-stu-id="12030-128">**data**</span></span> <br/> |<span data-ttu-id="12030-129">Informations supplémentaires pour l'élément de flux, telles que des images, du texte ou des liens.</span><span class="sxs-lookup"><span data-stu-id="12030-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="12030-130">Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML de flux d'activités](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="12030-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12030-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12030-131">See also</span></span>

- [<span data-ttu-id="12030-132">Vue d'ensemble du code XML pour un élément de flux d'activité</span><span class="sxs-lookup"><span data-stu-id="12030-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="12030-133">Élément activityDetails</span><span class="sxs-lookup"><span data-stu-id="12030-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="12030-134">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="12030-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="12030-135">Instructions pour afficher correctement les activités</span><span class="sxs-lookup"><span data-stu-id="12030-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="12030-136">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="12030-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="12030-137">Schéma XML du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="12030-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="12030-138">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="12030-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

