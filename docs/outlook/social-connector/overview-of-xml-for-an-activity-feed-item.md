---
title: Vue d’ensemble du code XML pour un élément de flux d’activité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: "Un flux d'activités se compose d'une ou de plusieurs activités se produisant sur un réseau social. Chaque flux d'activité est représenté par un élément activityFeed et se caractérise par ces trois éléments d'information:"
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439946"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="43d25-104">Vue d’ensemble du code XML pour un élément de flux d’activité</span><span class="sxs-lookup"><span data-stu-id="43d25-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="43d25-105">Un flux d'activités se compose d'une ou de plusieurs activités se produisant sur un réseau social.</span><span class="sxs-lookup"><span data-stu-id="43d25-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="43d25-106">Chaque flux d'activité est représenté par un élément **activityFeed** et se caractérise par ces trois éléments d'information:</span><span class="sxs-lookup"><span data-stu-id="43d25-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="43d25-107">**réseau**: nom du réseau social à l'origine des activités.</span><span class="sxs-lookup"><span data-stu-id="43d25-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="43d25-108">**activités**: conteneur pour les activités se produisant sur le compte de l'utilisateur connecté sur ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="43d25-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="43d25-109">**Templates**: conteneur pour les modèles qui sont utilisés pour afficher l'élément d'activité correspondant dans les **activités**.</span><span class="sxs-lookup"><span data-stu-id="43d25-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="43d25-110">Pour créer un élément de flux d'activités, vous devez vous conformer au schéma XML de l'extensibilité du fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="43d25-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="43d25-111">La figure 1 illustre la structure XML de flux d'activités.</span><span class="sxs-lookup"><span data-stu-id="43d25-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="43d25-112">**Figure 1. Structure XML des informations sur les activités**</span><span class="sxs-lookup"><span data-stu-id="43d25-112">**Figure 1. Activity feed XML structure**</span></span>

![Structure XML d’activité](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="43d25-114">Pour chaque élément de flux d'activités, les deux parties les plus importantes de ce schéma sont les éléments **activityDetails** et **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="43d25-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="43d25-115">L'élément **activityDetails** stocke des informations spécifiques pour chaque élément de flux d'activité, telles que le nom du propriétaire de l'activité ou l'URL des images chargées.</span><span class="sxs-lookup"><span data-stu-id="43d25-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="43d25-116">L'élément **activityTemplateContainer** stocke le format ou la mise en page de chaque élément de flux d'activité.</span><span class="sxs-lookup"><span data-stu-id="43d25-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="43d25-117">Elle se compose de modèles, représentés par des éléments **ActivityTemplate** individuels, qui peuvent être réutilisés pour plusieurs éléments de flux.</span><span class="sxs-lookup"><span data-stu-id="43d25-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="43d25-118">Pour un élément de flux d'activités individuel, l'élément **ActivityTemplate** spécifie les quatre éléments d'information suivants:</span><span class="sxs-lookup"><span data-stu-id="43d25-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="43d25-119">**Icon**— spécifie l'URL de l'icône qui affiche l'élément de flux d'activités.</span><span class="sxs-lookup"><span data-stu-id="43d25-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="43d25-120">**titre**— décrit l'élément de flux d'activités.</span><span class="sxs-lookup"><span data-stu-id="43d25-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="43d25-121">**type**— spécifie le type d'activité, par exemple un État, une photo ou une mise à jour de document.</span><span class="sxs-lookup"><span data-stu-id="43d25-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="43d25-122">**Data**— spécifie toutes les informations supplémentaires affichées avec l'élément de flux d'activité.</span><span class="sxs-lookup"><span data-stu-id="43d25-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="43d25-123">L'icône affichée dans le flux d'activités est toujours identique à l'icône du fournisseur renvoyée par la propriété **ISocialProvider:: SocialNetworkIcon** .</span><span class="sxs-lookup"><span data-stu-id="43d25-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="43d25-124">Pour plus d'informations sur l'élément **activityDetails** , l'élément **activityTemplateContainer** , les jetons de modèle et les variables de modèle, consultez les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="43d25-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="43d25-125">Élément activityDetails</span><span class="sxs-lookup"><span data-stu-id="43d25-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="43d25-126">Élément activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="43d25-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="43d25-127">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="43d25-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="43d25-128">Instructions pour afficher correctement les activités</span><span class="sxs-lookup"><span data-stu-id="43d25-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="43d25-129">Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML](activity-feed-xml-example.md)d'informations sur les activités.</span><span class="sxs-lookup"><span data-stu-id="43d25-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43d25-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43d25-130">See also</span></span>

- [<span data-ttu-id="43d25-131">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="43d25-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="43d25-132">Schéma XML du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="43d25-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="43d25-133">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="43d25-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

