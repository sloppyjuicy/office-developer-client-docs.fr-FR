---
title: Afficher un aperçu et déboguer les modèles de formulaires nécessitant la confiance totale
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Par défaut, si vous tentez de déboguer ou d'afficher un projet avec du code managé dont le code appelle un membre de modèle objet qui nécessite une confiance totale, comme la propriété LoginName qui doit accéder aux informations sur le domaine de connexion de l'utilisateur, Microsoft InfoPath affiche les messages d'erreurs suivants.
ms.openlocfilehash: e9077b4ec0f8369b869e986020e4860f325fc023
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782356"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Afficher un aperçu et déboguer les modèles de formulaires nécessitant la confiance totale

Par défaut, si vous tentez de déboguer ou d'afficher un projet avec du code managé dont le code appelle un membre de modèle objet qui nécessite une confiance totale, comme la propriété **LoginName** qui doit accéder aux informations sur le domaine de connexion de l'utilisateur, Microsoft InfoPath affiche les messages d'erreurs suivants. 
  
En mode Aperçu :
  
« Une exception non prise en charge s'est produite dans le code du formulaire. », suivi du message d'erreur « InfoPath ne peut pas exécuter cette action en raison d'une erreur dans le code du formulaire."
  
En mode débogage :
  
L'affichage est ciblé sur la ligne de code dans l'éditeur de code qui appelle le membre requérant une confiance totale, et le message suivant s'affiche : « L'exception **SecurityException** n'a pas été gérée par le code utilisateur - Échec de la demande. » 
  
Pour permettre à la logique métier d'appeler ce membre lorsqu'il est en cours de débogage ou affiché en mode Aperçu, vous devez définir le niveau de sécurité **Confiance totale** pour votre formulaire, en suivant la procédure décrite ci-après. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Configuration d'un modèle de formulaire avec code managé qui requiert une confiance totale

### <a name="set-your-forms-security-level-to-full-trust"></a>Attribution du niveau de sécurité Confiance totale à un formulaire

1. Dans InfoPath, ouvrez le modèle de formulaire en mode Création.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sous l'onglet **Infos** tab. 
    
3. Dans la liste **Catégorie**, cliquez sur **Sécurité et approbation.**
    
4. Dans la section **Niveau de sécurité**, désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité**.
    
5. Sélectionnez **Confiance totale**, puis cliquez sur **OK**.
    
Une fois cette procédure effectuée, vous pouvez déboguer votre projet comme indiqué dans [l’Aperçu et déboguer des modèles de formulaire InfoPath avec Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).
  
> [!NOTE]
> [!REMARQUE] Pour réussir le déploiement d'un modèle de formulaire avec code managé qui requiert une confiance totale, vous devez effectuer quelques étapes supplémentaires, notamment la signature numérique, ou l'installation et l'enregistrement du modèle de formulaire. Pour plus d’informations sur le déploiement d’un modèle de formulaire avec code managé après avoir il débogué voir, [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md). 
  
## <a name="see-also"></a>Voir aussi



[Afficher un aperçu et déboguer les modèles de formulaire InfoPath avec Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md)

