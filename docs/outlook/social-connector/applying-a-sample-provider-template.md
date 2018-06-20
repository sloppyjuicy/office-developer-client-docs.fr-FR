---
title: Appliquer un modèle de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Les exemples de modèles de fournisseur Outlook Social Connector (OSC) vous fournissent une infrastructure pour l’implémentation d’un fournisseur OSC. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787569"
---
# <a name="applying-a-sample-provider-template"></a>Appliquer un modèle de fournisseur

Les exemples de modèles de fournisseur Outlook Social Connector (OSC) vous fournissent une infrastructure pour l’implémentation d’un fournisseur OSC. Les modèles du fournisseur sont disponibles en C++, Visual C# et Visual Basic. Ces modèles sont simplement un point de départ pour le développement de votre fournisseur ; les modèles ne répondent pas écrire le code d’implémentation pour le fournisseur et la création d’un package d’installation pour le fournisseur. La procédure suivante montre comment appliquer un modèle de fournisseur OSC lorsque vous commencez à développer un fournisseur.
  
### <a name="to-apply-an-osc-provider-template"></a>Pour appliquer un modèle de fournisseur OSC

1. Dans le menu **Démarrer** , cliquez sur **Microsoft Visual Studio 2010** , cliquez sur la commande **Exécuter en tant qu’administrateur** . Lorsque vous y êtes invité, cliquez sur **Oui** pour exécuter Visual Studio en tant qu’administrateur. 
    
2. Remplacez le nom du projet et l’espace de noms dans le modèle de votre nom et l’espace de noms des identificateurs de projet.
    
3. Modifiez la classe **AssemblyInfo** pour spécifier les informations d’assembly approprié. 
    
4. Implémenter les membres de l’interface marqués comme étant **des tâches** et ajoutez les autres dépendances et les références, selon les besoins. 
    
5. Générez le projet.
    
6. Assurez-vous que l’assembly du fournisseur ProgID est répertorié en tant que clé sous `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
7. Pour distribuer le projet d’installation, créez un projet d’installation dans Visual Studio ou un outil de configuration de votre choix.
    
8. Votre projet d’installation doit effectuer l’enregistrement COM pour l’assembly et créer la clé ProgID comme indiqué à l’étape 5.
    
## <a name="see-also"></a>Voir aussi

- [Téléchargement d’exemples](downloading-the-samples.md)
- [Exemples de modèles de OSC](osc-sample-templates.md)

