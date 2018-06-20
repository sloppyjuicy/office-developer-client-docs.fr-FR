---
title: Éléments de fonctionnalités XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: Les tableaux de cette rubrique décrivent les éléments enfants de fonctionnalités XML et sont regroupées par les zones qu’ils prennent en charge.
ms.openlocfilehash: 53bce69bbe22f6e950302a92b0ada21ed0f5a1f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787574"
---
# <a name="capabilities-xml-elements"></a>Éléments de fonctionnalités XML

Les tableaux de cette rubrique décrivent les éléments enfants de **fonctionnalités** XML et sont regroupées par les zones qu’ils prennent en charge. La valeur par défaut de chaque élément **capabilities** a la **valeur false**. Si l’élément n’est pas spécifié dans les **fonctionnalités** XML renvoyé par la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , la valeur de l’élément est égale à **false**.
  
Pour une description de la vue d’ensemble des **fonctionnalités** XML, voir [XML des capacités](xml-for-capabilities.md). Pour obtenir un exemple de **fonctionnalités** XML, voir [Exemple de code XML des capacités](capabilities-xml-example.md). Pour une définition complète du schéma XML de fournisseur de Microsoft Outlook Social Connector (OSC), y compris les éléments qui sont obligatoires ou facultatives, voir [Schéma du XML fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Fonctionnalités de prise en charge des amis

Le tableau suivant présente les éléments qui s’appliquent à n’importe quel formulaire de synchronisation des amis ou non amis.
  
|**Élément**|**Description**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Indique si le fournisseur prend en charge l’appel de méthode [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md) .  <br/> **followPerson** et **doNotFollowPerson** sont indépendants d’un fournisseur OSC. Un fournisseur OSC peut indiquer la capacité de la possibilité d’ajouter une personne comme un ami (paramètre **followPerson** sur **true**) ou de pouvoir supprimer une personne comme un ami sur un compte de réseau social (paramètre **doNotFollowPerson** sur **true**). En règle générale, la pouvoir suivre n’implique pas la possibilité d’arrêter le suivi. **followPerson** est une fonctionnalité, et il ne doit ne pas être confondu sous forme d’action à suivre d’une personne spécifique ou toute personne sur le compte de réseau social. **followPerson** est **true** n’implique pas **doNotFollowPerson** a la **valeur false**.  <br/> |
|**followPerson** <br/> |Indique si le fournisseur prend en charge l’appel de méthode [ISocialSession::FollowPerson](isocialsession-followperson.md) . L’OSC vérifie **followPerson** si **cacheFriends** est **true** (synchronisation mis en cache d’amis), **dynamicContactsLookup** est **true** (à la demande de synchronisation de vos amis et non amis), ou les deux cacheFriends ** **et **dynamicContactsLookup** sont remplies (synchronisation hybride des amis et non amis). Si le fournisseur définit **followPerson** comme **true**, l’OSC affiche une étiquette de réseau dans le volet personnes pour les personnes que l’utilisateur est le suivant et permet la **sur \<NetworkName\> ** commande dans le menu **Ajouter (+)** dans les personnes Volet Office. Si le fournisseur définit **followPerson** comme **valeur false**, le logo de réseau n’est pas affiché et le **sur \<NetworkName\> ** commande est masquée.  <br/> |
|**getFriends** <br/> |Indique si le fournisseur prend en charge l’appel de méthode [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) ou [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . Si le fournisseur définit **getFriends** comme **true**, l’OSC utilise la valeur de **cacheFriends** ou **dynamicContactsLookup** pour déterminer si le réseau social autorise le stockage des amis en tant qu’éléments de contact Outlook ou dans la mémoire. Si le fournisseur définit **getFriends** comme **valeur false**, le réseaux sociaux ne prend pas en charge amis et **ISocialPerson::GetFriendsAndColleagues** et méthodes **ISocialSession2::GetPeopleDetails** et l’OSC ignore les valeurs de **cacheFriends** et **dynamicContactsLookup**.  <br/> |
   
Les éléments suivants s’appliquent uniquement aux synchronisation mise en cache d’amis ou de synchronisation hybride des amis et non amis. Pour plus d’informations sur la synchronisation des amis, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).
  
|**Élément**|**Description**|
|:-----|:-----|
|**cacheFriends** <br/> |Indique si le fournisseur OSC permet de stocker des amis sous forme d’éléments de contact Outlook. L’OSC vérifie **cacheFriends** uniquement si **getFriends** a la **valeur true**. Si le fournisseur définit **cacheFriends** comme **true**, l’OSC synchronise amis en mettant en cache et crée un dossier de contacts spécifiques au réseau dans la banque par défaut de l’utilisateur pour les contacts ami. Le nom du dossier contacts spécifiques du réseau est la valeur de la propriété [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . Si le fournisseur définit **cacheFriends** comme **false**, l’OSC ne crée pas d’un dossier contacts spécifiques du réseau pour les contacts ami stocker des amis.  <br/> |
|**contactSyncRestartInterval** <br/> |Détermine l’intervalle entre tentatives, en minutes, entre les tentatives de synchroniser les informations de vos amis à partir du réseau social, si cet événement se produit une erreur de synchronisation. L’OSC utilise cet élément uniquement si le fournisseur OSC prend en charge la synchronisation mis en cache ou dossier contacts de synchronisation hybride d’amis à un réseau social-spécifique (**cacheFriends** a la **valeur true**).  <br/> L’intervalle entre tentatives par défaut est 30 minutes, sauf si la valeur par défaut est remplacé par le `ContactSyncRestartInterval` clé sous `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`. Si le fournisseur définit **contactSyncRestartInterval**, la valeur de fournisseur remplace l’intervalle de nouvelle tentative par défaut de 30 minutes ou la valeur de clé de Registre.  <br/> Pour plus d’informations sur la synchronisation des amis et non amis d’informations sur la demande, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).  <br/> |
   
Les éléments suivants s’appliquent à la synchronisation de la demande ou de synchronisation hybride des amis et non amis.
  
|**Élément**|**Description**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Indique si le fournisseur OSC prend en charge l’appel de [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) pour la synchronisation de la demande de vos amis et non amis.  <br/> L’OSC vérifie **dynamicContactsLookup** uniquement si **getFriends** a la **valeur true**. Le paramètre par défaut pour **dynamicContactsLookup** a la **valeur false**.  <br/> Si le fournisseur OSC spécifie **dynamicContactsLookup** comme **true** et **getFriends** **a la valeur True**, l’OSC appelle **ISocialSession2::GetPeopleDetails** chaque fois que le volet personnes est actualisé. Le volet personnes est actualisé lorsque l’utilisateur sélectionne un autre utilisateur dans le volet personnes ou un autre élément dans la fenêtre d’Explorateur Outlook ou ouvre une fenêtre d’inspecteur Outlook. Recherche de contacts dynamique garantit que l’utilisateur toujours voit les dernières photos d’utilisateur et les informations de profil dans le volet personnes, mais augmente le nombre d’appels à partir du fournisseur de réseau social.  <br/> Si le fournisseur définit **dynamicContactsLookup** comme **false**, l’OSC n’appelle pas **ISocialSession2::GetPeopleDetails** pour actualiser le volet personnes.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Indique si l’OSC doit effectuer la synchronisation de la demande d’amis ou non amis lorsque le volet personnes est réduit.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Fonctionnalités de prise en charge des activités

L’élément suivant s’applique à n’importe quel formulaire de synchronisation des activités prises en charge par le fournisseur OSC.
  
|**Élément**|**Description**|
|:-----|:-----|
|**getActivities** <br/> |Indique si le fournisseur prend en charge les appels de méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) ou [ISocialPerson::GetActivities](isocialperson-getactivities.md) . Si le fournisseur définit **getActivities** comme **true**, l’OSC utilise la valeur de **cacheActivities** ou **dynamicActivitiesLookupEx** pour déterminer si le site de réseau social autorise le stockage des activités en tant qu’éléments RSS Outlook ou en tant que activités en mémoire. Si le fournisseur définit **getActivities** comme **valeur false**, le réseaux sociaux ne prend pas en charge activités et **ISocialSession2::GetActivitiesEx** et méthodes **ISocialPerson::GetActivities** et l’OSC ignore les valeurs de ** cacheActivities** et **dynamicActivitiesLookupEx**.  <br/> |
   
