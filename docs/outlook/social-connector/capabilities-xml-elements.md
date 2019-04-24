---
title: Éléments XML des fonctionnalités
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: Les tableaux de cette rubrique décrivent les éléments enfants du XML des fonctionnalités et sont regroupés par les domaines qu'ils prennent en charge.
ms.openlocfilehash: 6816bbdcd24eceffc47d6b9d0835a90c7089c039
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281189"
---
# <a name="capabilities-xml-elements"></a>Éléments XML des fonctionnalités

Les tableaux de cette rubrique décrivent les éléments enfants du XML des **fonctionnalités** et sont regroupés par les domaines qu'ils prennent en charge. La valeur par défaut de chaque élément **Capabilities** est **false**. Si l'élément n'est pas spécifié dans le code XML **Capabilities** renvoyé par la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) , la valeur de l'élément est **** égale à false.
  
Pour obtenir une vue d'ensemble des **fonctionnalités** XML, consultez la rubrique [XML for Capabilities](xml-for-capabilities.md). Pour obtenir un exemple de code XML de **fonctionnalités** , consultez la rubrique [Capabilities XML example](capabilities-xml-example.md). Pour obtenir une définition complète du schéma XML du fournisseur Microsoft Outlook Social Connector (OSC), y compris les éléments requis ou facultatifs, voir [schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Fonctionnalités de prise en charge des amis

Le tableau suivant présente les éléments qui s'appliquent à toute forme de synchronisation d'amis ou de non-amis.
  
|**Élément**|**Description**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Indique si le fournisseur prend en charge l'appel de méthode [ISocialSession:: UnFollowPerson](isocialsession-unfollowperson.md) .  <br/> **followPerson** et **doNotFollowPerson** sont des fonctionnalités indépendantes d'un fournisseur OSC. Un fournisseur OSC peut indiquer la possibilité d'ajouter une personne en tant qu'ami (définir **followPerson** sur **true**) ou de supprimer une personne en tant qu'ami sur un compte de réseau social (en affectant la **valeur true**à **doNotFollowPerson** ). En règle générale, la possibilité de suivre n'implique pas de ne pas pouvoir arrêter le suivi. **followPerson** est une fonctionnalité qui ne doit pas être interprétée de manière incorrecte comme une action de suivi d'une personne spécifique ou de chaque personne sur le compte de réseau social. **followPerson** la **valeur true** n'implique pas que **doNotFollowPerson** a la **valeur false**.  <br/> |
|**followPerson** <br/> |Indique si le fournisseur prend en charge l'appel de méthode [ISocialSession:: followPerson](isocialsession-followperson.md) . L'OSC vérifie **followPerson** si **cacheFriends** a la **valeur true** (synchronisation mise en cache des amis), **dynamicContactsLookup** a la **valeur true** (synchronisation à la demande des amis et des non-Friends), ou les deux **cacheFriends **et **dynamicContactsLookup** sont vrais (synchronisation hybride des amis et des non-amis). Si le fournisseur définit **followPerson** comme **true**, OSC affiche un badge réseau dans le volet de personnes pour les personnes suivies par l'utilisateur et active la **commande \<sur\> NetworkName** dans le menu **Ajouter (+)** dans le menu personnes. Arborescence. Si le fournisseur définit **followPerson** comme **false**, le badge réseau n'est pas affiché et la commande **sur \<NetworkName\> ** est masquée.  <br/> |
|**getFriends** <br/> |Indique si le fournisseur prend en charge l'appel de méthode [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) ou [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) . Si le fournisseur définit **getFriends** comme **true**, OSC utilise la valeur de **cacheFriends** ou **dynamicContactsLookup** pour déterminer si le réseau social permet de stocker des amis en tant qu'éléments de contacts Outlook ou en mémoire. Si le fournisseur définit **getFriends** comme **false**, le réseau social ne prend pas en charge les amis et les méthodes **ISocialPerson:: GetFriendsAndColleagues** et **ISOCIALSESSION2:: GetPeopleDetails** , et le OSC ignore les valeurs de **cacheFriends** et **dynamicContactsLookup**.  <br/> |
   
