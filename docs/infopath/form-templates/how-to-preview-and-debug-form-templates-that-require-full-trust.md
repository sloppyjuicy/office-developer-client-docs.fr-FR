---
title: Aperçu et débogage des modèles de formulaires qui nécessitent une confiance totale
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
ms.localizationpriority: medium
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Par défaut, si vous tentez de déboguer ou d'afficher un projet avec du code managé dont le code appelle un membre de modèle objet qui nécessite une confiance totale, comme la propriété LoginName qui doit accéder aux informations sur le domaine de connexion de l'utilisateur, Microsoft InfoPath affiche les messages d'erreurs suivants.
ms.openlocfilehash: 8fef3f0fceb1c9637cc4fbeb59bc8d716db442d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605567"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Aperçu et débogage des modèles de formulaires qui nécessitent une confiance totale

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
    
Une fois cette procédure effectuée, vous pouvez déboguer votre projet comme décrit dans l’aperçu et déboguer les modèles de formulaire [InfoPath avec code.](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
> [!NOTE]
> [!REMARQUE] Pour réussir le déploiement d'un modèle de formulaire avec code managé qui requiert une confiance totale, vous devez effectuer quelques étapes supplémentaires, notamment la signature numérique, ou l'installation et l'enregistrement du modèle de formulaire. Pour plus d’informations sur le déploiement d’un modèle de formulaire avec code géré après avoir été déboché, voir Déployer des modèles de formulaire [InfoPath avec code.](how-to-deploy-infopath-form-templates-with-code.md) 
  
## <a name="see-also"></a>Voir aussi



[Afficher un aperçu et déboguer des modèles de formulaires InfoPath avec code](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Déployer des modèles de formulaire InfoPath avec code](how-to-deploy-infopath-form-templates-with-code.md)