L’élément suivant s’applique à la synchronisation mis en cache ou de synchronisation hybride des activités.
  
|**Élément**|**Description**|
|:-----|:-----|
|**cacheActivities** <br/> |Démarrage d’Outlook Social Connector 2013, l’OSC ignore cet élément, dans la mesure où les fournisseurs peuvent ne plus synchroniser des activités en la mise en cache dans un dossier masqué dans le magasin de l’utilisateur.  <br/> Si le fournisseur prend en charge les activités, le fournisseur doivent prendre en charge synchroniser les activités à la demande. Le fournisseur définit **cacheActivities** comme **false** et **dynamicActivitesLookupEx** **a la valeur True**. L’OSC synchronise les activités à la demande et met en cache des activités en mémoire. La mémoire cache les activités est actualisé dans un intervalle de 30 minutes.  <br/> |
   
Les éléments suivants s’appliquent à la synchronisation de la demande ou de synchronisation hybride des activités.
  
|**Élément**|**Description**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Obsolète dans OSC 1.1.  <br/> À compter d’OSC 1.1, n’est plus l’OSC appelle [ISocialSession::GetActivities](isocialsession-getactivities.md) et ignore la valeur de **dynamicActivitiesLookup**. Pour prendre en charge de la recherche des activités à la demande, définissez **cacheActivities** comme **false** et **getActivities** et **dynamicActivitiesLookupEx** **a la valeur True**et la OSC appellera **ISocialSession2::GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Indique si le fournisseur OSC prend en charge l’appel de **ISocialSession2::GetActivitiesEx** pour la synchronisation de la demande d’activités.  <br/> Si le fournisseur OSC prend en charge la synchronisation des activités à la demande, elle définit **getActivities** et **dynamicActivitiesLookupEx** comme **true**et **cacheActivities** en tant que **valeur false**. L’OSC appelle **ISocialSession2::GetActivitiesEx** chaque fois que le volet personnes est actualisé. Le volet personnes est actualisé lorsque l’utilisateur modifie l’élément sélectionné dans la fenêtre d’Explorateur Outlook ou ouvre une fenêtre d’inspecteur Outlook. Choix des activités dynamique garantit que l’utilisateur s’affiche toujours les activités le plus récent dans le volet personnes, mais vous augmentez le nombre d’appels à partir du fournisseur de réseau social.  <br/> Si le fournisseur définit **dynamicActivitiesLookupEx** comme **false**, l’OSC n’appelle pas **ISocialSession2::GetActivitiesEx** pour les personnes affichées dans le volet personnes.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Indique si l’OSC doit effectuer la synchronisation à la demande pour les activités lorsque le volet personnes est réduit.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Fonctionnalités communes de prise en charge de la synchronisation à la demande ou hybride de vos amis, non amis et activités

