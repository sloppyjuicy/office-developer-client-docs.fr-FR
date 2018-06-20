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
# <a name="activity-feed-xml-example"></a>Exemple de flux XML d’activité

L’exemple de code XML de cette rubrique est une activité de flux de chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) pour un réseau social. 
  
L’exemple illustre le code XML qui contient les activités suivantes quatre **activityFeed** , chacun délimité par l’élément **activityDetails** et correspondant à un modèle pour afficher à des fins : 
  
- Une image de profil à jour en Melissa Macbeth, dont **ownerID** sur le réseau social est 4667647. Cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable** (qui est placé dans **listVariable**). Ces variables spécifient la personne ayant publié l’activité de flux de facturation et de l’image à mettre à jour (en utilisant les éléments enfants **nom**, **valeur**, **altText**et **href** de **pictureVariable**).
    
- Une image de profil mettre à jour par Michael Affronti dont **ownerID** sur le réseau social est 5015012. Semblable à la dernière activité, cette activité spécifie trois variables de modèle de type **publisherVariable**, **listVariable**et **pictureVariable**. Ces variables spécifient la personne ayant publié l’activité de flux d’élément et les informations de l’image à mettre à jour.
    
- Une mise à jour de statut par Michael Affronti, affichant le même **ownerID** 5015012 en tant que la dernière activité. Cette activité spécifie deux variables de modèle de type **publisherVariable** et **textVariable**. **publisherVariable** spécifie la personne ayant publié la flux d’élément d’activité et **textVariable** inclut une **valeur** de la ligne d’état`is hiking on Mount Rainier this weekend!`
    
- Billet de blog par Michael Affronti, affichant le même **ownerID** 5015012 en tant que les deux dernières activités. Cette activité spécifie deux variables de modèle de type **publisherVariable** et **linkVariable**. **publisherVariable** Spécifie l’élément de la personne ayant publié l’activité de flux et **linkVariable** comprend également des informations (spécifiées par les **nom**, le **texte**et **valeur** ses éléments enfants de **linkVariable**) sur le billet de blog.
    
Chacune des quatre activités spécifie une valeur **templateID** , qui correspond à l’un des trois modèles spécifiés par l’élément **templates** . Chaque modèle est dans son propre élément **activityTemplateContainer** , identifié par une valeur **templateID** qui est également utilisée pour afficher une activité qui possède la même valeur **templateID** . 
  
Pour obtenir une description détaillée des éléments XML utilisés dans l’exemple, consultez les rubriques suivantes : 
  
- [Vue d’ensemble du code XML pour une activité de flux d’élément](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails, élément](activitydetails-element.md)
    
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)
    
- [Variables de modèle](template-variables.md)
    
## <a name="xml-example"></a>Exemple de code XML

L’exemple suivant montre le code XML de quatre activités **activityFeed** : deux mises à jour de l’image, une mise à jour d’état et un billet de blog de profil. Le code XML spécifie également les trois modèles d’affichage d’activité pour afficher les activités correspondantes. 
  
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

## <a name="see-also"></a>Voir aussi

- [Exemples de code XML de fournisseur OSC](osc-provider-xml-examples.md)  
- [XML pour les activités](xml-for-activities.md) 
- [Exemple de code XML des fonctionnalités](capabilities-xml-example.md)  
- [Exemple de code XML amis](friends-xml-example.md)
- [Fournisseur Outlook Social Connector schéma XML](outlook-social-connector-provider-xml-schema.md)

