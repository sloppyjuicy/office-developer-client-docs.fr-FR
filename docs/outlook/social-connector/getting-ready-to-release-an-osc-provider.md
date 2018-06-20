---
title: Prise en main de publication d’un fournisseur OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Cette section propose des tests, que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787584"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Prise en main de publication d’un fournisseur OSC

Cette section propose des tests, que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC). Vous pouvez démarrer la référence pour les rubriques de cette section et procéder à certains de ces tests pendant le développement et les phases de test, mais vous devez avoir effectué ces tests au moment où que vous relâchez. 

Ces tests vérifient les fonctionnalités de base de votre implémentation des interfaces de fournisseur OSC en ce qui concerne les fonctionnalités que vous spécifiez pour le fournisseur OSC. En outre, même si l’OSC est une fonctionnalité partagée par plusieurs applications clientes d’Office, ces tests utilisent Outlook comme client pour tester la fonctionnalité fondamentale. Vous devez déterminer si les autres tests sont nécessaires pour les fonctionnalités spécifiques à votre fournisseur.
  
## <a name="in-this-section"></a>Dans cette section

- [Test du déploiement](testing-deployment.md): décrit les scénarios, vous devez tester autour de l’installation et de désinstallation d’un fournisseur OSC.
    
- [Test des fonctionnalités, l’authentification et la Configuration](testing-capabilities-authentication-and-configuration.md): description des tests pour obtenir les fonctionnalités et les scénarios de configuration d’un compte et l’authentification d’un utilisateur pour un réseau social.
    
- [Personnes Stop-suivantes et les tests suivants](testing-following-and-stop-following-persons.md): décrit les scénarios pour tester la capacité du fournisseur OSC pour ajouter une personne comme un ami, ou pour supprimer un ami à partir du réseau social. 
    
- [Test des amis](testing-friends.md): décrit les scénarios pour vérifier que le fournisseur OSC renvoie correctement les données des amis et non-amis, le cas échéant, selon le mode de synchronisation que le fournisseur prend en charge et les tests.
    
- [Activités de test](testing-activities.md): décrit les scénarios pour vérifier que le fournisseur OSC renvoie correctement les activités des amis et non-amis, le cas échéant, selon le mode de synchronisation que le fournisseur prend en charge et les tests.
    
## <a name="reference"></a>R�f�rence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections associées

- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)
  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  