Les éléments suivants s'appliquent uniquement à la synchronisation mise en cache des amis ou de la synchronisation hybride des amis et des non-amis. Pour plus d'informations sur la synchronisation des amis, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
|**Élément**|**Description**|
|:-----|:-----|
|**cacheFriends** <br/> |Indique si le fournisseur OSC permet de stocker des amis en tant qu'éléments de contacts Outlook. L'OSC vérifie **cacheFriends** uniquement si **getFriends** a la **valeur true**. Si le fournisseur définit **cacheFriends** comme **true**, OSC synchronise les amis en mettant en cache et crée un dossier de contacts spécifique au réseau dans la Banque par défaut de l'utilisateur pour les contacts Friend. Le nom du dossier de contacts spécifique au réseau est la valeur de la propriété [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) . Si le fournisseur définit **cacheFriends** comme **false**, le OSC ne crée pas de dossier de contacts spécifique au réseau pour les contacts Friend afin de stocker des amis.  <br/> |
|**contactSyncRestartInterval** <br/> |Détermine l'intervalle de nouvelle tentative, en minutes, entre les tentatives de synchronisation des informations des amis à partir du réseau social, si une erreur de synchronisation se produit. Le paramètre OSC utilise cet élément uniquement si le fournisseur OSC prend en charge la synchronisation mise en cache ou la synchronisation hybride des amis vers un dossier de contacts spécifique au réseau social (**cacheFriends** a la **valeur true**).  <br/> L'intervalle de nouvelle tentative par défaut est de 30 minutes, sauf si la clé `ContactSyncRestartInterval` par défaut `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`est remplacée par la clé sous. Si le fournisseur définit **contactSyncRestartInterval**, la valeur du fournisseur remplace l'intervalle de relance par défaut de 30 minutes ou la valeur de la clé de registre.  <br/> Pour plus d'informations sur la synchronisation des amis et des informations non relatives à la demande, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).  <br/> |
   
Les éléments suivants s'appliquent uniquement à la synchronisation à la demande ou à la synchronisation hybride des amis et des non-amis.
  
|**Élément**|**Description**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Indique si le fournisseur OSC prend en charge l'appel [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) pour la synchronisation à la demande des amis et des non-amis.  <br/> L'OSC vérifie **dynamicContactsLookup** uniquement si **getFriends** a la **valeur true**. Le paramètre par défaut de **dynamicContactsLookup** est **false**.  <br/> Si le fournisseur OSC spécifie **dynamicContactsLookup** comme **true** et **getFriends** comme **true**, OSC appelle **ISocialSession2:: GetPeopleDetails** à chaque fois que le volet personnes est actualisé. Le volet personnes est actualisé lorsque l'utilisateur sélectionne un autre utilisateur dans le volet personnes ou un autre élément dans la fenêtre d'explorateur Outlook, ou ouvre une fenêtre d'inspecteur Outlook. La recherche de contacts dynamiques garantit que l'utilisateur voit toujours les dernières images utilisateur et informations de profil dans le volet personnes, mais augmente le nombre d'appels du fournisseur vers le réseau social.  <br/> Si le fournisseur définit **dynamicContactsLookup** comme **false**, le OSC n'appelle pas **ISocialSession2:: GetPeopleDetails** pour actualiser le volet personnes.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Indique si OSC doit effectuer une synchronisation à la demande pour les amis et les non-amis lorsque le volet de personnes est réduit.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Fonctionnalités de prise en charge des activités

L'élément suivant s'applique à toute forme de synchronisation des activités prises en charge par le fournisseur OSC.
  
|**Élément**|**Description**|
|:-----|:-----|
|**getActivities** <br/> |Indique si le fournisseur prend en charge les appels de méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) ou [ISocialPerson:: GetActivities](isocialperson-getactivities.md) . Si le fournisseur définit **GetActivities** comme **true**, OSC utilise la valeur de **cacheActivities** ou **dynamicActivitiesLookupEx** pour déterminer si le site réseau social autorise le stockage des activités en tant qu'éléments RSS Outlook ou en tant que activités en mémoire. Si le fournisseur définit **GetActivities** comme **false**, le réseau social ne prend pas en charge les activités et les méthodes **ISocialSession2:: GetActivitiesEx** et **ISOCIALPERSON:: GetActivities** , et le OSC ignore les valeurs de ** cacheActivities** et **dynamicActivitiesLookupEx**.  <br/> |
   
L'élément suivant s'applique uniquement à la synchronisation mise en cache ou à la synchronisation hybride des activités.
  
