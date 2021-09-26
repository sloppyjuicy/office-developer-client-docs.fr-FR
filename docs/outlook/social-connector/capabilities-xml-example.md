---
title: Exemple de fonctionnalités XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: L’exemple XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialProvider::GetCapabilities pour un réseau social. Le XML montre comment un fournisseur OSC spécifie ses fonctionnalités et ses exigences pour OSC.
ms.openlocfilehash: 7ab0e08739e77964fcea4874e2422d12c65d753a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608913"
---
# <a name="capabilities-xml-example"></a>Exemple de fonctionnalités XML

L’exemple XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour un réseau social. Le XML montre comment un fournisseur OSC spécifie ses fonctionnalités et ses exigences pour OSC. 
  
## <a name="capabilities-for-friends"></a>Fonctionnalités pour les amis

Dans cet exemple, le fournisseur OSC spécifie les éléments suivants pour afficher ses fonctionnalités de prise en charge de la fonctionnalité amis :
  
- **getFriends comme** **true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir les informations des amis par programme. 
    
- **CacheFriends comme** **true pour** prendre en charge la mise en cache des informations des amis dans un Outlook contacts. 
    
- **contactSyncRestartInterval** comme 60 pour indiquer qu’en cas d’erreur, l’OSC doit réessayer d’actualisation du cache toutes les 60 minutes. 
    
- **suivezPerson comme** **true** pour indiquer la possibilité d’ajouter des amis sur le réseau social. 
    
- **doNotFollowPerson** comme **false** pour indiquer que le fournisseur OSC ne prend pas en charge la suppression d’une personne en tant qu’ami sur le réseau social. 
    
- **dynamicContactsLookup** comme **false** pour indiquer que l’OSC ne doit pas stocker les informations des amis en mémoire. 
    
## <a name="capabilities-for-activities"></a>Fonctionnalités pour les activités

Le fournisseur OSC spécifie les éléments suivants pour afficher sa capacité à prendre en charge les activités :
  
- **getActivities** comme **true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) pour obtenir les activités des amis par programme. 
    
- **CacheActivities comme** **false pour prendre** en charge les activités de mise en cache d’amis dans le dossier masqué Outlook News Feed. 
    
- **dynamicActivitiesLookupEx** comme **true** pour indiquer que l’OSC doit stocker les activités des amis en mémoire. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Fonctionnalités d’authentification et de configuration de compte

Le fournisseur OSC spécifie les éléments suivants pour afficher sa prise en charge de l’authentification et de la configuration de compte :
  
- **utilisezLogonWebAuth comme** **faux pour** indiquer que le fournisseur OSC prend en charge l’authentification de base. 
    
- **supportsAutoConfigure** comme **false** pour indiquer que l’OSC ne doit pas tenter de configurer et de se connecter automatiquement au réseau social de l’utilisateur. 
    
- **utilisezLogonCached** et **hideRememberMyPassword** comme **false** pour indiquer que l’OSC doit à chaque fois indiquer le mot de passe et ne doit pas utiliser les informations d’identification de connexion mises en cache pour se connecter. 
    
- **displayUrl comme** **false** pour indiquer que l’OSC ne doit pas afficher l’URL du réseau social dans la boîte de dialogue configuration du compte. 
    
- **hideHyperlinks**  comme false pour indiquer que le fournisseur OSC prend en charge uniquement les comptes existants avec des mots de passe connus et que l’OSC ne doit pas afficher les liens hypertexte Click **here pour** créer un compte et **Vous** avez oublié votre mot de passe ? dans la boîte de dialogue configuration du compte. 
    
## <a name="xml-example"></a>Exemple de XML

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

- [Exemples XML de fournisseur OSC](osc-provider-xml-examples.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md)  
- [Exemple XML Friends](friends-xml-example.md)  
- [Exemple de XML de flux d’activités](activity-feed-xml-example.md)  
- [Outlook Schéma XML du fournisseur Social Connector](outlook-social-connector-provider-xml-schema.md)

