---
title: Préparation à la publication d’un fournisseur OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Cette section suggère des tests que vous pouvez faire avant de libérer votre fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 32fe16dacb0af5b42b6884de1982452076d5615f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629185"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Préparation à la publication d’un fournisseur OSC

Cette section suggère des tests que vous pouvez faire avant de libérer votre fournisseur Outlook Social Connector (OSC). Vous pouvez commencer à faire référence aux rubriques de cette section et effectuer certains de ces tests au cours de vos phases de développement et de test, mais vous devriez avoir effectué ces tests au moment de la publication. 

Ces tests vérifient les fonctionnalités de base de votre implémentation des interfaces du fournisseur OSC par rapport aux fonctionnalités que vous spécifiez pour le fournisseur OSC. En outre, même si OSC est une fonctionnalité partagée par plusieurs applications clientes Office, ces tests utilisent Outlook comme client pour tester les fonctionnalités fondamentales. Vous devez déterminer si d’autres tests sont nécessaires pour les fonctionnalités spécifiques à votre fournisseur.
  
## <a name="in-this-section"></a>Dans cette section

- [Test du](testing-deployment.md)déploiement : décrit les scénarios que vous devez tester autour de l’installation et de la désinstallation d’un fournisseur OSC.
    
- [Test des fonctionnalités,](testing-capabilities-authentication-and-configuration.md)de l’authentification et de la configuration : décrit les tests d’obtention des fonctionnalités et les scénarios de configuration d’un compte et d’authentification d’un utilisateur pour un réseau social.
    
- [Test des](testing-following-and-stop-following-persons.md)personnes Stop-Following suivantes : décrit les scénarios pour tester la capacité du fournisseur OSC à ajouter une personne en tant qu’ami ou à supprimer un ami du réseau social. 
    
- [Testing Friends](testing-friends.md): décrit les tests et les scénarios pour vérifier que le fournisseur OSC renvoie correctement les données d’amis et de non-amis, le cas échéant, en fonction du mode de synchronisation qu’il prend en charge.
    
- [Activités de](testing-activities.md)test : décrit les tests et les scénarios pour vérifier que le fournisseur OSC renvoie correctement les activités d’amis et de non-amis, le cas échéant, en fonction du mode de synchronisation qu’il prend en charge.
    
## <a name="reference"></a>Référence

- [Documentation de référence sur le fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Sections connexes

- [Exemples de modèles de OSC](osc-sample-templates.md)
  
- [Séquences d'appels classiques OSC](osc-typical-calling-sequences.md)
  
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Débogage d'un fournisseur](debugging-a-provider.md)
  
- [Déploiement d'un fournisseur](deploying-a-provider.md)
  

