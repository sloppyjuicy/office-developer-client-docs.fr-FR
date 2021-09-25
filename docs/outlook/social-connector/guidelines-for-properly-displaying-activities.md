---
title: Instructions pour l’affichage correct des activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Les fournisseurs OSC (Social Connector) peuvent définir les éléments getActivities et dynamicActivitiesLookupEx de manière à ce qu’ILS stockent les éléments d’activité en mémoire.
ms.openlocfilehash: 77763ca1ec1f95ec0220c1cf59f3bdd61aa53bff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560395"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Instructions pour l’affichage correct des activités

Outlook Les fournisseurs OSC (Social Connector) peuvent définir les éléments **getActivities** et **dynamicActivitiesLookupEx** de manière à ce qu’ILS stockent les éléments d’activité en mémoire. Cette rubrique décrit les API d’extensibilité du fournisseur OSC que l’OSC appelle pour obtenir ou actualiser les activités et les détails du propriétaire de l’activité, si le fournisseur OSC prend en charge la synchronisation des flux d’activités à partir du réseau social. Cette rubrique répertorie également quelques éléments enfants de l’élément **activityFeed** que le fournisseur OSC doit définir pour qu’OSC affiche correctement les activités dans la carte de visite Office ou le volet contacts Outlook. 
  
- L’OSC appelle la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) pour obtenir et stocker les activités dans le dossier Des flux d’actualités pour l’utilisateur connecté. Le fournisseur OSC doit implémenter **GetActivitiesEx** pour retourner une chaîne _XML_ d’activités conforme à la définition de schéma XML du fournisseur OSC de l’élément **activityFeed.** 
    
- Le fournisseur OSC doit définir **l’élément ownerID,** qui est un élément enfant de l’élément **activityDetails.** **ownerID** est une chaîne opaque qui identifie le propriétaire de l’activité sur le réseau social. 
    
- Le fournisseur OSC doit définir les éléments **nameHint** et **emailAddress** dans le nœud **publisherVariable** de l’élément **templateVariables.** 
    
   Notez que, selon le schéma XML du fournisseur OSC, **l’élément nameHint** est un élément facultatif. L’OSC l’utilise pour correspondre au nom complet de l’utilisateur sélectionné dans la carte de visite ou le volet Contacts. De même, **l’élément emailAddress** est un élément facultatif dans le schéma XML. L’OSC l’utilise pour correspondre à l’adresse SMTP de l’utilisateur sélectionné dans la carte de visite ou le volet Contacts. 
    
   Si seul l’élément **ownerID** est spécifié, mais qu’un ou les deux de **nameHint** et **emailAddress** ne sont pas spécifiés, l’OSC appelle la méthode [ISocialSession2::GetPeopleDetails,](isocialsession2-getpeopledetails.md) puis la méthode [ISocialPerson::GetDetails](isocialperson-getdetails.md) pour obtenir plus d’informations sur la personne identifiée par **ownerID**. Lorsque l’OSC appelle **ISocialPerson::GetDetails,** le fournisseur doit retourner le **code** XML de la personne qui spécifie les éléments **fullName** et **emailAddress.** 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les activités](xml-for-activities.md)  
- [XML pour les amis](xml-for-friends.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md)

