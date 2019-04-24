---
title: Préparation de la publication d'un fournisseur OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Cette section propose des tests que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327152"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Préparation de la publication d'un fournisseur OSC

Cette section propose des tests que vous pouvez effectuer avant de libérer votre fournisseur Outlook Social Connector (OSC). Vous pouvez commencer à vous référer aux rubriques de cette section et effectuer certains de ces tests pendant les phases de développement et de test, mais vous devez avoir effectué ces tests au moment de la publication. 

Ces tests vérifient les fonctionnalités de base de votre implémentation des interfaces du fournisseur OSC en ce qui concerne les fonctionnalités que vous spécifiez pour le fournisseur OSC. Par ailleurs, même si OSC est une fonctionnalité partagée par plusieurs applications clientes Office, ces tests utilisent Outlook comme client pour tester les fonctionnalités fondamentales. Vous devez déterminer si d'autres tests sont nécessaires pour les fonctionnalités spécifiques à votre fournisseur.
  
## <a name="in-this-section"></a>Contenu de cette section

- [Test du déploiement](testing-deployment.md): décrit les scénarios que vous devez tester pour l'installation et la désinstallation d'un fournisseur OSC.
    
- [Test des fonctionnalités, de l'authentification et](testing-capabilities-authentication-and-configuration.md)de la configuration: décrit les tests permettant d'obtenir des fonctionnalités, ainsi que les scénarios de configuration d'un compte et d'authentification d'un utilisateur pour un réseau social.
    
- [Test suivi des personnes](testing-following-and-stop-following-persons.md)suivantes: décrit les scénarios permettant de tester la capacité du fournisseur OSC à ajouter une personne en tant qu'ami ou à supprimer un ami du réseau social. 
    
- [Test des amis](testing-friends.md): décrit les tests et les scénarios pour vérifier que le fournisseur OSC retourne correctement les données des amis et des non-amis, le cas échéant, en fonction du mode de synchronisation pris en charge par le fournisseur.
    
- [Activités de test](testing-activities.md): décrit les tests et les scénarios pour vérifier que le fournisseur OSC retourne correctement les activités des amis et des non-amis, le cas échéant, selon le mode de synchronisation pris en charge par le fournisseur.
    
## <a name="reference"></a>Référence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections connexes

- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)
  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  

