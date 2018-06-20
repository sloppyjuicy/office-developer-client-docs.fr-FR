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
ms.openlocfilehash: 82bb5322118fa3ebd7610f56b8f34ae95b59a40f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787578"
---
# <a name="getting-activities"></a>Obtention d’activités

L’OSC appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **getActivities** et **dynamicActivitiesLookupEx** dans le renvoyée XML des **capacités** indiquent que le fournisseur OSC prend en charge les activités de mise en route sur la demande et le stockage des activités en mémoire, l’OSC peut rendre les éléments suivants séquence d’appel. L’OSC notes également la fonction de hachage spécifiée dans l’élément **hashFunction** dans le XML des **fonctionnalités** . L’OSC appelle des méthodes dans l’ordre suivant pour obtenir des informations et les activités (tel qu’il est pris en charge par l’interface [ISocialPerson](isocialpersoniunknown.md) ) d’amis ou non amis sur le réseau social : 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) — à la fin du processus d’authentification, l’OSC appelle **GetLoggedOnUser** pour obtenir une interface [ISocialProfile](isocialprofileisocialperson.md) pour l’utilisateur authentifié. Pour plus d’informations sur l’authentification, voir [L’authentification de base](basic-authentication.md) et [l’authentification basée sur les formulaires](forms-based-authentication.md).
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) — pour les personnes affichées dans le volet personnes Outlook, obtient l’OSC et hachages leur SMTP résout, appelle **ISocialSession2::GetActivitiesEx**et stocke les données activités (en mémoire) renvoyées pour ces personnes. Il obtient l’OSC dans un paramètre de sortie, _les activités_, qui est une chaîne qui constituée une collection d’activités d’amis ou de l’utilisateur connecté. Cette chaîne est conforme à la définition de schéma pour l’élément **activityFeed** . 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) — pour chaque élément **activityDetails** dans le code XML renvoyé par **GetActivitiesEx** **activityFeed** , il existe un élément **ownerID** qui indique la personne qui possède cette activité. L’OSC utilise cette valeur **ownerID** pour appeler **GetPerson** pour obtenir une interface **ISocialPerson** correspondant à cette personne. 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) — en fonction de l’objet **ISocialPerson** obtenu à l’étape 3, le OSC appelle **GetDetails** pour obtenir plus d’informations pour cette personne, telles que le prénom et le nom. L’OSC peut faire de même pour chaque activité spécifiée dans un élément **activityDetails** **activityFeed** le code XML renvoyé par **GetActivitiesEx** à l’étape 2. 
    
> [!NOTE]
> L’OSC actualise le cache des activités à un intervalle par défaut. Pour plus d’informations sur l’actualisation du cache d’activités, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

