---
title: Séquences d’appel classiques OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: Cette section décrit les séquences d’appel par défaut Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité de fournisseur OSC, qui implémente un fournisseur OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787697"
---
# <a name="osc-typical-calling-sequences"></a>Séquences d’appel classiques OSC

Cette section décrit les séquences d’appel par défaut Outlook Social Connector (OSC) des membres dans les interfaces d’extensibilité de fournisseur OSC, qui implémente un fournisseur OSC. Les séquences d’appel classiques illustrent comment et quand l’OSC utilise ces interfaces et méthodes, pour vous permettre de mieux déterminent comment mettre en œuvre un membre donné sur une interface d’extensibilité de fournisseur. La séquence d’appel réelle peut varier selon les fonctionnalités renvoyées par la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) . Exemples de fonctionnalités sont les suivantes : 
  
- Fournisseur prend en charge pour l’obtention, la mise en cache ou recherchez dynamiquement des amis et des activités à partir du réseau social.
    
- L’interface utilisateur qui doit s’afficher l’OSC pour l’ouverture de session.
    
- Le type d’authentification (par exemple, l’authentification par formulaire) que l’OSC doit utiliser.
    
## <a name="in-this-section"></a>Dans cette section

- [L’authentification de base](basic-authentication.md): décrit la séquence d’appel par défaut de l’OSC pour prendre en charge d’un utilisateur d’Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification de base.
    
- [L’authentification basée sur les formulaires](forms-based-authentication.md): décrit la séquence d’appel par défaut de l’OSC pour prendre en charge d’un utilisateur d’Office qui se connecte à un réseau social, si le fournisseur OSC prend en charge l’authentification basée sur les formulaires.
    
- [Obtention des activités](getting-activities.md): décrit la séquence d’appel par défaut de l’OSC pour synchroniser les activités de vos amis de l’utilisateur d’Office à partir d’un réseau social, si le fournisseur OSC de réseau social prend en charge la synchronisation des activités.
    
- [Obtention d’informations sur des amis](getting-friends-information.md): décrit la séquence d’appel par défaut de l’OSC de synchroniser la liste d’amis de l’utilisateur d’Office à partir d’un réseau social, si le fournisseur OSC de réseau social prend en charge la mise en cache la synchronisation des contacts.
    
## <a name="reference"></a>R�f�rence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections associées

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Voir aussi

- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)

