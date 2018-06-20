---
title: Exemple de flux XML d’activité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: L’exemple de code XML de cette rubrique est qu'un flux d’activités chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialSession2::GetActivitiesEx pour un réseau social.
ms.openlocfilehash: ab27ddfad5044994a19bb32759994a0e98c39ae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787570"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="f3261-103">Exemple de flux XML d’activité</span><span class="sxs-lookup"><span data-stu-id="f3261-103">Activity Feed XML Example</span></span>

<span data-ttu-id="f3261-104">L’exemple de code XML de cette rubrique est une activité de flux de chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="f3261-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="f3261-105">L’exemple illustre le code XML qui contient les activités suivantes quatre **activityFeed** , chacun délimité par l’élément **activityDetails** et correspondant à un modèle pour afficher à des fins :</span><span class="sxs-lookup"><span data-stu-id="f3261-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="f3261-106">Une image de profil à jour en Melissa Macbeth, dont **ownerID** sur le réseau social est 4667647.</span><span class="sxs-lookup"><span data-stu-id="f3261-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="f3261-107">Cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable** (qui est placé dans **listVariable**).</span><span class="sxs-lookup"><span data-stu-id="f3261-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="f3261-108">Ces variables spécifient la personne ayant publié l’activité de flux de facturation et de l’image à mettre à jour (en utilisant les éléments enfants **nom**, **valeur**, **altText**et **href** de **pictureVariable**).</span><span class="sxs-lookup"><span data-stu-id="f3261-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="f3261-109">Une image de profil mettre à jour par Michael Affronti dont **ownerID** sur le réseau social est 5015012.</span><span class="sxs-lookup"><span data-stu-id="f3261-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="f3261-110">Semblable à la dernière activité, cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="f3261-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="f3261-111">Ces variables spécifient la personne ayant publié l’activité de flux d’élément et les informations de l’image à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="f3261-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="f3261-112">Une mise à jour de statut par Michael Affronti, affichant le même **ownerID** 5015012 en tant que la dernière activité.</span><span class="sxs-lookup"><span data-stu-id="f3261-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="f3261-113">Cette activité spécifie deux variables de modèle de type **publisherVariable** et **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="f3261-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="f3261-114">**publisherVariable** spécifie la personne ayant publié la flux d’élément d’activité et **textVariable** inclut une **valeur** de la ligne d’état`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="f3261-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="f3261-115">Billet de blog par Michael Affronti, affichant le même **ownerID** 5015012 en tant que les deux dernières activités.</span><span class="sxs-lookup"><span data-stu-id="f3261-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="f3261-116">Cette activité spécifie deux variables de modèle de type **publisherVariable** et **linkVariable**.</span><span class="sxs-lookup"><span data-stu-id="f3261-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="f3261-117">**publisherVariable** Spécifie l’élément de la personne ayant publié l’activité de flux et **linkVariable** comprend également des informations (spécifiées par les **nom**, le **texte**et **valeur** ses éléments enfants de **linkVariable**) sur le billet de blog.</span><span class="sxs-lookup"><span data-stu-id="f3261-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="f3261-118">Chacune des quatre activités spécifie une valeur **templateID** , qui correspond à l’un des trois modèles spécifiés par l’élément **templates** .</span><span class="sxs-lookup"><span data-stu-id="f3261-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="f3261-119">Chaque modèle est dans son propre élément **activityTemplateContainer** , identifié par une valeur **templateID** qui est également utilisée pour afficher une activité qui possède la même valeur **templateID** .</span><span class="sxs-lookup"><span data-stu-id="f3261-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="f3261-120">Pour obtenir une description détaillée des éléments XML utilisés dans l’exemple, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3261-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="f3261-121">Vue d’ensemble du code XML pour une activité de flux d’élément</span><span class="sxs-lookup"><span data-stu-id="f3261-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="f3261-122">activityDetails, élément</span><span class="sxs-lookup"><span data-stu-id="f3261-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="f3261-123">activityTemplateContainer, élément</span><span class="sxs-lookup"><span data-stu-id="f3261-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="f3261-124">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="f3261-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="f3261-125">Exemple de code XML</span><span class="sxs-lookup"><span data-stu-id="f3261-125">XML example</span></span>

<span data-ttu-id="f3261-126">L’exemple suivant montre le code XML de quatre activités **activityFeed** : deux mises à jour de l’image, une mise à jour d’état et un billet de blog de profil.</span><span class="sxs-lookup"><span data-stu-id="f3261-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="f3261-127">Le code XML spécifie également les trois modèles d’affichage d’activité pour afficher les activités correspondantes.</span><span class="sxs-lookup"><span data-stu-id="f3261-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>http://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="f3261-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3261-128">See also</span></span>

- [<span data-ttu-id="f3261-129">Exemples de code XML de fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="f3261-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="f3261-130">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="f3261-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="f3261-131">Exemple de code XML des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f3261-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="f3261-132">Exemple de code XML amis</span><span class="sxs-lookup"><span data-stu-id="f3261-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="f3261-133">Fournisseur Outlook Social Connector schéma XML</span><span class="sxs-lookup"><span data-stu-id="f3261-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

