---
title: Exemple de XML d'informations sur les activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: "L'exemple XML de cette rubrique est une chaîne XML d'informations sur les activités renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialSession2:: GetActivitiesEx pour un réseau social."
ms.openlocfilehash: 6370b559c5160bfa48d32afa77715e9a7c126aab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281331"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="a7cd8-103">Exemple de XML d'informations sur les activités</span><span class="sxs-lookup"><span data-stu-id="a7cd8-103">Activity Feed XML Example</span></span>

<span data-ttu-id="a7cd8-104">L'exemple XML de cette rubrique est une chaîne XML d'informations sur les activités renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="a7cd8-105">L'exemple montre le code XML **activityFeed** qui contient les quatre activités suivantes, chacune étant délimitée par l'élément **activityDetails** et correspondant à un modèle à des fins d'affichage:</span><span class="sxs-lookup"><span data-stu-id="a7cd8-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="a7cd8-106">Une mise à jour de l'image de profil de melissa Macbeth, dont l' **ownerID** sur le réseau social est 4667647.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="a7cd8-107">Cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable** (qui est incluse dans **listVariable**).</span><span class="sxs-lookup"><span data-stu-id="a7cd8-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="a7cd8-108">Ces variables spécifient la personne qui a publié l'élément de flux d'activités, ainsi que les informations relatives à l'image à mettre à jour (à l'aide des éléments **Name**, **value**, **AltText**et **href** enfants de **pictureVariable**).</span><span class="sxs-lookup"><span data-stu-id="a7cd8-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="a7cd8-109">Une mise à jour de l'image de profil par Michael Affronti dont l' **ownerID** sur le réseau social est 5015012.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="a7cd8-110">À l'inStar de la dernière activité, cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="a7cd8-111">Ces variables spécifient la personne qui a publié l'élément de flux d'activité et les informations pour l'image à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="a7cd8-112">Une mise à jour d'État par Michael Affronti, affichant le même **ownerID** de 5015012 comme dernière activité.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="a7cd8-113">Cette activité spécifie deux variables de modèle de type **publisherVariable** et **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="a7cd8-114">**publisherVariable** spécifie la personne qui a publié l'élément de flux d'activités, et **textVariable** inclut une **valeur** de la ligne d'État`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="a7cd8-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="a7cd8-115">Billet de blog publié par Michael Affronti, affichant le même **ownerID** de 5015012 que les deux dernières activités.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="a7cd8-116">Cette activité spécifie deux variables de modèle de type **publisherVariable** et **LinkVariable**.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="a7cd8-117">**publisherVariable** spécifie la personne qui a publié l'élément de flux d'activités, et **LinkVariable** inclut des informations supplémentaires (spécifiées par les éléments enfants **Name**, **Text**et **value** de **LinkVariable**) à propos du billet de blog.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="a7cd8-118">Chacune des quatre activités spécifie une valeur **TemplateID** , qui correspond à l'un des trois modèles spécifiés par l'élément **Templates** .</span><span class="sxs-lookup"><span data-stu-id="a7cd8-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="a7cd8-119">Chaque modèle est dans son propre élément **activityTemplateContainer** , identifié par une valeur **TemplateID** qui est également utilisée pour afficher une activité qui a la même valeur **TemplateID** .</span><span class="sxs-lookup"><span data-stu-id="a7cd8-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="a7cd8-120">Pour obtenir une description détaillée des éléments XML utilisés dans l'exemple, consultez les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="a7cd8-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="a7cd8-121">Vue d'ensemble du code XML pour un élément de flux d'activité</span><span class="sxs-lookup"><span data-stu-id="a7cd8-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="a7cd8-122">Élément activityDetails</span><span class="sxs-lookup"><span data-stu-id="a7cd8-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="a7cd8-123">Élément activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="a7cd8-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="a7cd8-124">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="a7cd8-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="a7cd8-125">Exemple XML</span><span class="sxs-lookup"><span data-stu-id="a7cd8-125">XML example</span></span>

<span data-ttu-id="a7cd8-126">L'exemple suivant montre le code XML **activityFeed** de quatre activités: les deux mises à jour des images de profil, une mise à jour de l'État et un billet de blog.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="a7cd8-127">Le code XML spécifie également trois modèles d'affichage d'activité pour l'affichage des activités correspondantes.</span><span class="sxs-lookup"><span data-stu-id="a7cd8-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
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
          <profileUrl>https://www.contoso.com</profileUrl>
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>https://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
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
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="a7cd8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7cd8-128">See also</span></span>

- [<span data-ttu-id="a7cd8-129">Exemples de fournisseurs XML OSC</span><span class="sxs-lookup"><span data-stu-id="a7cd8-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="a7cd8-130">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="a7cd8-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="a7cd8-131">Exemple de XML de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a7cd8-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="a7cd8-132">Exemple de code XML pour les amis</span><span class="sxs-lookup"><span data-stu-id="a7cd8-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="a7cd8-133">Schéma XML du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="a7cd8-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

