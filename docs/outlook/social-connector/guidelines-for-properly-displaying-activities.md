---
title: Instructions pour l’affichage correct des activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Les fournisseurs Outlook Social Connector (OSC) peuvent définir les éléments getActivities et dynamicActivitiesLookupEx pour que les éléments d'activité de magasin OSC soient en mémoire.
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286180"
---
# <a name="guidelines-for-properly-displaying-activities"></a>Instructions pour l’affichage correct des activités

Les fournisseurs Outlook Social Connector (OSC) peuvent définir les éléments **GetActivities** et **dynamicActivitiesLookupEx** pour que les éléments d'activité de magasin OSC soient en mémoire. Cette rubrique décrit les API de l'extensibilité du fournisseur OSC que le OSC appelle pour obtenir ou actualiser les activités et les détails du propriétaire de l'activité, si le fournisseur OSC prend en charge la synchronisation des flux d'activités à partir du réseau social. La rubrique répertorie également quelques éléments enfants de l'élément **activityFeed** que le fournisseur OSC doit définir pour le OSC afin d'afficher correctement les activités dans la carte de visite Office ou le volet de personnes Outlook. 
  
- Le OSC appelle la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) pour obtenir et stocker des activités dans le dossier du flux d'actualités de l'utilisateur connecté. Le fournisseur OSC doit implémenter **GetActivitiesEx** pour retourner une chaîne XML d' _activités_ conforme à la définition de schéma XML du fournisseur OSC de l'élément **activityFeed** . 
    
- Le fournisseur OSC doit définir l'élément **ownerID** , qui est un élément enfant de l'élément **activityDetails** . **ownerID** est une chaîne opaque qui identifie le propriétaire de l'activité sur le réseau social. 
    
- Le fournisseur OSC doit définir les éléments **nameHint** et **EmailAddress** dans le nœud **publisherVariable** de l'élément **templateVariables** . 
    
   Notez que, par le schéma XML du fournisseur OSC, l'élément **nameHint** est un élément facultatif. Le OSC l'utilise pour faire correspondre le nom complet de l'utilisateur sélectionné dans la carte de visite ou le volet de personnes. De même, l'élément **EmailAddress** est un élément facultatif dans le schéma XML. Le OSC l'utilise pour correspondre à l'adresse SMTP de l'utilisateur sélectionné dans la carte de visite ou dans le volet de personnes. 
    
   Si seul l'élément **ownerID** est spécifié, mais que l'un ou les deux **nameHint** et **EmailAddress** ne sont pas spécifiés, l'objet OSC appelle la méthode [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) , puis [ISocialPerson:: GetDetails](isocialperson-getdetails.md) méthode pour obtenir plus d'informations sur la personne identifiée par l' **ownerID**. Lorsque l' **utilisateur** OSC appelle **ISocialPerson:: GetDetails**, le fournisseur doit renvoyer du code XML qui spécifie les éléments **FullName** et **EmailAddress** . 
    
## <a name="see-also"></a>Voir aussi

- [XML pour les activités](xml-for-activities.md)  
- [XML pour les amis](xml-for-friends.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md)