|**Élément**|**Description**|
|:-----|:-----|
|**cacheActivities** <br/> |À partir d'Outlook Social Connector 2013, le OSC ignore cet élément dans la mesure où les fournisseurs ne peuvent plus synchroniser les activités en les mettant en cache dans un dossier masqué dans le magasin de l'utilisateur.  <br/> Si le fournisseur prend en charge les activités, le fournisseur doit prendre en charge la synchronisation des activités à la demande. Le fournisseur définit **cacheActivities** comme **false** et définit **dynamicActivitesLookupEx** comme **true**. Le OSC synchronise les activités à la demande et met en cache les activités en mémoire. Le cache mémoire des activités est actualisé sur une période de 30 minutes.  <br/> |
   
Les éléments suivants s'appliquent uniquement à la synchronisation à la demande ou à la synchronisation hybride des activités.
  
|**Élément**|**Description**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Déconseillé dans le OSC 1,1.  <br/> À partir du OSC 1,1, le OSC n'appelle plus [ISocialSession:: GetActivities](isocialsession-getactivities.md) et ignore la valeur de **dynamicActivitiesLookup**. Pour prendre en charge la recherche des activités à la demande, définissez **cacheActivities** sur **false** et **GetActivities** et **DynamicActivitiesLookupEx** sur **true**, et OSC appelle **ISocialSession2:: GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Indique si le fournisseur OSC prend en charge l'appel **ISocialSession2:: GetActivitiesEx** pour la synchronisation à la demande des activités.  <br/> Si le fournisseur OSC prend en charge la synchronisation des activités à la demande, il définit **GetActivities** et **dynamicActivitiesLookupEx** comme **true**, et **cacheActivities** comme **false**. Le OSC appelle **ISocialSession2:: GetActivitiesEx** à chaque fois que le volet personnes est actualisé. Le volet personnes est actualisé lorsque l'utilisateur modifie l'élément sélectionné dans la fenêtre de l'explorateur Outlook ou ouvre une fenêtre d'inspecteur Outlook. La recherche des activités dynamiques garantit que l'utilisateur verra toujours les dernières activités dans le volet de personnes, mais augmentera le nombre d'appels du fournisseur vers le réseau social.  <br/> Si le fournisseur définit **dynamicActivitiesLookupEx** comme **false**, le OSC n'appelle pas **ISocialSession2:: GetActivitiesEx** pour les personnes affichées dans le volet de personnes.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Indique si OSC doit effectuer une synchronisation à la demande pour les activités lorsque le volet personnes est réduit.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Fonctionnalités communes pour la prise en charge de la synchronisation à la demande ou hybride des amis, des non-amis et des activités

|**Élément**|**Description**|
|:-----|:-----|
|**hashFunction** <br/> | Spécifie la fonction de hachage que le fournisseur OSC prend en charge. Pour protéger les informations d'identification personnelle des utilisateurs qui ne se trouvent pas sur le réseau social ou l'application métier du fournisseur, le OSC transmet des adresses de messagerie hachées à **ISocialSession2:: GetPeopleDetails** et **ISocialSession2:: GetActivitiesEx**.  <br/>  Si **dynamicContactsLookup** est défini sur **true** ou **si dynamicActivitiesLookupEx** est défini **sur true**, le fournisseur doit définir **hashFunction** sur l'une des valeurs autorisées: **SHA1**, **MD5**ou **CRC32MD5**. Si **hashFunction** est manquant ou spécifie une valeur incorrecte, OSC renvoie une erreur.  <br/> **SHA1** est Internet Engineering Task Force (IETF) US Secure Hash Algorithm 1 défini par [[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt). Par exemple, la valeur hachée **SHA1** de l'adresse de messagerie `bb81577b567262a21a4df5f6e335c1250acd7b50`melissa@contoso.com est.  <br/> **MD5** est l'algorithme MD5 de message MD5 de l'IETF (Internet Engineering Task Force) défini par [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt). Par exemple, la valeur Hashed **MD5** de l'adresse de messagerie `c8c39e61ca1662477b39b83d7b0a0615`melissa@contoso.com est.  <br/> **CRC32MD5** est une combinaison de **CRC32** et de **MD5** définie comme suit:  <br/>  Normalisez l'adresse de messagerie en supprimant les espaces de début et de fin et en convertissant tous les caractères en minuscules.  <br/>  Calculez la valeur **CRC32** pour l'adresse de messagerie normalisée et utilisez la représentation décimale entière de cette valeur. Si votre implémentation renvoie des entiers signés, vous devez convertir l'entier signé en entier non signé.  <br/>  Calculez la valeur **MD5** pour l'adresse de messagerie normalisée et utilisez la représentation hexadécimale de cette valeur (en minuscules pour A à F).  <br/>  Combine ces deux valeurs avec un trait de soulignement.  <br/>  Par exemple, la valeur hachée **CRC32MD5** de l'adresse de messagerie `2149665315_c8c39e61ca1662477b39b83d7b0a0615`melissa@contoso.com est.  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Fonctionnalités de prise en charge de l'authentification et de la configuration des comptes

