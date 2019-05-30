---
title: Exemple de fonctionnalités XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: 'L’exemple XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialProvider:: GetCapabilities pour un réseau social. Le XML montre comment un fournisseur OSC spécifie ses capacités et ses conditions requises pour le OSC.'
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542260"
---
# <a name="capabilities-xml-example"></a>Exemple de fonctionnalités XML

L’exemple XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) pour un réseau social. Le XML montre comment un fournisseur OSC spécifie ses capacités et ses conditions requises pour le OSC. 
  
## <a name="capabilities-for-friends"></a>Fonctionnalités pour les amis

Dans cet exemple, le fournisseur OSC spécifie les éléments suivants pour afficher ses fonctionnalités dans la prise en charge de la fonctionnalité Friends:
  
- **getFriends** comme **true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir les informations des amis par programme. 
    
- **cacheFriends** comme **true** pour prendre en charge la mise en cache des informations des amis dans un dossier de contacts Outlook. 
    
- **contactSyncRestartInterval** en tant que 60 pour indiquer qu’en cas d’erreur, l’OSC doit réessayer d’actualiser le cache toutes les 60 minutes. 
    
- **followPerson** comme **true** pour indiquer la possibilité d’ajouter des amis sur le réseau social. 
    
- **doNotFollowPerson** **false** pour indiquer que le fournisseur OSC ne prend pas en charge la suppression d’une personne en tant qu’ami sur le réseau social. 
    
- **dynamicContactsLookup** **false** pour indiquer que OSC ne doit pas stocker les informations des amis dans la mémoire. 
    
## <a name="capabilities-for-activities"></a>Fonctionnalités pour les activités

Le fournisseur OSC spécifie les éléments suivants pour montrer sa capacité à prendre en charge les activités:
  
- **GetActivities** comme **true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialProfile:: GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) pour obtenir les activités de Friends par programme. 
    
- **cacheActivities** **false** pour prendre en charge la mise en cache des activités d’amis dans le dossier de flux d’actualités Outlook masqué. 
    
- **dynamicActivitiesLookupEx** comme **true** pour indiquer que le OSC doit stocker les activités de Friend dans la mémoire. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Fonctionnalités d’authentification et de configuration de compte

Le fournisseur OSC spécifie les éléments suivants pour montrer sa prise en charge de la configuration de l’authentification et des comptes:
  
- **useLogonWebAuth** **false** pour indiquer que le fournisseur OSC prend en charge l’authentification de base. 
    
- **supportsAutoConfigure** **false** pour indiquer que OSC ne doit pas tenter de configurer et d’ouvrir automatiquement une session sur le réseau social de l’utilisateur. 
    
- **useLogonCached** et **hideRememberMyPassword** **false** pour indiquer que OSC doit demander un mot de passe à chaque fois et ne doit pas utiliser les informations d’identification d’ouverture de session mises en cache pour se connecter. 
    
- **DisplayUrl** **false** pour indiquer que OSC ne doit pas afficher l’URL du réseau social dans la boîte de dialogue Configuration du compte. 
    
- **hideHyperlinks** comme **false** pour indiquer que le fournisseur OSC prend en charge uniquement les comptes existants avec des mots de passe connus et que OSC ne doit pas afficher les liens de **Cliquer ici pour créer un compte** et avoir **oublié votre mot de passe?** liens hypertexte dans le boîte de dialogue Configuration du compte. 
    
## <a name="xml-example"></a>Exemple XML

L’exemple suivant montre les **fonctionnalités** XML d’un fournisseur OSC. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Voir aussi

- [Exemples de fournisseurs XML OSC](osc-provider-xml-examples.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md)  
- [Exemple de code XML pour les amis](friends-xml-example.md)  
- [Exemple de XML d’informations sur les activités](activity-feed-xml-example.md)  
- [Schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

