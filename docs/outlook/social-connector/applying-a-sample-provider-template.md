---
title: Application d’un exemple de modèle de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Les exemples Outlook de fournisseurs OSC (Social Connector) vous donnent une infrastructure pour l’implémentation d’un fournisseur OSC. '
ms.openlocfilehash: bb2262d993163afc2fb5a8260d09de2b91bbd9dc
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381956"
---
# <a name="applying-a-sample-provider-template"></a>Application d’un exemple de modèle de fournisseur

Les exemples Outlook de fournisseurs OSC (Social Connector) vous donnent une infrastructure pour l’implémentation d’un fournisseur OSC. Les modèles de fournisseur sont disponibles en C++, C# et Visual Basic. Ces modèles ne sont qu’un point de départ pour le développement de votre fournisseur . les modèles n’abordent pas l’écriture du code d’implémentation pour le fournisseur et la création d’un package d’installation pour le fournisseur. La procédure suivante montre comment appliquer un modèle de fournisseur OSC lorsque vous commencez à développer un fournisseur.
  
### <a name="to-apply-an-osc-provider-template"></a>Pour appliquer un modèle de fournisseur OSC

1. Dans **le menu** Démarrer, cliquez avec le bouton **droit Microsoft Visual Studio 2010** et cliquez sur la commande Exécuter **en tant qu’administrateur**. Lorsque vous y est invité, cliquez sur **Oui** pour exécuter Visual Studio en tant qu’administrateur.

2. Modifiez le nom et l’espace de noms du projet dans le modèle en identifiants de nom de projet et d’espace de noms.

3. Modifiez la **classe AssemblyInfo** pour spécifier les informations d’assembly appropriées.

4. Implémentez les membres d’interface **marqués comme To-Do** et ajoutez d’autres dépendances et références, selon les besoins.

5. Créez le projet.

6. Assurez-vous que le ProgID d’assembly du fournisseur est répertorié en tant que clé sous `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.

7. Pour distribuer le projet d’installation, créez un projet d’installation Visual Studio ou un outil d’installation de votre choix.

8. Votre projet d’installation doit terminer l’inscription COM pour votre assembly et également créer la clé ProgID comme répertorié à l’étape 5.

## <a name="see-also"></a>Voir aussi

- [Téléchargement des exemples](downloading-the-samples.md)
- [Exemples de modèles de OSC](osc-sample-templates.md)
