---
title: Étapes rapides pour apprendre à développer un fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Cette rubrique propose quelques étapes pour vous familiariser avec le développement d'un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424216"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Étapes rapides pour apprendre à développer un fournisseur

Pour développer un fournisseur OSC, vous devez effectuer les étapes générales suivantes:
  
- Implémentez les quatre interfaces obligatoires: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)et [ISocialPerson](isocialpersoniunknown.md). En fonction de la prise en charge de votre réseau social concernant la mise en cache des informations d'identification de connexion, le suivi d'une personne sur le réseau social ou la synchronisation dynamique des amis et de leurs activités, vous pouvez implémenter l'interface [ISocialSession2](isocialsession2iunknown.md) . 
    
- Parallèlement aux interfaces d'implémentation, testez et déboguez le fournisseur OSC. 

- Déployez le fournisseur OSC.  

- Effectuer les tests finaux avant la publication.
    
## <a name="step-a-implementing-interfaces"></a>Étape A: implémentation d'interfaces

Un fournisseur OSC implémente des interfaces afin que le OSC puisse utiliser ces interfaces pour obtenir les informations nécessaires concernant ou à partir du réseau social, via le fournisseur OSC. Ces informations incluent les éléments suivants:
  
- Présenter la boîte de dialogue de connexion à un utilisateur.    
- Si le fournisseur prend en charge l'affichage des amis ou des activités tel qu'il est affiché sur le réseau social.    
- Comment afficher des amis et des activités dans la carte de visite ou dans le volet de contacts Outlook.     
- Quand actualiser les informations des amis ou des activités sur la carte de visite ou le volet des personnes.
    
Les informations sont généralement transmises du fournisseur au OSC, sous la forme de chaînes XML, en tant que paramètres de sortie des méthodes d'interface. Les fournisseurs OSC et OSC sont conformes au schéma XML du fournisseur OSC. Par conséquent, dans le cadre de l'implémentation des interfaces, vous avez besoin d'une bonne compréhension de la façon dont le schéma XML vous permet de spécifier des informations comme indiqué ci-dessus. 

Les ressources suivantes expliquent comment spécifier le code XML pour les fonctionnalités, les amis et les activités du fournisseur:
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)    
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)    
- [Exemple de XML de fonctionnalités](capabilities-xml-example.md)   
- [XML pour les fonctionnalités](xml-for-capabilities.md)    
- [Exemple de code XML pour les amis](friends-xml-example.md)    
- [XML pour les amis](xml-for-friends.md)   
- [Exemple de XML d'informations sur les activités](activity-feed-xml-example.md)   
- [XML pour les activités](xml-for-activities.md)
    
Avant de commencer l'implémentation, consultez les rubriques suivantes pour gagner du temps lors du processus de débogage:
  
- [Exigences techniques](technical-requirements.md)    
- [Meilleures pratiques pour le développement d'un fournisseur](best-practices-for-developing-a-provider.md)    
- [Exemples de modèles de OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Étape B: débogage

Le débogage d' [un fournisseur](debugging-a-provider.md) suggère des procédures de débogage que vous pouvez utiliser lors du développement d'un fournisseur OSC. 
  
Lors du développement, vous pouvez également vous reporter à la préparation de la [publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md) pour mieux comprendre le comportement attendu dans certains scénarios (par exemple, l'authentification de base et l'authentification basée sur les formulaires). 
  
## <a name="step-c-deploying"></a>Étape C: déploiement

Consultez les rubriques suivantes pour en savoir plus sur les exigences en matière de déploiement:
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)    
- [Inscription d'un fournisseur](registering-a-provider.md)   
- [Liste de vérification de l'installation](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Étape D: test final avant la publication

En fonction de votre réseau social et du fournisseur OSC, il existe généralement des tests spécifiques au fournisseur que vous devez effectuer avant de libérer votre fournisseur. Pour obtenir une liste de tests suggérés, consultez la rubrique [préparation à la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Voir aussi

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

