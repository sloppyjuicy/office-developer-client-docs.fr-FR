---
title: Exemple de code XML des fonctionnalités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: L’exemple de code XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialProvider::GetCapabilities pour un réseau social. Le code XML montre comment un fournisseur OSC spécifie ses fonctionnalités et la configuration requise pour l’OSC.
ms.openlocfilehash: 5cafd6d29de8b4357e9e0ce6dab30b125f53b8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787581"
---
# <a name="capabilities-xml-example"></a>Exemple de code XML des fonctionnalités

L’exemple de code XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour un réseau social. Le code XML montre comment un fournisseur OSC spécifie ses fonctionnalités et la configuration requise pour l’OSC. 
  
## <a name="capabilities-for-friends"></a>Fonctionnalités d’amis

Dans cet exemple, le fournisseur OSC spécifie les éléments suivants pour afficher ses fonctionnalités de prise en charge de la fonctionnalité d’amis :
  
- **getFriends** en tant que **la valeur true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir des informations de vos amis par programme. 
    
- **cacheFriends** en tant que **la valeur true** pour prendre en charge les informations de mise en cache amis dans un dossier de contacts Outlook. 
    
- **contactSyncRestartInterval** 60 pour indiquer que sur erreur, l’OSC doit recommencer l’actualisation du cache toutes les 60 minutes. 
    
- **followPerson** en tant que **la valeur true** pour indiquer la possibilité d’ajouter des amis sur le réseaux sociaux. 
    
- **doNotFollowPerson** en tant que **valeur false** pour indiquer que le fournisseur OSC ne gère pas la suppression d’une personne comme un ami sur le réseaux sociaux. 
    
- **dynamicContactsLookup** en tant que **valeur false** pour indiquer que l’OSC ne devez pas stocker les informations de vos amis en mémoire. 
    
## <a name="capabilities-for-activities"></a>Fonctionnalités pour les activités

Le fournisseur OSC spécifie les éléments pour afficher sa capacité à prendre en charge les activités suivantes :
  
- **getActivities** en tant que **la valeur true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) pour obtenir par programme des activités de vos amis. 
    
- **cacheActivities** en tant que **valeur false** pour prendre en charge les activités de mise en cache des amis dans le dossier Outlook de News masqué. 
    
- **dynamicActivitiesLookupEx** en tant que **la valeur true** pour indiquer que l’OSC doit stocker les activités amis en mémoire. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Fonctionnalités de configuration de compte et d’authentification

Le fournisseur OSC spécifie les éléments suivants pour afficher la prise en charge pour l’authentification et la configuration de compte :
  
- **useLogonWebAuth** en tant que **valeur false** pour indiquer que le fournisseur OSC prend en charge l’authentification de base. 
    
- **supportsAutoConfigure** en tant que **valeur false** pour indiquer que l’OSC ne doit pas essayer configurer automatiquement et ouvrez une session sur le réseau social pour l’utilisateur. 
    
- **useLogonCached** et **hideRememberMyPassword** en tant que **valeur false** pour indiquer que l’OSC doit demander le mot de passe chaque fois et ne doit pas utiliser mis en cache les informations d’identification d’ouverture de session pour vous connecter. 
    
- **displayUrl** en tant que **valeur false** pour indiquer que l’OSC ne doit pas afficher l’URL pour le réseau social dans la boîte de dialogue de configuration de compte. 
    
- **hideHyperlinks** en tant que **valeur false** pour indiquer que le fournisseur OSC prend en charge uniquement des comptes existants par mot de passe connus et le OSC ne doit pas afficher la **Cliquez ici pour créer un compte** et **vous avez oublié votre mot de passe ?** des liens hypertexte dans le boîte de dialogue de configuration de compte. 
    
## <a name="xml-example"></a>Exemple de code XML

L’exemple suivant montre le XML des **fonctionnalités** d’un fournisseur OSC. 
  
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
  <createAccountUrl>http://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>http://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Voir aussi

- [Exemples de code XML de fournisseur OSC](osc-provider-xml-examples.md)  
- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)  
- [Exemple de code XML amis](friends-xml-example.md)  
- [Exemple de flux XML d’activité](activity-feed-xml-example.md)  
- [Fournisseur Outlook Social Connector schéma XML](outlook-social-connector-provider-xml-schema.md)

