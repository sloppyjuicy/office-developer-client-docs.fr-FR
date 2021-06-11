---
title: Exemple de XML de flux d’activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: L’exemple XML de cette rubrique est une chaîne XML de flux d’activités renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialSession2::GetActivitiesEx pour un réseau social.
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538325"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="02f2d-103">Exemple de XML de flux d’activités</span><span class="sxs-lookup"><span data-stu-id="02f2d-103">Activity Feed XML Example</span></span>

<span data-ttu-id="02f2d-104">L’exemple XML de cette rubrique est une chaîne XML de flux d’activités renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="02f2d-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="02f2d-105">L’exemple montre le **XML activityFeed** qui contient les quatre activités suivantes, chacune délimitée par l’élément **activityDetails** et correspondant à un modèle à des fins d’affichage :</span><span class="sxs-lookup"><span data-stu-id="02f2d-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="02f2d-106">Mise à jour de l’image de profil par Melissa Macbeth, dont **le ownerID** sur le réseau social est 4667647.</span><span class="sxs-lookup"><span data-stu-id="02f2d-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="02f2d-107">Cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable** et **pictureVariable** (qui est entouré de **listVariable**).</span><span class="sxs-lookup"><span data-stu-id="02f2d-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="02f2d-108">Ces variables spécifient la personne qui a publié l’élément de flux d’activités et les informations pour l’image à mettre à jour (à l’aide du nom **,** de la valeur **,** **altText** et des éléments enfants **href** de **pictureVariable**).</span><span class="sxs-lookup"><span data-stu-id="02f2d-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="02f2d-109">Mise à jour de l’image de profil par Michael Quéi dont **le ownerID** sur le réseau social est 5015012.</span><span class="sxs-lookup"><span data-stu-id="02f2d-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="02f2d-110">Similaire à la dernière activité, cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable** et **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="02f2d-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="02f2d-111">Ces variables spécifient la personne qui a publié l’élément de flux d’activités et les informations pour l’image à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="02f2d-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="02f2d-112">Mise à jour de l’état par Michael Titrei, montrant le **même ownerID** de 5015012 que la dernière activité.</span><span class="sxs-lookup"><span data-stu-id="02f2d-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="02f2d-113">Cette activité spécifie deux variables de modèle de type **publisherVariable** et **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="02f2d-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="02f2d-114">**publisherVariable** spécifie la personne qui a publié l’élément de flux d’activités, et **textVariable** inclut une **valeur** de la ligne d’état  `is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="02f2d-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="02f2d-115">Un billet de blog de Michael Quéi, montrant le **même ownerID** de 5015012 que les deux dernières activités.</span><span class="sxs-lookup"><span data-stu-id="02f2d-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="02f2d-116">Cette activité spécifie deux variables de modèle de type **publisherVariable** et **linkVariable**.</span><span class="sxs-lookup"><span data-stu-id="02f2d-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="02f2d-117">**publisherVariable** spécifie la personne qui a publié l’élément de flux d’activités, et  **linkVariable** inclut des informations supplémentaires (spécifiées par le **nom,** le texte et les éléments enfants de valeur de **linkVariable**) sur le billet de blog.</span><span class="sxs-lookup"><span data-stu-id="02f2d-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="02f2d-118">Chacune des quatre activités spécifie une valeur **templateID,** qui correspond à l’un des trois modèles spécifiés par **l’élément templates.**</span><span class="sxs-lookup"><span data-stu-id="02f2d-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="02f2d-119">Chaque modèle se trouve dans son propre élément **activityTemplateContainer,** identifié par une valeur **templateID** qui est également utilisée pour afficher une activité qui a la même valeur **templateID.**</span><span class="sxs-lookup"><span data-stu-id="02f2d-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="02f2d-120">Pour obtenir une description détaillée des éléments XML utilisés dans l’exemple, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="02f2d-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="02f2d-121">Vue d’ensemble du XML pour un élément de flux d’activités</span><span class="sxs-lookup"><span data-stu-id="02f2d-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="02f2d-122">activityDetails, élément</span><span class="sxs-lookup"><span data-stu-id="02f2d-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="02f2d-123">activityTemplateContainer, élément</span><span class="sxs-lookup"><span data-stu-id="02f2d-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="02f2d-124">Variables de modèle</span><span class="sxs-lookup"><span data-stu-id="02f2d-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="02f2d-125">Exemple de XML</span><span class="sxs-lookup"><span data-stu-id="02f2d-125">XML example</span></span>

<span data-ttu-id="02f2d-126">L’exemple suivant montre le code XML **activityFeed** de quatre activités : deux mises à jour d’image de profil, une mise à jour d’état et un billet de blog.</span><span class="sxs-lookup"><span data-stu-id="02f2d-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="02f2d-127">Le XML spécifie également trois modèles d’affichage d’activité pour l’affichage des activités correspondantes.</span><span class="sxs-lookup"><span data-stu-id="02f2d-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="02f2d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02f2d-128">See also</span></span>

- [<span data-ttu-id="02f2d-129">Exemples XML de fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="02f2d-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="02f2d-130">XML pour les activités</span><span class="sxs-lookup"><span data-stu-id="02f2d-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="02f2d-131">Exemple de fonctionnalités XML</span><span class="sxs-lookup"><span data-stu-id="02f2d-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="02f2d-132">Exemple XML Friends</span><span class="sxs-lookup"><span data-stu-id="02f2d-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="02f2d-133">Outlook Schéma XML du fournisseur Social Connector</span><span class="sxs-lookup"><span data-stu-id="02f2d-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

