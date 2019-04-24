---
title: Séquences d’appels classiques OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Cette section décrit les séquences d'appel classiques Outlook Social Connector (OSC) dans les interfaces d'extensibilité du fournisseur OSC, qui sont implémentées par un fournisseur OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356265"
---
# <a name="osc-typical-calling-sequences"></a>Séquences d’appels classiques OSC

Cette section décrit les séquences d'appel classiques Outlook Social Connector (OSC) dans les interfaces d'extensibilité du fournisseur OSC, qui sont implémentées par un fournisseur OSC. Les séquences d'appel classiques montrent comment et quand OSC utilise ces interfaces et méthodes, pour vous permettre de mieux déterminer la façon d'implémenter un membre donné sur une interface d'extensibilité de fournisseur. La séquence d'appel réelle peut varier en fonction des fonctionnalités renvoyées par la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) . Voici des exemples de fonctionnalités: 
  
- Prise en charge du fournisseur pour l'obtention, la mise en cache ou la recherche dynamique des amis et des activités à partir du réseau social.
    
- Interface utilisateur que OSC doit afficher pour l'ouverture de session de l'utilisateur.
    
- Le type d'authentification (par exemple, l'authentification basée sur les formulaires) que le OSC doit utiliser.
    
## <a name="in-this-section"></a>Contenu de cette section

- [Authentification de base](basic-authentication.md): décrit la séquence d'appel classique du OSC afin de prendre en charge un utilisateur Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l'authentification de base.
    
- [Authentification basée sur les formulaires](forms-based-authentication.md): décrit la séquence d'appel classique du OSC afin de prendre en charge un utilisateur Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l'authentification basée sur les formulaires.
    
- [Obtenir des activités](getting-activities.md): décrit la séquence d'appel classique du OSC afin de synchroniser les activités des amis d'un utilisateur Office à partir d'un réseau social, si le fournisseur du réseau social OSC prend en charge la synchronisation des activités.
    
- [Obtenir des informations sur les amis](getting-friends-information.md): décrit la séquence d'appel par défaut du OSC pour synchroniser la liste des amis de l'utilisateur Office à partir d'un réseau social, si le fournisseur du réseau social OSC prend en charge la synchronisation mise en cache des contacts.
    
## <a name="reference"></a>Référence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections connexes

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  
- [Meilleures pratiques pour le développement d'un fournisseur](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)

