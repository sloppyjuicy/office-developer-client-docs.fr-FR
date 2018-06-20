---
title: Étapes rapides pour apprendre à développer un fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Cette rubrique suggère quelques étapes pour en savoir plus sur le développement d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787704"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Étapes rapides pour apprendre à développer un fournisseur

Pour développer un fournisseur OSC, vous devez effectuer les étapes générales suivantes :
  
- Implémenter les interfaces obligatoires quatre : [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)et [ISocialPerson](isocialpersoniunknown.md). En fonction de la prise en charge de votre réseau social pour la mise en cache des informations d’identification d’ouverture de session, suivi d’une personne sur le réseau social, ou dynamiquement synchronisation amis et leurs activités, vous souhaiterez mettre en œuvre l’interface [ISocialSession2](isocialsession2iunknown.md) . 
    
- Parallèlement à implémenter des interfaces, tester et déboguer le fournisseur OSC. 

- Déployer le fournisseur OSC.  

- Effectuer un test final avant le lancement.
    
## <a name="step-a-implementing-interfaces"></a>Étape a : implémenter des interfaces

Un fournisseur OSC implémente des interfaces afin que le OSC permettre utiliser ces interfaces pour obtenir les informations nécessaires sur ou à partir du réseau social, via le fournisseur OSC. Ces informations sont les suivantes :
  
- Comment présenter la boîte de dialogue compte d’ouverture de session à un utilisateur.    
- Si le fournisseur prend en charge affichant amis ou activités telle qu’elle apparaît sur le réseau social.    
- Mode d’affichage des amis et des activités dans la carte de visite ou le volet personnes.     
- Heure d’actualiser des amis ou des activités d’informations sur la carte de visite ou le volet personnes.
    
Les informations sont généralement passées à partir du fournisseur à l’OSC, sous la forme de chaînes XML en tant que paramètres de sortie de méthodes d’interface. À la fois l’OSC et un fournisseur OSC respectent le schéma XML du fournisseur OSC. Par conséquent, au cours de l’implémentation des interfaces, vous devez bien comprendre comment le schéma XML permet de spécifier les informations comme indiqué ci-dessus. 

Les ressources suivantes expliquent comment spécifier le code XML pour les activités, amis et des fonctionnalités du fournisseur :
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)    
- [Synchronisation de vos amis et activités](synchronizing-friends-and-activities.md)    
- [Exemple de code XML des fonctionnalités](capabilities-xml-example.md)   
- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)    
- [Exemple de code XML amis](friends-xml-example.md)    
- [Code XML des amis](xml-for-friends.md)   
- [Exemple de flux XML d’activité](activity-feed-xml-example.md)   
- [XML pour les activités](xml-for-activities.md)
    
Avant de commencer la mise en œuvre, consultez également les rubriques suivantes pour gagner du temps plus loin dans le processus de débogage :
  
- [Conditions techniques](technical-requirements.md)    
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)    
- [Exemples de modèles de OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Étape b : débogage

La rubrique [débogage d’un fournisseur](debugging-a-provider.md) suggère les procédures que vous pouvez utiliser lors du développement d’un fournisseur OSC de débogage. 
  
Lors du développement, vous pouvez également vous reporter à [Préparation pour la publication d’un fournisseur OSC](getting-ready-to-release-an-osc-provider.md) à mieux comprendre le comportement attendu dans certains scénarios (par exemple, l’authentification basée sur les formulaires et de base). 
  
## <a name="step-c-deploying"></a>Étape c : déploiement

Voir les rubriques suivantes pour en savoir plus sur les exigences de déploiement :
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)    
- [Inscription d’un fournisseur](registering-a-provider.md)   
- [Aide-mémoire d’installation](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Étape d : Final test avant la publication

En fonction de votre réseau social et le fournisseur OSC, il existe des tests généralement spécifiques au fournisseur que vous devez effectuer avant de libérer votre fournisseur. Pour une liste de suggestion de tests, voir [Préparation pour la publication d’un fournisseur OSC](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Voir aussi

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

