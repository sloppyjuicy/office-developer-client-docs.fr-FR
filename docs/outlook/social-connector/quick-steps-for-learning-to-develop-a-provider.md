---
title: Étapes rapides pour apprendre à développer un fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Cette rubrique suggère quelques étapes pour en savoir plus sur le développement d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 3dbb4e40a3cfe3d2b37c7b2fb9ef60515640adc6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629059"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Étapes rapides pour apprendre à développer un fournisseur

Pour développer un fournisseur OSC, vous devez effectuer les étapes générales suivantes :
  
- Implémenter les quatre interfaces obligatoires : [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)et [ISocialPerson](isocialpersoniunknown.md). Selon la prise en charge de votre réseau social pour la mise en cache des informations d’identification de connexion, le suivi d’une personne sur le réseau social ou la synchronisation dynamique des amis et de leurs activités, vous pouvez implémenter l’interface [ISocialSession2.](isocialsession2iunknown.md) 
    
- Parallèlement à l’implémentation d’interfaces, testez et déboguer le fournisseur OSC. 

- Déployez le fournisseur OSC.  

- Test final avant publication.
    
## <a name="step-a-implementing-interfaces"></a>Étape A : Mise en œuvre d’interfaces

Un fournisseur OSC implémente des interfaces afin que l’OSC puisse utiliser ces interfaces pour obtenir les informations nécessaires sur le réseau social ou à partir de celui-ci, via le fournisseur OSC. Ces informations sont les suivantes :
  
- Présentation de la boîte de dialogue d’accès au compte à un utilisateur.    
- Indique si le fournisseur prend en charge l’affichage d’amis ou d’activités tels qu’ils sont affichés sur le réseau social.    
- Comment afficher des amis et des activités dans la carte de visite ou Outlook volet Contacts.     
- Quand actualiser les informations d’amis ou d’activités sur la carte de visite ou le volet Contacts.
    
Les informations sont généralement transmises du fournisseur à OSC, sous la forme de chaînes XML en tant que paramètres de sortie des méthodes d’interface. OsC et un fournisseur OSC sont conformes au schéma XML du fournisseur OSC. Par conséquent, au cours de l’implémentation des interfaces, vous devez bien comprendre comment le schéma XML vous permet de spécifier des informations telles que répertoriées ci-dessus. 

Les ressources suivantes expliquent comment spécifier du XML pour les fonctionnalités du fournisseur, les amis et les activités :
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)    
- [Synchronisation des amis et des activités](synchronizing-friends-and-activities.md)    
- [Exemple de fonctionnalités XML](capabilities-xml-example.md)   
- [XML pour les fonctionnalités](xml-for-capabilities.md)    
- [Exemple XML Friends](friends-xml-example.md)    
- [XML pour les amis](xml-for-friends.md)   
- [Exemple de XML de flux d’activités](activity-feed-xml-example.md)   
- [XML pour les activités](xml-for-activities.md)
    
Avant de commencer l’implémentation, consultez également les rubriques suivantes pour gagner du temps plus tard dans le processus de débogage :
  
- [Conditions techniques requises](technical-requirements.md)    
- [Meilleures pratiques pour le développement d’un fournisseur](best-practices-for-developing-a-provider.md)    
- [Exemples de modèles de OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Étape B : Débogage

La rubrique [Débogage d’un](debugging-a-provider.md) fournisseur suggère des procédures de débogage que vous pouvez utiliser lors du développement d’un fournisseur OSC. 
  
Pendant le développement, vous pouvez également vous référer à [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) pour mieux comprendre le comportement attendu dans certains scénarios (par exemple, l’authentification de base et basée sur les formulaires). 
  
## <a name="step-c-deploying"></a>Étape C : Déploiement

Consultez les rubriques suivantes pour en savoir plus sur les exigences de déploiement :
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)    
- [Inscription d’un fournisseur](registering-a-provider.md)   
- [Liste de vérification de l’installation](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Étape D : Test final avant publication

En fonction de votre réseau social et du fournisseur OSC, il existe généralement des tests spécifiques au fournisseur que vous devez effectuer avant de libérer votre fournisseur. Pour obtenir la liste des tests suggérés, voir Préparation à la publication [d’un fournisseur OSC.](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a>Voir aussi

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

