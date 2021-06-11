---
title: Obtention d’activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: L’OSC appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420576"
---
# <a name="getting-activities"></a>Obtention d’activités

L’OSC appelle [la méthode ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **getActivities** et **dynamicActivitiesLookupEx** dans le **XML** des fonctionnalités renvoyées indiquent que le fournisseur OSC prend en charge l’obtention d’activités à la demande et le stockage des activités en mémoire, l’OSC peut effectuer la séquence d’appels suivante. L’OSC note également la fonction de hachage spécifiée dans l’élément **hashFunction** dans le XML **des fonctionnalités.** L’OSC appelle des méthodes dans l’ordre suivant pour obtenir des activités et des informations (telles que prise en charge par l’interface [ISocialPerson)](isocialpersoniunknown.md) pour les amis et les non-amis sur le réseau social : 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : à la fin du processus d’authentification, l’OSC appelle **GetLoggedOnUser** pour obtenir une interface [ISocialProfile](isocialprofileisocialperson.md) pour l’utilisateur authentifié. Pour plus d’informations sur l’authentification, consultez [l’authentification de](basic-authentication.md) base et [l’authentification basée sur les formulaires.](forms-based-authentication.md)
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) — Pour les personnes affichées dans le volet Personnes de Outlook, l’OSC obtient et hait ses adresses SMTP, appelle **ISocialSession2::GetActivitiesEx** et stocke (en mémoire) les données d’activités renvoyées pour ces personnes. L’OSC obtient un paramètre de sortie,  _activities,_ qui est une chaîne qui contient une collection d’activités pour les amis de l’utilisateur connecté. Cette chaîne est conforme à la définition de schéma de **l’élément activityFeed.** 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) —Pour chaque élément **activityDetails** dans le XML **activityFeed** renvoyé par **GetActivitiesEx**, il existe un **élément ownerID** qui indique la personne propriétaire de cette activité. L’OSC utilise cette **valeur ownerID** pour appeler **GetPerson** afin d’obtenir une interface **ISocialPerson** pour cette personne. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) — En fonction de l’objet **ISocialPerson** obtenu à l’étape 3, l’OSC appelle **GetDetails** pour obtenir des détails sur cette personne, tels que le prénom et le nom. L’OSC peut faire de même pour chaque activité spécifiée dans un élément **activityDetails** dans le **XML activityFeed** renvoyé par **GetActivitiesEx** à l’étape 2. 
    
> [!NOTE]
> OsC actualise le cache des activités à un intervalle par défaut. Pour plus d’informations sur l’actualisation du cache d’activités, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

