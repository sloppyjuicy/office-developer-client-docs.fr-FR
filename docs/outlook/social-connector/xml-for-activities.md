---
title: XML pour les activités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Cette rubrique contient un exemple de scénario qui montre le fournisseur Outlook Social Connector (OSC) appels API d’extensibilité qui implémente un fournisseur OSC et l’OSC permet d’obtenir des informations sur des activités. Informations sont exprimées dans des chaînes de code XML conforme au schéma XML OSC fournisseur.
ms.openlocfilehash: 44f74d9e72eec3ff6da7f9967315fc9d75191584
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787721"
---
# <a name="xml-for-activities"></a>XML pour les activités

Cette rubrique contient un exemple de scénario qui montre le fournisseur Outlook Social Connector (OSC) appels API d’extensibilité qui implémente un fournisseur OSC et l’OSC permet d’obtenir des informations sur des activités. Informations sont exprimées dans des chaînes de code XML conforme au schéma XML OSC fournisseur.
  
Le schéma XML du fournisseur OSC permet à un fournisseur OSC définir les activités. Informations sur les activités peuvent inclure le réseaux sociaux, où les informations sur les activités à l’origine, les éléments détails de chaque élément d’informations sur les activités (telles que le propriétaire, tapez et date de publication de l’activité) et le modèle pour afficher l’activité. Pour prendre en charge des activités d’affichage dans le volet personnes ou d’une carte de visite, fournisseur OSC d’un réseau social doit mettre en œuvre et renvoyer les activités correctes XML. Pour obtenir un exemple de l’activité de flux XML, voir [Exemple de code XML activité de flux](activity-feed-xml-example.md). Pour plus d’informations sur la synchronisation des activités de vos amis, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). Pour une définition complète du schéma XML de fournisseur OSC, y compris les éléments qui sont obligatoires ou facultatives, voir [Schéma du XML fournisseur Outlook Social Connector](outlook-social-connector-provider-xml-schema.md). 
  
Dans le scénario suivant, l’OSC dynamiquement synchronise les activités d’une personne sélectionnée dans le volet personnes et obtient des informations relatives à cette personne :
  
1. Un fournisseur OSC qui prend en charge la synchronisation de la demande d’activités qui indique à l’OSC en utilisant les éléments **getActivities** et **dynamicActivitiesLookupEx** . Le fournisseur OSC définit également l’élément **hashFunction** . Tous les trois éléments sont des éléments enfants de **fonctionnalités**. 
    
2. Le fournisseur OSC implémente les méthodes **ISocialProvider::GetCapabilities** et [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. Les appels OSC **ISocialProvider::GetCapabilities** pour vérifier la valeur de **getActivities** et **dynamicActivitiesLookupEx** pour vérifier que le fournisseur OSC prend en charge la synchronisation de la demande d’activités. L’OSC notes également la valeur de l’élément **hashFunction** pris en charge par le fournisseur OSC. 
    
4. L’OSC actualise le volet personnes ou une carte de visite pour permettre à l’utilisateur de voir les activités le plus récent de la personne sélectionnée. L’OSC chiffre adresse SMTP de la personne à l’aide de la fonction de hachage spécifiée dans l’élément **hashFunction** , formation d’une chaîne XML qui est conforme à la définition de schéma XML pour l’élément **hashedAddresses** . 
    
5. L’OSC appelle **ISocialSession2::GetActivitiesEx**, fournir cette chaîne XML de l’adresse de hachage en tant que paramètre _hashedAddresses_ , pour obtenir une collection d’activités en cours correspondant à cette personne dans le paramètre _activités_ . La chaîne de paramètre _activités_ est conforme à la définition de schéma XML de l’élément **activityFeed** . 
    
6. En fonction de la définition de schéma XML pour **activityFeed**, plus le OSC analyse la chaîne de _activités_ pour déterminer le type, date et autres informations sur chaque activité et comment afficher l’activité de publication. 
    
7. Pour obtenir plus d’informations sur la personne sélectionnée, le OSC appelle [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), fournissant la même chaîne XML des adresses de hachage en tant qu’argument pour le paramètre _personsAddresses_ . Les plus d’informations sur la personne sont retournés dans le paramètre _personsCollection_ . Il peut s’agir **firstName**, **lastName**et **emailAddress**. Le paramètre _personsCollection_ est conforme à la définition de schéma XML pour l’élément de la **personne** . 
    
Vous trouverez plus d’informations sur la spécification XML pour les activités dans les rubriques suivantes de cette section :
  
- [Vue d’ensemble du code XML pour une activité de flux d’élément](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails, élément](activitydetails-element.md)
    
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)
    
- [Variables de modèle](template-variables.md)
    
- [Conseils pour l’affichage correctement les activités](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>Voir aussi

- [Exemple de flux XML d’activité](activity-feed-xml-example.md)  
- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md) 
- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)  
- [Code XML des amis](xml-for-friends.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

