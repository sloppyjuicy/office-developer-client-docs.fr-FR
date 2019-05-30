---
title: Exemple de XML d’informations sur les activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: 'L’exemple XML de cette rubrique est une chaîne XML d’informations sur les activités renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialSession2:: GetActivitiesEx pour un réseau social.'
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538325"
---
# <a name="activity-feed-xml-example"></a>Exemple de XML d’informations sur les activités

L’exemple XML de cette rubrique est une chaîne XML d’informations sur les activités renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) pour un réseau social. 
  
L’exemple montre le code XML **activityFeed** qui contient les quatre activités suivantes, chacune étant délimitée par l’élément **activityDetails** et correspondant à un modèle à des fins d’affichage: 
  
- Une mise à jour de l’image de profil de melissa Macbeth, dont l' **ownerID** sur le réseau social est 4667647. Cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable** (qui est incluse dans **listVariable**). Ces variables spécifient la personne qui a publié l’élément de flux d’activités, ainsi que les informations relatives à l’image à mettre à jour (à l’aide des éléments **Name**, **value**, **AltText**et **href** enfants de **pictureVariable**).
    
- Une mise à jour de l’image de profil par Michael Affronti dont l' **ownerID** sur le réseau social est 5015012. À l’instar de la dernière activité, cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable**. Ces variables spécifient la personne qui a publié l’élément de flux d’activité et les informations pour l’image à mettre à jour.
    
- Une mise à jour d’État par Michael Affronti, affichant le même **ownerID** de 5015012 comme dernière activité. Cette activité spécifie deux variables de modèle de type **publisherVariable** et **textVariable**. **publisherVariable** spécifie la personne qui a publié l’élément de flux d’activités, et **textVariable** inclut une **valeur** de la ligne d’État`is hiking on Mount Rainier this weekend!`
    
- Billet de blog publié par Michael Affronti, affichant le même **ownerID** de 5015012 que les deux dernières activités. Cette activité spécifie deux variables de modèle de type **publisherVariable** et **LinkVariable**. **publisherVariable** spécifie la personne qui a publié l’élément de flux d’activités, et **LinkVariable** inclut des informations supplémentaires (spécifiées par les éléments enfants **Name**, **Text**et **value** de **LinkVariable**) à propos du billet de blog.
    
Chacune des quatre activités spécifie une valeur **TemplateID** , qui correspond à l’un des trois modèles spécifiés par l’élément **Templates** . Chaque modèle est dans son propre élément **activityTemplateContainer** , identifié par une valeur **TemplateID** qui est également utilisée pour afficher une activité qui a la même valeur **TemplateID** . 
  
Pour obtenir une description détaillée des éléments XML utilisés dans l’exemple, consultez les rubriques suivantes: 
  
- [Vue d’ensemble du code XML pour un élément de flux d’activité](overview-of-xml-for-an-activity-feed-item.md)
    
- [Élément activityDetails](activitydetails-element.md)
    
- [Élément activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de modèle](template-variables.md)
    
## <a name="xml-example"></a>Exemple XML

L’exemple suivant montre le code XML **activityFeed** de quatre activités: les deux mises à jour des images de profil, une mise à jour de l’État et un billet de blog. Le code XML spécifie également trois modèles d’affichage d’activité pour l’affichage des activités correspondantes. 
  
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

## <a name="see-also"></a>Voir aussi

- [Exemples de fournisseurs XML OSC](osc-provider-xml-examples.md)  
- [XML pour les activités](xml-for-activities.md) 
- [Exemple de XML de fonctionnalités](capabilities-xml-example.md)  
- [Exemple de code XML pour les amis](friends-xml-example.md)
- [Schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

