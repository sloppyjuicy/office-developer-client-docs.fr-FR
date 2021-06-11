---
title: Exemple de code XML sur les amis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: L’exemple XML de cette rubrique est une chaîne XML d’ami renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialPerson::GetFriendsAndColleagues. L’exemple montre le XML des amis pour deux amis, chacun délimité par l’élément person. Chaque ami spécifie une valeur unique pour l’élément userID sur le réseau social.
ms.openlocfilehash: 593019ec4dcd1b9b578bfe275fb8e6664bbd11a9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542225"
---
# <a name="friends-xml-example"></a>Exemple de code XML sur les amis

L’exemple XML de cette rubrique est une chaîne XML d’ami renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialPerson::GetFriendsAndColleagues.](isocialperson-getfriendsandcolleagues.md) L’exemple montre le XML **des** amis pour deux amis, chacun délimité par l’élément **person.** Chaque ami spécifie une valeur unique pour **l’élément userID** sur le réseau social. 
  
Les autres éléments du XML **amis** ont des noms explicites. Pour obtenir une description détaillée de ces éléments, voir [XML for Friends](xml-for-friends.md). 
  
## <a name="xml-example"></a>Exemple de XML

L’exemple suivant montre le XML **des** amis de deux personnes sur le réseau social. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a>Voir aussi

- [Exemples XML de fournisseur OSC](osc-provider-xml-examples.md)  
- [Exemple de fonctionnalités XML](capabilities-xml-example.md) 
- [Exemple de XML de flux d’activités](activity-feed-xml-example.md) 
- [Outlook Schéma XML du fournisseur Social Connector](outlook-social-connector-provider-xml-schema.md)

