---
title: Éléments XML des fonctionnalités
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: Les tableaux de cette rubrique décrivent les éléments enfants des fonctionnalités XML et sont regroupés par domaines qu’ils supportent.
ms.openlocfilehash: bc351939675f1603267116dc87d7ca6028cb0561
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372443"
---
# <a name="capabilities-xml-elements"></a>Éléments XML des fonctionnalités

Les tableaux de cette rubrique décrivent les éléments enfants des fonctionnalités **XML** et sont regroupés par domaines qu’ils supportent. La valeur par défaut de chaque **élément capabilities** est **false**. Si l’élément n’est pas spécifié dans les fonctionnalités **XML** renvoyées par la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , la valeur de l’élément est égale à **false**.
  
Pour une description générale des **fonctionnalités** XML, voir [XML for Capabilities](xml-for-capabilities.md). Pour obtenir un exemple de **fonctionnalités** XML, voir [Exemple de fonctionnalités XML](capabilities-xml-example.md). Pour obtenir une définition complète du schéma XML du fournisseur Microsoft Outlook Social Connector (OSC), y compris les éléments requis ou facultatifs, voir [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Fonctionnalités de prise en charge des amis

Le tableau suivant présente les éléments qui s’appliquent à toute forme de synchronisation d’amis ou de non-amis.
  
|**Élément**|**Description**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Indique si le fournisseur prend en charge l’appel de méthode [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md) . **followPerson et** **doNotFollowPerson sont** des fonctionnalités indépendantes d’un fournisseur OSC. Un fournisseur OSC peut indiquer la possibilité d’ajouter une personne en tant qu’ami (définir **followPerson** sur **true**) ou de supprimer une personne en tant qu’ami sur un compte de réseau social (définition **de doNotFollowPerson** sur **true**). En règle générale, la possibilité de suivre n’implique pas de pouvoir arrêter le suivi. **followPerson** est une fonctionnalité qui ne doit pas être interprétée comme une action de suivi d’une personne spécifique ou de chaque personne sur le compte de réseau social. **La valeur followPerson** **n’implique** pas **que doNotFollowPerson** est **false**. |
|**followPerson** <br/> |Indique si le fournisseur prend en charge l’appel de méthode [ISocialSession::FollowPerson](isocialsession-followperson.md) . Les vérifications OSC **suiventPerson** si **cacheFriends** est **vrai (synchronisation** mise en cache des amis), **dynamicContactsLookup** est **vrai** (synchronisation à la demande des amis et non-amis) ou les deux **cacheFriends** et **dynamicContactsLookup** sont true (synchronisation hybride des amis et non-amis). Si le fournisseur définit **followPerson** comme **vrai**, l’OSC affiche un badge réseau dans le volet Personnes pour les personnes que l’utilisateur suit, et active la commande **Sur \<NetworkName\>** dans le menu Ajouter **(+)** dans le volet Personnes. Si le fournisseur définit **followPerson** comme **false**, le badge réseau n’est pas affiché et la **commande sur \<NetworkName\>** est masquée. |
|**getFriends** <br/> |Indique si le fournisseur prend en charge l’appel de méthode [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) ou [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . Si le fournisseur définit **getFriends** comme **vrai**, l’OSC utilise la valeur **cacheFriends** ou **dynamicContactsLookup** pour déterminer si le réseau social autorise le stockage d’amis en tant qu’éléments de contact Outlook ou en mémoire. Si le fournisseur définit **getFriends** comme **faux, le** réseau social ne prend pas en charge les amis et les méthodes **ISocialPerson::GetFriendsAndColleagues** et **ISocialSession2::GetPeopleDetails** , et l’OSC ignore les valeurs de **cacheFriends** et **dynamicContactsLookup**. |

Les éléments suivants s’appliquent uniquement à la synchronisation mise en cache des amis ou à la synchronisation hybride des amis et des non-amis. Pour plus d’informations sur la synchronisation des amis, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
|**Élément**|**Description**|
|:-----|:-----|
|**cacheFriends** <br/> |Indique si le fournisseur OSC autorise le stockage d’amis sous la Outlook des éléments de contact. L’OSC vérifie **cacheFriends uniquement** si **getFriends** est **vrai**. Si le fournisseur définit **cacheFriends** comme **vrai**, l’OSC synchronise les amis par la mise en cache et crée un dossier de contacts propre au réseau dans la boutique par défaut de l’utilisateur pour les contacts amis. Le nom du dossier de contacts propre au réseau est la valeur de la propriété [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . Si le fournisseur définit **cacheFriends** comme **faux**, l’OSC ne crée pas de dossier de contacts spécifiques au réseau pour stocker des amis. |
|**contactSyncRestartInterval** <br/> |Détermine l’intervalle de nouvelle tentative, en minutes, entre les tentatives de synchronisation des informations des amis à partir du réseau social, en cas d’erreur de synchronisation. L’OSC utilise cet élément uniquement si le fournisseur OSC prend en charge la synchronisation mise en cache ou la synchronisation hybride des amis vers un dossier de contacts propre au réseau social (**cacheFriends** est **vrai**). L’intervalle de nouvelle tentative par défaut est de 30 minutes, sauf si la valeur par défaut est overridée par la `ContactSyncRestartInterval` clé sous `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`. Si le fournisseur définit **contactSyncRestartInterval**, la valeur du fournisseur remplace l’intervalle de nouvelle tentative par défaut de 30 minutes ou la valeur de la clé de Registre. Pour plus d’informations sur la synchronisation des amis et des non-amis à la demande, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). |

Les éléments suivants s’appliquent uniquement à la synchronisation à la demande ou à la synchronisation hybride des amis et des non-amis.
  
|**Élément**|**Description**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Indique si le fournisseur OSC prend en charge l’appel [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) pour la synchronisation à la demande des amis et non-amis. L’OSC vérifie **dynamicContactsLookup uniquement** si **getFriends** est **vrai**. Le paramètre par défaut **de dynamicContactsLookup** est **false**. Si le fournisseur OSC spécifie **dynamicContactsLookup** comme **true** et **getFriends** comme **true**, l’OSC appelle **ISocialSession2::GetPeopleDetails** chaque fois que le volet Personnes est actualisé. Le volet Personnes est actualisé lorsque l’utilisateur sélectionne un autre utilisateur dans le volet Personnes ou un autre élément dans la fenêtre de l’explorateur Outlook, ou ouvre une fenêtre d’inspecteur Outlook utilisateur. La recherche dynamique de contacts garantit que l’utilisateur voit toujours les dernières images de l’utilisateur et les informations de profil dans le volet Contacts, mais augmente le nombre d’appels du fournisseur vers le réseau social. Si le fournisseur définit **dynamicContactsLookup** comme **false**, l’OSC n’appelle pas **ISocialSession2::GetPeopleDetails** pour actualiser le volet Personnes. |
|**showOnDemandContactsWhenMinimized** <br/> |Indique si l’OSC doit effectuer une synchronisation à la demande pour les amis et les non-amis lorsque le volet Personnes est réduit. |

## <a name="capabilities-for-supporting-activities"></a>Fonctionnalités de prise en charge des activités

L’élément suivant s’applique à toute forme de synchronisation des activités prise en charge par le fournisseur OSC.
  
|**Élément**|**Description**|
|:-----|:-----|
|**getActivities** <br/> |Indique si le fournisseur prend en charge les appels de méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) ou [ISocialPerson::GetActivities](isocialperson-getactivities.md) . Si le fournisseur définit **getActivities** comme **true**, l’OSC utilise la valeur **cacheActivities** ou **dynamicActivitiesLookupEx** pour déterminer si le site de réseau social autorise le stockage des activités en tant qu’éléments RSS Outlook ou en tant qu’activités en mémoire. Si le fournisseur définit **getActivities** comme **false**, le réseau social ne prend pas en charge les activités et les méthodes **ISocialSession2::GetActivitiesEx** et **ISocialPerson::GetActivities** , et l’OSC ignore les valeurs de **cacheActivities** et **dynamicActivitiesLookupEx**. |

L’élément suivant s’applique uniquement à la synchronisation mise en cache ou à la synchronisation hybride des activités.
  
|**Élément**|**Description**|
|:-----|:-----|
|**cacheActivities** <br/> |À compter de Outlook Social Connector 2013, l’OSC ignore cet élément, car les fournisseurs ne peuvent plus synchroniser les activités en les achant dans un dossier masqué dans la boutique de l’utilisateur. Si le fournisseur prend en charge les activités, il doit prendre en charge la synchronisation des activités à la demande. Le fournisseur définit **cacheActivities** comme **false** et **définit dynamicActivitesLookupEx** comme **true**. L’OSC synchronise les activités à la demande et met en cache les activités en mémoire. Le cache mémoire des activités est actualisé pendant un intervalle de 30 minutes. |

Les éléments suivants s’appliquent uniquement à la synchronisation à la demande ou à la synchronisation hybride des activités.
  
|**Élément**|**Description**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |Supprimé dans OSC 1.1. À partir d’OSC 1.1, l’OSC n’appelle plus [ISocialSession::GetActivities](isocialsession-getactivities.md) et ignore la valeur **de dynamicActivitiesLookup**. Pour prendre en charge la recherche d’activités à la demande, définissez **cacheActivities** sur **false** et **getActivities** et **dynamicActivitiesLookupEx** comme **true**, et l’OSC appelle **ISocialSession2::GetActivitiesEx**. |
|**dynamicActivitiesLookupEx** <br/> |Indique si le fournisseur OSC prend en charge l’appel **ISocialSession2::GetActivitiesEx** pour la synchronisation à la demande des activités. Si le fournisseur OSC prend en charge la synchronisation des activités à la demande, il définit **getActivities** et **dynamicActivitiesLookupEx** comme **true** et **cacheActivities** comme **false**. L’OSC appelle **ISocialSession2::GetActivitiesEx** chaque fois que le volet Personnes est actualisé. Le volet Personnes est actualisé lorsque l’utilisateur modifie l’élément sélectionné dans la fenêtre Outlook’explorateur ou ouvre une fenêtre Outlook’inspecteur. La recherche d’activités dynamiques garantit que l’utilisateur verra toujours les dernières activités dans le volet Personnes, mais qu’il augmente le nombre d’appels du fournisseur vers le réseau social. Si le fournisseur définit **dynamicActivitiesLookupEx** comme **false**, l’OSC n’appelle pas **ISocialSession2::GetActivitiesEx** pour les personnes affichées dans le volet Personnes. |
|**showOnDemandActivitiesWhenMinimized** <br/> |Indique si l’OSC doit effectuer une synchronisation à la demande pour les activités lorsque le volet Personnes est réduit. |

## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Fonctionnalités courantes pour la prise en charge de la synchronisation à la demande ou hybride d’amis, de non-amis et d’activités

|**Élément**|**Description**|
|:-----|:-----|
|**hashFunction** <br/> | Spécifie la fonction de hachage que le fournisseur OSC prend en charge. Pour protéger les informations d’identification personnelle des utilisateurs qui ne sont pas sur le réseau social ou l’application métier du fournisseur, l’OSC transmet les adresses e-mail hachées à **ISocialSession2::GetPeopleDetails** et **ISocialSession2::GetActivitiesEx**.  Si **dynamicContactsLookup** est définie sur **true** ou **dynamicActivitiesLookupEx** est définie sur **true**, le fournisseur doit définir **hashFunction** sur l’une des valeurs autorisées : **SHA1**, **MD5** ou **CRC32MD5**. Si **hashFunction est** manquant ou spécifie une valeur incorrecte, l’OSC renvoie une erreur. **SHA1 est** internet Engineering Task Force (IETF) US Secure Hash Algorithm 1 défini par [[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt). Par exemple, la **valeur de** hachage SHA1 de l’adresse de messagerie melissa@contoso.com est `bb81577b567262a21a4df5f6e335c1250acd7b50`. **MD5** est le groupe de travail IETF (Internet Engineering Task Force) MD5 Message-Digest algorithme défini par [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt). Par exemple, la valeur de **hachage MD5** de l’adresse de messagerie melissa@contoso.com est `c8c39e61ca1662477b39b83d7b0a0615`. **CRC32MD5** est une combinaison de **CRC32** et **MD5 définie** comme suit :  <br/>  Normalisez l’adresse e-mail en supprimant les espaces de début et de fin et en convertissant tous les caractères en minuscules.  Calculez la **valeur CRC32** pour l’adresse e-mail normalisation et utilisez la représentation d’un nombre nombre incimal de cette valeur. Si votre implémentation renvoie des integers signés, vous devez convertir l’integer signé en un integer non signé.  Calculez la **valeur MD5** pour l’adresse e-mail normalisation et utilisez la représentation hexadée de cette valeur (en minuscules pour A à F).  Combinez ces deux valeurs avec un trait de soulignement.  Par exemple, la **valeur de hachage CRC32MD5** de l’adresse de melissa@contoso.com est `2149665315_c8c39e61ca1662477b39b83d7b0a0615`. |

## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Fonctionnalités de prise en charge de l’authentification et de la configuration de compte

|**Élément**|**Description**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Indique si le réseau social permet à l’utilisateur de modifier les paramètres de configuration automatique, par exemple en fournissant une URL différente pour se connecter. |
|**createAccountUrl** <br/> |Si le fournisseur définit **hideHyperlinks** comme **false**, lorsque l’utilisateur clique  sur Cliquer ici pour créer un compte dans la boîte de dialogue **Configuration** du compte, l’URL spécifiée par **createAccountUrl** s’ouvre dans le navigateur par défaut. |
|**displayUrl** <br/> |Indique si OSC doit afficher la zone de texte Adresse **de l’URL** pour le réseau social dans la boîte de dialogue configuration du compte. |
|**forgotPasswordUrl** <br/> |Si le fournisseur définit **hideHyperlinks** comme **faux**, lorsque l’utilisateur clique sur Vous avez oublié votre mot de passe **?** Dans la boîte de dialogue **Configuration** du compte, l’URL spécifiée par **forgotPasswordUrl** s’ouvre dans le navigateur par défaut. |
|**hideHyperlinks** <br/> |Indique si OSC doit masquer le bouton Cliquer  ici pour créer un compte et a oublié votre mot de passe **?** Liens hypertexte dans la boîte de dialogue configuration du compte. OSC 1.0 ignore ce paramètre et les liens hypertexte sont toujours masqués. OSC 1.1 observe la valeur de ce paramètre. |
|**hideRememberMyPassword** <br/> |Indique si OSC doit masquer la case à cocher Mémoriser **mon mot** de passe dans la boîte de dialogue configuration du compte. Si le fournisseur définit **hideRememberMyPassword** comme **vrai**, l’OSC agit comme si la  zone Mémoriser mon mot de passe est décochée et n’enregistre pas le mot de passe. Si le fournisseur définit **hideRememberMyPassword** comme **false**, l’OSC affiche la  case à cocher Mémoriser mon mot de passe dans la boîte de dialogue configuration du compte. |
|**supportsAutoConfigure** <br/> |Indique si OSC doit appeler la fonction **GetAutoConfiguredSession** sur l’interface **ISocialProvider** pour tenter la configuration automatique et se connecter au réseau social de l’utilisateur. |
|**useLogonCached** <br/> |Indique si le fournisseur OSC prend en charge l’appel [ISocialSession2::LogonCached](isocialsession2-logoncached.md) pour se connecter avec les informations d’identification mises en cache. Si le fournisseur définit **useLogonCached** comme **true**, l’OSC ignore le paramètre pour **useLogonWebAuth** et l’OSC appelle **ISocialSession2::LogonCached** pour l’authentification. Si le fournisseur définit **dynamicActivitiesLookupEx** comme **false**, l’OSC n’appelle pas **ISocialSession2::LogonCached** pour l’authentification. |
|**useLogonWebAuth** <br/> |Indique si l’OSC doit utiliser l’authentification basée sur les formulaires et la méthode [ISocialSession::LogonWeb](isocialsession-logonweb.md) . Si le fournisseur définit **useLogonWebAuth** comme **false**, l’OSC utilise l’authentification de base et appelle la [méthode ISocialSession::Logon](isocialsession-logon.md) . Si le fournisseur définit **useLogonWebAuth** comme **true**, l’OSC utilise l’authentification basée sur les formulaires et appelle **ISocialSession::LogonWeb**. |

Selon les **fonctionnalités** XML renvoyées par le fournisseur dans la méthode **ISocialProvider::GetCapabilities** , la boîte de dialogue de configuration du compte change. Par exemple, la figure 1 montre la boîte de dialogue de configuration de compte pour un exemple TestProvider.
  
**Figure 1. Exemple TestProvider dans la boîte de dialogue configuration du compte**

![Informations de configuration d’exemple TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
