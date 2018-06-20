---
title: Conseils pour l’affichage correctement les activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Fournisseurs d’Outlook Social Connector (OSC) peuvent définir les éléments getActivities et dynamicActivitiesLookupEx l’OSC de stocker les éléments d’activité en mémoire.
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787577"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Conseils pour l’affichage correctement les activités

Fournisseurs d’Outlook Social Connector (OSC) peuvent définir la **getActivities** et éléments **dynamicActivitiesLookupEx** pour que l’OSC stockent les éléments d’activité en mémoire. Cette rubrique décrit l’extensibilité du fournisseur OSC API l’OSC appelle pour obtenir ou actualiser les activités et les détails de l’activité propriétaire, si le fournisseur OSC prend en charge la synchronisation des activités des flux à partir du réseau social. Il décrit également quelques éléments enfants de l’élément **activityFeed** que le fournisseur OSC doit être défini pour le OSC d’afficher correctement les activités dans la carte de visite Office ou le volet personnes. 
  
- L’OSC appelle la méthode de [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) permettant d’obtenir et de stocker des activités dans le dossier de News pour l’utilisateur connecté. Le fournisseur OSC doit implémenter **GetActivitiesEx** pour renvoyer une chaîne XML _activités_ conforme à la définition de schéma XML de l’élément **activityFeed** du fournisseur OSC. 
    
- Le fournisseur OSC doit définir l’élément **ownerID** , qui est un élément enfant de l’élément **activityDetails** . **ownerID** est une chaîne opaque qui identifie le propriétaire de l’activité sur le réseau social. 
    
- Le fournisseur OSC doit définir les éléments **nameHint** et **emailAddress** dans le nœud **publisherVariable** de l’élément **templateVariables** . 
    
   Notez que, par rapport au schéma XML du fournisseur OSC, l’élément **nameHint** est un élément facultatif. L’OSC utilise pour correspondre au nom complet de l’utilisateur sélectionné dans la carte de visite ou le volet personnes. De même, l’élément **emailAddress** est un élément facultatif dans le schéma XML. L’OSC utilise pour correspondre à l’adresse SMTP de l’utilisateur sélectionné dans la carte de visite ou le volet personnes. 
    
   Si seule l’élément **ownerID** est spécifié, mais un ou les deux **nameHint** et **emailAddress** ne sont pas spécifiés, le OSC appelle la méthode [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) , puis [ISocialPerson::GetDetails](isocialperson-getdetails.md) méthode pour obtenir plus d’informations sur la personne identifiée par **ownerID**. Lorsque l’OSC appelle **ISocialPerson::GetDetails**, le fournisseur doit retourner **personne** XML qui spécifie les éléments **fullName** et **emailAddress** . 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les activités](xml-for-activities.md)  
- [Code XML des amis](xml-for-friends.md)  
- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)

