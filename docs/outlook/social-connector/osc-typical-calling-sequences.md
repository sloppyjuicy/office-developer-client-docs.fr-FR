---
title: Séquences d’appels classiques OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Cette section décrit les séquences d’appels classiques Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité du fournisseur OSC, qu’un fournisseur OSC implémente.
ms.openlocfilehash: 5106bc31cab1854cba07d5188a5888ea5f382d50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566177"
---
# <a name="osc-typical-calling-sequences"></a>Séquences d’appels classiques OSC

Cette section décrit les séquences d’appels classiques Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité du fournisseur OSC, qu’un fournisseur OSC implémente. Les séquences d’appels classiques illustrent comment et quand OSC utilise ces interfaces et méthodes, pour vous aider à mieux déterminer comment implémenter un membre donné sur une interface d’extensibilité de fournisseur. La séquence d’appels réelle peut varier en fonction des fonctionnalités renvoyées par la méthode [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md) Voici quelques exemples de fonctionnalités : 
  
- Prise en charge par les fournisseurs pour l’obtention, la mise en cache ou la recherche dynamique d’amis et d’activités à partir du réseau social.
    
- Interface utilisateur que l’OSC doit afficher pour l’utilisateur.
    
- Type d’authentification (par exemple, authentification basée sur les formulaires) que l’OSC doit utiliser.
    
## <a name="in-this-section"></a>Dans cette section

- [Authentification](basic-authentication.md)de base : décrit la séquence d’appels classique de l’OSC pour prendre en charge un utilisateur Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification de base.
    
- [](forms-based-authentication.md)Authentification basée sur les formulaires : décrit la séquence d’appels classique de l’OSC pour prendre en charge un utilisateur Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification basée sur les formulaires.
    
- [Obtention](getting-activities.md)d’activités : décrit la séquence d’appels classique de l’OSC pour synchroniser les activités des amis de l’utilisateur Office à partir d’un réseau social, si le fournisseur OSC du réseau social prend en charge la synchronisation des activités.
    
- [Obtention d’informations](getting-friends-information.md)sur les amis : décrit la séquence d’appels classique de l’OSC pour synchroniser la liste des amis de l’utilisateur Office à partir d’un réseau social, si le fournisseur OSC du réseau social prend en charge la synchronisation des contacts mise en cache.
    
## <a name="reference"></a>Référence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections connexes

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Voir aussi

- [XML pour les fonctionnalités](xml-for-capabilities.md)

