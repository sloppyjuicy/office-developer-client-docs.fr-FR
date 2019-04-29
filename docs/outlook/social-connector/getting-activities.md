---
title: Obtention d’activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: 'Le OSC appelle la méthode ISocialProvider:: GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.'
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420576"
---
# <a name="getting-activities"></a>Obtention d’activités

Le OSC appelle la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **GetActivities** et **dynamicActivitiesLookupEx** dans le code XML des **fonctionnalités** renvoyées indiquent que le fournisseur OSC prend en charge l'obtention d'activités à la demande et le stockage d'activités dans la mémoire, l'OSC peut procéder comme suit: séquence d'appel. OSC note également la fonction de hachage spécifiée dans l'élément **hashFunction** dans le code XML des **fonctionnalités** . Le OSC appelle des méthodes dans la séquence suivante pour obtenir des activités et des informations (telles que prises en charge par l'interface [ISocialPerson](isocialpersoniunknown.md) ) pour des amis et des non-Friends sur le réseau social: 
  
1. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) : à la fin du processus d'authentification, OSC appelle **GetLoggedOnUser** pour obtenir une interface [ISocialProfile](isocialprofileisocialperson.md) pour l'utilisateur authentifié. Pour plus d'informations sur l'authentification, consultez la rubrique authentification de [base](basic-authentication.md) et [authentification basée sur les formulaires](forms-based-authentication.md).
    
2. [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) : pour les personnes affichées dans le volet de contacts Outlook, OSC Obtient et hache leurs adresses SMTP, appelle **ISocialSession2:: GetActivitiesEx**et stocke (en mémoire) les données d'activités renvoyées pour ces personnes. Le OSC se trouve dans un paramètre de __ sortie, Activities, qui est une chaîne qui contient une collection d'activités pour les amis de l'utilisateur connecté. Cette chaîne est conforme à la définition de schéma pour l'élément **activityFeed** . 
    
3. [ISocialSession:: GetPerson](isocialsession-getperson.md) : pour chaque élément **activityDetails** dans le code XML **activityFeed** renvoyé par **GetActivitiesEx**, il existe un élément **ownerID** qui indique la personne propriétaire de cette activité. Le OSC utilise cette valeur **ownerID** pour appeler **GetPerson** afin d'obtenir une interface **ISocialPerson** pour cette personne. 
    
4. [ISocialPerson:: GetDetails](isocialperson-getdetails.md) : en fonction de l'objet **ISocialPerson** obtenu à l'étape 3, l'utilisateur OSC appelle **GetDetails** pour obtenir les détails de cette personne, tels que le prénom et le nom. Le OSC peut effectuer les mêmes opérations pour chaque activité spécifiée dans un élément **activityDetails** dans le code XML **activityFeed** renvoyé par **GetActivitiesEx** à l'étape 2. 
    
> [!NOTE]
> Le OSC actualise le cache des activités à un intervalle par défaut. Pour plus d'informations sur l'actualisation du cache des activités, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)

