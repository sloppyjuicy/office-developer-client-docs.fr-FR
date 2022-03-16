---
title: XML pour les activités
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: Cette rubrique contient un exemple de scénario qui montre les appels d’API d’extensibilité du fournisseur Outlook Social Connector (OSC) qu’un fournisseur OSC implémente et qu’OSC effectue pour obtenir des informations sur les activités. Les informations sont exprimées en chaînes XML conformes au schéma XML du fournisseur OSC.
ms.openlocfilehash: 52f431514ff1076b2569e698ed962e01f5eb1a26
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507566"
---
# <a name="xml-for-activities"></a>XML pour les activités

Cette rubrique contient un exemple de scénario qui montre les appels d’API d’extensibilité du fournisseur Outlook Social Connector (OSC) qu’un fournisseur OSC implémente et qu’OSC effectue pour obtenir des informations sur les activités. Les informations sont exprimées en chaînes XML conformes au schéma XML du fournisseur OSC.
  
Le schéma XML du fournisseur OSC permet à un fournisseur OSC de définir des activités. Les informations sur l’activité peuvent inclure le réseau social d’où proviennent les éléments de flux d’activités, les détails de chaque élément de flux d’activités (par exemple, propriétaire, type et date de publication de l’activité) et le modèle d’affichage de l’activité. Pour prendre en charge l’affichage des activités sur le volet Contacts ou la carte de visite, le fournisseur OSC d’un réseau social doit implémenter et renvoyer les activités XML correctes. Pour obtenir un exemple de données XML de flux d’activités, voir [l’exemple XML des flux d’activités](activity-feed-xml-example.md). Pour plus d’informations sur la synchronisation des activités des amis, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). Pour obtenir une définition complète du schéma XML du fournisseur OSC, y compris les éléments requis ou facultatifs, voir Outlook [Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).
  
Dans le scénario suivant, OSC synchronise dynamiquement les activités d’une personne sélectionnée dans le volet Personnes et obtient des détails sur cette personne :
  
1. Un fournisseur OSC qui prend en charge la synchronisation à la demande des activités indique cela à l’OSC à l’aide des éléments **getActivities** et **dynamicActivitiesLookupEx** . Le fournisseur OSC définit également **l’élément hashFunction** . Les trois éléments sont des éléments enfants **de fonctionnalités**.

2. Le fournisseur OSC implémente les méthodes **ISocialProvider::GetCapabilities** et [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .

3. L’OSC appelle **ISocialProvider::GetCapabilities** pour vérifier la valeur de **getActivities** et **dynamicActivitiesLookupEx** afin de vérifier que le fournisseur OSC prend en charge la synchronisation à la demande des activités. L’OSC note également la valeur de **l’élément hashFunction** pris en charge par le fournisseur OSC.

4. OsC actualise le volet Contacts ou la carte de visite pour que l’utilisateur voie les dernières activités de la personne sélectionnée. L’OSC chiffre l’adresse SMTP de la personne à l’aide de la fonction de hachage spécifiée dans l’élément **hashFunction** , en formant une chaîne XML conforme à la définition de schéma XML de l’élément **hashedAddresses** .

5. L’OSC appelle **ISocialSession2::GetActivitiesEx**, en fournissant cette chaîne XML de l’adresse hachée comme paramètre _hashedAddresses_, pour obtenir une collection actuelle d’activités pour cette personne  dans le paramètre d’activités. La _chaîne du paramètre activities_ est conforme à la définition de schéma XML de **l’élément activityFeed** .

6. En fonction de la définition de schéma XML pour **activityFeed**, l’OSC pare davantage  la chaîne d’activités pour connaître le type, la date de publication et d’autres informations sur chaque activité et comment afficher l’activité.

7. Pour obtenir des détails sur la personne sélectionnée, l’OSC appelle [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), fournissant la même chaîne XML d’adresses hachées que l’argument pour le paramètre _personsAddresses_ . Les détails sur la personne sont renvoyés dans le _paramètre personsCollection_ . Ces détails peuvent inclure **firstName**, **lastName** et **emailAddress**. Le _paramètre personsCollection_ est conforme à la définition de schéma XML de **l’élément de** personne.

Vous trouverez plus d’informations sur la spécification de XML pour les activités dans les rubriques suivantes de cette section :
  
- [Vue d’ensemble du XML pour un élément de flux d’activités](overview-of-xml-for-an-activity-feed-item.md)
- [activityDetails, élément](activitydetails-element.md)
- [activityTemplateContainer, élément](activitytemplatecontainer-element.md)
- [Variables de modèle](template-variables.md)
- [Recommandations en matière d’affichage correct des activités](guidelines-for-properly-displaying-activities.md)

## <a name="see-also"></a>Voir aussi

- [Exemple de XML de flux d’activités](activity-feed-xml-example.md)  
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)
- [XML pour les fonctionnalités](xml-for-capabilities.md)  
- [XML pour les amis](xml-for-friends.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
