---
title: Obtention d’activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: L’OSC appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: ec8ee2243fbc8128968436a021ab48494b11ffce
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375509"
---
# <a name="getting-activities"></a>Obtention d’activités

L’OSC appelle [la méthode ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social. Si les éléments **getActivities** et **dynamicActivitiesLookupEx** dans **le XML** des fonctionnalités renvoyées indiquent que le fournisseur OSC prend en charge l’obtention d’activités à la demande et le stockage des activités en mémoire, l’OSC peut effectuer la séquence d’appels suivante. L’OSC note également la fonction de hachage spécifiée dans l’élément **hashFunction** dans le XML **des fonctionnalités** . L’OSC appelle des méthodes dans l’ordre suivant pour obtenir des activités et des informations (telles que prise en charge par l’interface [ISocialPerson](isocialpersoniunknown.md) ) pour les amis et les non-amis sur le réseau social :
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) : à la fin du processus d’authentification, l’OSC appelle **GetLoggedOnUser** pour obtenir une interface [ISocialProfile](isocialprofileisocialperson.md) pour l’utilisateur authentifié. Pour plus d’informations sur l’authentification, voir [Authentification de](basic-authentication.md) base et [authentification basée sur les formulaires](forms-based-authentication.md).

2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) — Pour les personnes affichées dans le volet Personnes de Outlook, l’OSC obtient et hait ses adresses SMTP, appelle **ISocialSession2::GetActivitiesEx** et stocke (en mémoire) les données d’activités renvoyées pour ces personnes. L’OSC obtient un paramètre de sortie, _activities_, qui est une chaîne qui contient une collection d’activités pour les amis de l’utilisateur connecté. Cette chaîne est conforme à la définition de schéma de **l’élément activityFeed** .

3. [ISocialSession::GetPerson](isocialsession-getperson.md) —Pour chaque élément **activityDetails** dans le XML **activityFeed** renvoyé par **GetActivitiesEx**, il existe un **élément ownerID** qui indique la personne propriétaire de cette activité. L’OSC utilise cette **valeur ownerID** pour appeler **GetPerson** afin d’obtenir une interface **ISocialPerson** pour cette personne.

4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) — En fonction de l’objet **ISocialPerson** obtenu à l’étape 3, l’OSC appelle **GetDetails** pour obtenir les détails de cette personne, tels que le prénom et le nom. L’OSC peut faire de même pour chaque activité spécifiée dans un élément **activityDetails** dans le **XML activityFeed** renvoyé par **GetActivitiesEx** à l’étape 2.

> [!NOTE]
> L’OSC actualise le cache des activités à un intervalle par défaut. Pour plus d’informations sur l’actualisation du cache d’activités, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)