|**Élément**|**Description**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Indique si le réseau social permet à l'utilisateur de modifier les paramètres de configuration automatique, comme fournir une autre URL pour se connecter.  <br/> |
|**createAccountUrl** <br/> |Si le fournisseur définit **hideHyperlinks** comme **false**, lorsque l'utilisateur clique **sur cliquer ici pour créer un compte** dans la boîte de dialogue **configuration du compte** , l'URL spécifiée par **createAccountUrl** s'ouvre dans le navigateur par défaut.  <br/> |
|**displayUrl** <br/> |Indique si OSC doit afficher la zone de texte adresse de l' **URL** pour le réseau social dans la boîte de dialogue Configuration du compte.  <br/> |
|**forgotPasswordUrl** <br/> |Si le fournisseur définit **hideHyperlinks** comme **false**, lorsque l'utilisateur clique sur **oublier votre mot de passe?** dans la boîte de dialogue **configuration du compte** , l'URL spécifiée par **forgotPasswordUrl** s'ouvre dans le navigateur par défaut.  <br/> |
|**hideHyperlinks** <br/> |Indique si OSC doit masquer les liens hypertexte **Cliquer ici pour créer un compte** et **oublié votre mot de passe?** dans la boîte de dialogue Configuration du compte.  <br/> OSC 1,0 ignore ce paramètre et les liens hypertexte sont toujours masqués. OSC 1,1 observe la valeur de ce paramètre.  <br/> |
|**hideRememberMyPassword** <br/> |Indique si OSC doit masquer la case à cocher **Mémoriser mon mot de passe** dans la boîte de dialogue Configuration du compte.  <br/> Si le fournisseur définit **hideRememberMyPassword** comme **true**, le OSC se comporte comme si la case à cocher **Mémoriser mon mot de passe** n'est pas cochée et n'enregistrera pas le mot de passe.  <br/> Si le fournisseur définit **hideRememberMyPassword** comme **false**, le OSC affichera la case à cocher **Mémoriser mon mot de passe** dans la boîte de dialogue Configuration du compte.  <br/> |
|**supportsAutoConfigure** <br/> |Indique si OSC doit appeler la fonction **GetAutoConfiguredSession** sur l'interface **ISocialProvider** pour effectuer une configuration automatique et ouvrir une session sur le réseau social de l'utilisateur.  <br/> |
|**useLogonCached** <br/> |Indique si le fournisseur OSC prend en charge l'appel [ISocialSession2:: LogonCached](isocialsession2-logoncached.md) pour se connecter avec les informations d'identification mises en cache.  <br/> Si le fournisseur définit **useLogonCached** comme **true**, OSC ignore le paramètre pour **UseLogonWebAuth** et le OSC appelle **ISocialSession2:: LogonCached** pour l'authentification.  <br/> Si le fournisseur définit **dynamicActivitiesLookupEx** comme **false**, le OSC n'appelle pas **ISocialSession2:: LogonCached** pour l'authentification.  <br/> |
|**useLogonWebAuth** <br/> |Indique si OSC doit utiliser l'authentification basée sur les formulaires et la méthode [ISocialSession:: LogonWeb](isocialsession-logonweb.md) . Si le fournisseur définit **useLogonWebAuth** comme **false**, le OSC utilise l'authentification de base et appelle la méthode [ISocialSession:: Logon](isocialsession-logon.md) . Si le fournisseur définit **useLogonWebAuth** comme **true**, OSC utilise l'authentification basée sur les formulaires et appelle **ISocialSession:: LogonWeb**.  <br/> |
   
En fonction du code XML des **fonctionnalités** renvoyé par le fournisseur dans la méthode **ISocialProvider:: GetCapabilities** , la boîte de dialogue Configuration du compte change. Par exemple, la figure 1 illustre la boîte de dialogue Configuration du compte pour un exemple de TestProvider. 
  
**Figure 1. Exemple de TestProvider dans la boîte de dialogue Configuration du compte**

![Informations de configuration d’exemple TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)

