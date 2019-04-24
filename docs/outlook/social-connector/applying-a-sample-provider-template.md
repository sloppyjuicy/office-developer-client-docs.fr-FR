---
title: Application d'un exemple de modèle de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: "Les modèles de fournisseurs Outlook Social Connector (OSC) vous permettent d'implémenter un fournisseur OSC. "
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281126"
---
# <a name="applying-a-sample-provider-template"></a>Application d'un exemple de modèle de fournisseur

Les modèles de fournisseurs Outlook Social Connector (OSC) vous permettent d'implémenter un fournisseur OSC. Les modèles de fournisseur sont disponibles en C++, C# et Visual Basic. Ces modèles ne constituent qu'un point de départ pour le développement de votre fournisseur; les modèles ne traitent pas de l'écriture du code d'implémentation pour le fournisseur et de la création d'un package de configuration pour le fournisseur. La procédure suivante montre comment appliquer un modèle de fournisseur OSC lorsque vous commencez à développer un fournisseur.
  
### <a name="to-apply-an-osc-provider-template"></a>Pour appliquer un modèle de fournisseur OSC

1. Dans le menu **Démarrer** , cliquez avec le bouton droit sur **Microsoft Visual Studio 2010** , puis cliquez sur la commande **exécuter en tant qu'administrateur** . Lorsque vous y êtes invité, cliquez sur **Oui** pour exécuter Visual Studio en tant qu'administrateur. 
    
2. Remplacez le nom du projet et l'espace de noms dans le modèle par le nom de votre projet et les identificateurs d'espace de noms.
    
3. Modifiez la classe **AssemblyInfo** pour spécifier les informations d'assembly appropriées. 
    
4. Implémentez les membres d'interface marqués comme **to-do** et ajoutez des dépendances et des références supplémentaires, selon les besoins. 
    
5. Créez le projet.
    
6. Assurez-vous que le ProgID d'assembly du fournisseur `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`est affiché sous la forme d'une clé sous.
    
7. Pour distribuer le projet d'installation, créez un projet de configuration dans Visual Studio ou un outil de configuration de votre choix.
    
8. Votre projet de configuration doit terminer l'inscription COM pour votre assembly et créer la clé ProgID comme décrit à l'étape 5.
    
## <a name="see-also"></a>Voir aussi

- [Téléchargement des exemples](downloading-the-samples.md)
- [Exemples de modèles de OSC](osc-sample-templates.md)

