---
title: XML pour les activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Cette rubrique contient un exemple de scénario illustrant les appels de l'API d'extensibilité du fournisseur Outlook Social Connector (OSC) qu'un fournisseur OSC implémente et l'interface OSC pour obtenir des informations sur les activités. Les informations sont exprimées dans des chaînes XML conformes au schéma XML du fournisseur OSC.
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409628"
---
# <a name="xml-for-activities"></a>XML pour les activités

Cette rubrique contient un exemple de scénario illustrant les appels de l'API d'extensibilité du fournisseur Outlook Social Connector (OSC) qu'un fournisseur OSC implémente et l'interface OSC pour obtenir des informations sur les activités. Les informations sont exprimées dans des chaînes XML conformes au schéma XML du fournisseur OSC.
  
Le schéma XML du fournisseur OSC permet à un fournisseur OSC de définir des activités. Les informations sur l'activité peuvent inclure le réseau social où sont issus les éléments de flux d'activités, les détails de chaque élément de flux d'activité (par exemple, le propriétaire, le type et la date de publication de l'activité), ainsi que le modèle pour afficher l'activité. Pour prendre en charge l'affichage des activités dans le volet contacts ou la carte de visite, le fournisseur OSC d'un réseau social doit implémenter et renvoyer le XML des activités correct. Pour obtenir un exemple de XML d'informations sur les activités, voir [exemple de XML](activity-feed-xml-example.md)d'informations sur les activités. Pour plus d'informations sur la synchronisation des activités des amis, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). Pour obtenir une définition complète du schéma XML du fournisseur OSC, y compris les éléments requis ou facultatifs, voir [schéma XML du fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md). 
  
Dans le scénario suivant, le OSC synchronise dynamiquement les activités pour une personne sélectionnée dans le volet personnes, et obtient des détails sur cette personne:
  
1. Un fournisseur OSC qui prend en charge la synchronisation à la demande des activités indique qu'au OSC à l'aide des éléments **GetActivities** et **dynamicActivitiesLookupEx** . Le fournisseur OSC définit également l'élément **hashFunction** . Les trois éléments sont des éléments enfants des **fonctionnalités**. 
    
2. Le fournisseur OSC implémente les méthodes **ISocialProvider:: GetCapabilities** et [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. Le OSC appelle **ISocialProvider:: GetCapabilities** pour vérifier la valeur de **GetActivities** et **dynamicActivitiesLookupEx** afin de vérifier que le fournisseur OSC prend en charge la synchronisation à la demande des activités. Le OSC note également la valeur de l'élément **hashFunction** pris en charge par le fournisseur OSC. 
    
4. Le OSC actualise le volet personnes ou la carte de visite pour permettre à l'utilisateur de consulter les dernières activités de la personne sélectionnée. Le OSC chiffre l'adresse SMTP de la personne à l'aide de la fonction de hachage spécifiée dans l'élément **hashFunction** , formant une chaîne XML conforme à la définition de schéma XML pour l'élément **hashedAddresses** . 
    
5. Le OSC appelle **ISocialSession2:: GetActivitiesEx**, en fournissant cette chaîne XML de l'adresse hachée en tant que paramètre _hashedAddresses_ , pour obtenir une collection d'activités en cours pour cette personne dans le paramètre _Activities_ . La __ chaîne de paramètre Activities est conforme à la définition de schéma XML de l'élément **activityFeed** . 
    
6. En fonction de la définition de schéma XML pour **activityFeed**, le OSC analyse la chaîne d' _activités_ pour déterminer le type, la date de publication et d'autres informations sur chaque activité, et comment afficher l'activité. 
    
7. Pour obtenir des détails sur la personne sélectionnée, le OSC appelle [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md), en fournissant la même chaîne XML d'adresses hachées que l'argument pour le paramètre _personsAddresses_ . Les détails relatifs à la personne sont renvoyés dans le paramètre _personsCollection_ . Ces détails peuvent être les suivants: **prénom**, **nom**et **EmailAddress**. Le paramètre _personsCollection_ est conforme à la définition de schéma XML pour l'élément **Person** . 
    
Vous trouverez plus d'informations sur la spécification de XML pour les activités dans les rubriques suivantes de cette section:
  
- [Vue d'ensemble du code XML pour un élément de flux d'activité](overview-of-xml-for-an-activity-feed-item.md)
    
- [Élément activityDetails](activitydetails-element.md)
    
- [Élément activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de modèle](template-variables.md)
    
- [Instructions pour afficher correctement les activités](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Voir aussi

- [Exemple de XML d'informations sur les activités](activity-feed-xml-example.md)  
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md) 
- [XML pour les fonctionnalités](xml-for-capabilities.md)  
- [XML pour les amis](xml-for-friends.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

