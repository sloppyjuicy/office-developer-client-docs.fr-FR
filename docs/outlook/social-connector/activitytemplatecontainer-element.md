---
title: activityTemplateContainer, élément
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un élément activityTemplateContainer est un modèle qui vous permet de mettre en forme les éléments d’informations sur les activités et la réutilisation XML qui spécifie une mise en forme.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787582"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="7913e-103">activityTemplateContainer, élément</span><span class="sxs-lookup"><span data-stu-id="7913e-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="7913e-104">Un élément **activityTemplateContainer** est un modèle qui vous permet de mettre en forme les éléments d’informations sur les activités et la réutilisation XML qui spécifie une mise en forme.</span><span class="sxs-lookup"><span data-stu-id="7913e-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="7913e-105">Utilisez l’ID (**applicationID** et **templateID**) pour correspondre à un élément de flux (**activityDetails**) à un modèle (**activityTemplateContainer**).</span><span class="sxs-lookup"><span data-stu-id="7913e-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="7913e-106">Stocker les données de mise en page dans le cadre de l’élément **activityTemplate** .</span><span class="sxs-lookup"><span data-stu-id="7913e-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="7913e-107">Pour référencer des données sont extraites de l’activité individuelle flux élément, utilisez variables de modèle comme espaces réservés pour des informations telles que des personnes, des liens et le texte.</span><span class="sxs-lookup"><span data-stu-id="7913e-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="7913e-108">Le tableau suivant décrit les trois éléments nécessitant l’élément **activityTemplateContainer** .</span><span class="sxs-lookup"><span data-stu-id="7913e-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="7913e-109">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7913e-109">**Element**</span></span>|<span data-ttu-id="7913e-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="7913e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7913e-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="7913e-111">**applicationID**</span></span> <br/> |<span data-ttu-id="7913e-112">Une des deux identificateurs uniques qui sont utilisés pour la correspondance de l’élément de flux avec son modèle.</span><span class="sxs-lookup"><span data-stu-id="7913e-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="7913e-113">Si vous disposez de plusieurs applications ou autres groupes, il peut servir en tant qu’un organisateur de modèle de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="7913e-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="7913e-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="7913e-114">**templateID**</span></span> <br/> |<span data-ttu-id="7913e-115">Second ID unique qui est utilisée pour la correspondance de l’élément à son modèle de flux.</span><span class="sxs-lookup"><span data-stu-id="7913e-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="7913e-116">Cela peut servir d’un organisateur de modèle de second niveau.</span><span class="sxs-lookup"><span data-stu-id="7913e-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="7913e-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="7913e-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="7913e-118">La mise en page du modèle (éléments de **données** , le **titre**et**icône**) et le type d’activité (**type** d’élément).</span><span class="sxs-lookup"><span data-stu-id="7913e-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="7913e-119">Le tableau suivant décrit les éléments enfants **activityTemplate**, qui décrivent la mise en page et le type d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="7913e-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="7913e-120">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7913e-120">**Element**</span></span>|<span data-ttu-id="7913e-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="7913e-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7913e-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="7913e-122">**icon**</span></span> <br/> |<span data-ttu-id="7913e-123">Un jeton de liaison, qui fait référence à l’URL de l’icône de cet élément de flux.</span><span class="sxs-lookup"><span data-stu-id="7913e-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="7913e-124">**title**</span><span class="sxs-lookup"><span data-stu-id="7913e-124">**title**</span></span> <br/> |<span data-ttu-id="7913e-125">Les informations requises pour l’élément de flux.</span><span class="sxs-lookup"><span data-stu-id="7913e-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="7913e-126">**type**</span><span class="sxs-lookup"><span data-stu-id="7913e-126">**type**</span></span> <br/> |<span data-ttu-id="7913e-127">Le type d’activité, par exemple une mise à jour d’état, photo ou document.</span><span class="sxs-lookup"><span data-stu-id="7913e-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="7913e-128">**data**</span><span class="sxs-lookup"><span data-stu-id="7913e-128">**data**</span></span> <br/> |<span data-ttu-id="7913e-129">Des informations supplémentaires pour l’élément de flux, tels que des images, du texte ou des liens.</span><span class="sxs-lookup"><span data-stu-id="7913e-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="7913e-130">Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="7913e-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7913e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7913e-131">See also</span></span>

- [<span data-ttu-id="7913e-132">Vue d’ensemble du code XML pour une activité de flux d’élément</span><span class="sxs-lookup"><span data-stu-id="7913e-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="7913e-133">activityDetails, élément</span><span class="sxs-lookup"><span data-stu-id="7913e-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="7913e-134">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="7913e-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="7913e-135">Conseils pour l’affichage correctement les activités</span><span class="sxs-lookup"><span data-stu-id="7913e-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="7913e-136">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="7913e-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="7913e-137">Fournisseur Outlook Social Connector schéma XML</span><span class="sxs-lookup"><span data-stu-id="7913e-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="7913e-138">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="7913e-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