|**Élément**|**Description**|
|:-----|:-----|
|**hashFunction** <br/> | Spécifie la fonction de hachage qui prend en charge par le fournisseur OSC. Pour protéger les informations d’identification personnelle des utilisateurs qui ne figurent pas dans du fournisseur réseau social ou line-of-business application, l’OSC transmet les adresses de messagerie de hachage à **ISocialSession2::GetPeopleDetails** et **ISocialSession2 :: GetActivitiesEx**.  <br/>  Si **dynamicContactsLookup** est défini sur **true** ou **dynamicActivitiesLookupEx** est définie sur **true**, le fournisseur doit définir **hashFunction** à une des valeurs autorisées : **SHA1**, **MD5**ou **CRC32MD5**. Si **hashFunction** est manquante ou spécifie une valeur incorrecte, l’OSC renvoie une erreur.  <br/> **SHA1** est un algorithme de hachage sécurisé Task Force IETF (Internet Engineering) US 1 définis par [[RFC3174]](http://www.rfc-editor.org/rfc/rfc3174.txt). Par exemple, la valeur de **SHA1** haché de messagerie adresse melissa@contoso.com est `bb81577b567262a21a4df5f6e335c1250acd7b50`.  <br/> **MD5** est un algorithme de Message condensé MD5 Internet Engineering Task Force (IETF) définie par [[RFC1321]](http://www.rfc-editor.org/rfc/rfc1321.txt). Par exemple, la valeur de **MD5** haché de messagerie adresse melissa@contoso.com est `c8c39e61ca1662477b39b83d7b0a0615`.  <br/> **CRC32MD5** est une combinaison de **CRC32** et **MD5** définie comme suit :  <br/>  Normaliser l’adresse de messagerie en supprimant les et espaces de fin et convertir tous les caractères en minuscules.  <br/>  Calculer la valeur **CRC32** pour l’adresse de messagerie normalisé et utilisez la représentation sous forme de nombre entier décimal de cette valeur. Si votre implémentation renvoie entiers signés, vous devez convertir l’entier signé en entier non signé.  <br/>  Calculer la valeur **MD5** pour l’adresse de messagerie normalisé et utiliser la représentation hexadécimale de cette valeur (à l’aide de minuscules de A à F).  <br/>  Combiner ces deux valeurs avec un trait de soulignement.  <br/>  Par exemple, la valeur de **CRC32MD5** haché de messagerie adresse melissa@contoso.com est `2149665315_c8c39e61ca1662477b39b83d7b0a0615`.  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Fonctionnalités de prise en charge de l’authentification et la configuration de compte

|**Élément**|**Description**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Indique si le réseaux sociaux autorise l’utilisateur à modifier les paramètres de configuration automatique, tels que la fourniture d’une autre URL pour se connecter.  <br/> |
|**createAccountUrl** <br/> |Si le fournisseur définit **hideHyperlinks** comme **false**, lorsque l’utilisateur clique sur **Cliquez ici pour créer un compte** dans la boîte de dialogue **configuration du compte** , l’URL spécifiée par **createAccountUrl** s’ouvre dans le navigateur par défaut.  <br/> |
|**displayUrl** <br/> |Indique si l’OSC doit afficher la zone de texte **Adresse de l’URL** pour le réseau social dans la boîte de dialogue de configuration de compte.  <br/> |
|**forgotPasswordUrl** <br/> |Si le fournisseur définit **hideHyperlinks** comme **false**, lorsque l’utilisateur clique sur **vous avez oublié votre mot de passe ?** dans la boîte de dialogue **configuration du compte** , l’URL spécifiée par **forgotPasswordUrl** s’ouvre dans le navigateur par défaut.  <br/> |
|**hideHyperlinks** <br/> |Indique si l’OSC doit masquer la **Cliquez ici pour créer un compte** et **vous avez oublié votre mot de passe ?** des liens hypertexte dans la boîte de dialogue de configuration de compte.  <br/> OSC 1.0 ignore ce paramètre, et les liens hypertexte sont toujours masqués. OSC 1.1 respecte la valeur de ce paramètre.  <br/> |
|**hideRememberMyPassword** <br/> |Indique si l’OSC doit masquer la case à cocher **Mémoriser mon mot de passe** dans la boîte de dialogue de configuration de compte.  <br/> Si le fournisseur définit **hideRememberMyPassword** comme **true**, l’OSC agira comme si la case **Mémoriser mon mot de passe** est désactivée et le mot de passe n’est pas enregistrées.  <br/> Si le fournisseur définit **hideRememberMyPassword** comme **false**, l’OSC affiche la case à cocher **Mémoriser mon mot de passe** dans la boîte de dialogue de configuration de compte.  <br/> |
|**supportsAutoConfigure** <br/> |Indique si l’OSC doit appeler la fonction **GetAutoConfiguredSession** sur l’interface **ISocialProvider** à essayer de la configuration automatique, ouvrez une session sur le réseau social pour l’utilisateur.  <br/> |
|**useLogonCached** <br/> |Indique si le fournisseur OSC prend en charge l’appel [ISocialSession2::LogonCached](isocialsession2-logoncached.md) se connecter avec des informations d’identification mises en cache.  <br/> Si le fournisseur définit **useLogonCached** comme **true**, l’OSC ignore le paramètre pour **useLogonWebAuth** et l’OSC appelle **ISocialSession2::LogonCached** pour l’authentification.  <br/> Si le fournisseur définit **dynamicActivitiesLookupEx** comme **false**, l’OSC n’appelle pas **ISocialSession2::LogonCached** pour l’authentification.  <br/> |
|**useLogonWebAuth** <br/> |Indique si l’OSC doit utiliser l’authentification basée sur les formulaires et la méthode [ISocialSession::LogonWeb](isocialsession-logonweb.md) . Si le fournisseur définit **useLogonWebAuth** comme **false**, l’OSC utilise l’authentification de base et appelle la méthode [ISocialSession::Logon](isocialsession-logon.md) . Si le fournisseur définit **useLogonWebAuth** comme **true**, l’OSC utilise l’authentification basée sur les formulaires et appelle **ISocialSession::LogonWeb**.  <br/> |
   
Selon les **fonctionnalités** XML renvoyé par le fournisseur dans la méthode **ISocialProvider::GetCapabilities** , la configuration du compte boîte de dialogue change. Par exemple, la Figure 1 montre la boîte de dialogue de configuration de compte pour obtenir un exemple TestProvider. 
  
**La figure 1. Exemple TestProvider dans la boîte de dialogue de configuration de compte**

![Informations de configuration d’exemple TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Voir aussi

- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)

