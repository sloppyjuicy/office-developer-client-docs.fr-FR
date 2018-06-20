---
title: Vue d’ensemble du code XML pour une activité de flux d’élément
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Un flux d’activité se compose d’une ou plusieurs activités qui ont lieu sur un réseau social. Chaque flux d’activité est représenté par un élément activityFeed et se caractérise par ces trois éléments d’information :'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787718"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="bbae9-104">Vue d’ensemble du code XML pour une activité de flux d’élément</span><span class="sxs-lookup"><span data-stu-id="bbae9-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="bbae9-105">Un flux d’activité se compose d’une ou plusieurs activités qui ont lieu sur un réseau social.</span><span class="sxs-lookup"><span data-stu-id="bbae9-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="bbae9-106">Chaque flux d’activité est représenté par un élément **activityFeed** et se caractérise par ces trois éléments d’information :</span><span class="sxs-lookup"><span data-stu-id="bbae9-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="bbae9-107">**réseau**: nom du réseau social à partir de laquelle les activités à l’origine.</span><span class="sxs-lookup"><span data-stu-id="bbae9-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="bbae9-108">**activités**: conteneur pour les activités qui se passe sur le compte de l’utilisateur ayant ouvert une session sur ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="bbae9-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="bbae9-109">**modèles**: conteneur pour les modèles utilisés pour afficher les **activités**de l’élément d’activité correspondant.</span><span class="sxs-lookup"><span data-stu-id="bbae9-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="bbae9-110">Pour créer un élément de flux d’activités, vous devez vous conformer au schéma XML de l’extensibilité de fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="bbae9-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="bbae9-111">La figure 1 montre la que structure XML de l’activité de flux.</span><span class="sxs-lookup"><span data-stu-id="bbae9-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="bbae9-112">**La figure 1. Structure XML des informations sur les activités**</span><span class="sxs-lookup"><span data-stu-id="bbae9-112">**Figure 1. Activity feed XML structure**</span></span>

![Structure XML d’activité](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="bbae9-114">Pour chaque activité de flux d’élément, les deux composants principaux de ce schéma sont les éléments **activityDetails** et **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="bbae9-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="bbae9-115">L’élément **activityDetails** stocke des informations spécifiques pour chaque activité de flux d’élément, par exemple le nom du propriétaire de l’activité ou l’URL pour les images téléchargées.</span><span class="sxs-lookup"><span data-stu-id="bbae9-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="bbae9-116">L’élément **activityTemplateContainer** stocke le format ou élément de mise en page pour chaque activité de flux.</span><span class="sxs-lookup"><span data-stu-id="bbae9-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="bbae9-117">Il se compose de modèles, représentées par des éléments individuels **activityTemplate** , qui peuvent être réutilisées pour plusieurs éléments de flux.</span><span class="sxs-lookup"><span data-stu-id="bbae9-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="bbae9-118">Pour une activité individuelle flux d’élément, l’élément **activityTemplate** spécifie les quatre éléments d’information suivants :</span><span class="sxs-lookup"><span data-stu-id="bbae9-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="bbae9-119">**icône**— Spécifie l’URL de l’icône à afficher l’activité de flux d’élément.</span><span class="sxs-lookup"><span data-stu-id="bbae9-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="bbae9-120">**titre**: décrit l’activité de flux item.</span><span class="sxs-lookup"><span data-stu-id="bbae9-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="bbae9-121">**type**: Spécifie le type d’activité, comme un état, photo ou la mise à jour du document.</span><span class="sxs-lookup"><span data-stu-id="bbae9-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="bbae9-122">**données**— spécifie des informations supplémentaires avec un élément de flux d’activités.</span><span class="sxs-lookup"><span data-stu-id="bbae9-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="bbae9-123">L’icône affichée dans la flux d’activités est toujours le même que l’icône de fournisseur renvoyée par la propriété **ISocialProvider::SocialNetworkIcon** .</span><span class="sxs-lookup"><span data-stu-id="bbae9-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="bbae9-124">Consultez les rubriques suivantes pour plus d’informations sur l’élément **activityDetails** , l’élément **activityTemplateContainer** , jetons de modèle et variables de modèle :</span><span class="sxs-lookup"><span data-stu-id="bbae9-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="bbae9-125">activityDetails, élément</span><span class="sxs-lookup"><span data-stu-id="bbae9-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="bbae9-126">activityTemplateContainer, élément</span><span class="sxs-lookup"><span data-stu-id="bbae9-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="bbae9-127">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="bbae9-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="bbae9-128">Conseils pour l’affichage correctement les activités</span><span class="sxs-lookup"><span data-stu-id="bbae9-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="bbae9-129">Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="bbae9-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbae9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbae9-130">See also</span></span>

- [<span data-ttu-id="bbae9-131">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="bbae9-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="bbae9-132">Fournisseur Outlook Social Connector schéma XML</span><span class="sxs-lookup"><span data-stu-id="bbae9-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="bbae9-133">Développement d'un fournisseur avec le schéma XML OSC</span><span class="sxs-lookup"><span data-stu-id="bbae9-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

