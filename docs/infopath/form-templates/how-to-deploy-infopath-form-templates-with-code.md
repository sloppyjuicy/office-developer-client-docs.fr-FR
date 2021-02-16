---
title: Déployer des modèles de formulaire InfoPath avec code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- deploying form templates [infopath 2007],InfoPath 2007, deploying form templates,form templates [InfoPath 2007], deploying,.NET Framework security settings [InfoPath 2007],deployment [InfoPath 2007], form templates
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: Le code du formulaire d'un modèle de formulaire InfoPath avec code managé est compilé pour comment assembly exécuté dans Common Language Runtime (CLR). Chaque fois que vous devez modifier le code du formulaire, vous devez ouvrir le projet correspondant dans Visual Studio 2012, apporter les modifications dans l'éditeur de code, recompiler le modèle de formulaire, puis redéployer le modèle de formulaire. De plus, l'assembly privé étant exécuté dans le domaine d'une application hôte du CLR, les paramètres de sécurité des formulaires qui nécessitent une confiance totale diffèrent légèrement de ceux des modèles de formulaires qui ne nécessitent pas une confiance totale.
ms.openlocfilehash: ba3629e786a224ea950e78bbec9a9fe94d4499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406898"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Déployer des modèles de formulaire InfoPath avec code

Le code du formulaire d'un modèle de formulaire InfoPath avec code managé est compilé pour comment assembly exécuté dans Common Language Runtime (CLR). Chaque fois que vous devez modifier le code du formulaire, vous devez ouvrir le projet correspondant dans Visual Studio 2012, apporter les modifications dans l'éditeur de code, recompiler le modèle de formulaire, puis redéployer le modèle de formulaire. De plus, l'assembly privé étant exécuté dans le domaine d'une application hôte du CLR, les paramètres de sécurité des formulaires qui nécessitent une confiance totale diffèrent légèrement de ceux des modèles de formulaires qui ne nécessitent pas une confiance totale.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>Déploiement de modèles de formulaires ne nécessitant pas la confiance totale

Si le code de formulaire de votre modèle de formulaire n'utilise pas de membres du modèle objet InfoPath qui nécessitent la confiance totale et que le modèle de formulaire n'utilise pas de fonctionnalités qui nécessitent la confiance totale, vous pouvez publier votre modèle de formulaire directement dans InfoPath à l'aide de la procédure qui suit. Pour plus d’informations sur le modèle de sécurité InfoPath, voir À propos du modèle de sécurité pour les [modèles de formulaires avec code.](about-the-security-model-for-form-templates-with-code.md)
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Déploiement d'un modèle de formulaire ne nécessitant pas la confiance totale

1. Créez et déboguez le modèle de formulaire dans Visual Studio 2012.
    
2. Si vous utilisez l'éditeur de code Visual Studio 2012, accédez à InfoPath, cliquez sur l'onglet **Fichier**, puis cliquez sur le bouton correspondant à l'emplacement souhaité sous l'onglet **Publier** (Si vous avez déjà publié le modèle de formulaire, vous pouvez cliquer sur l'onglet **Fichier**, puis sur **Publication rapide** pour republier le modèle de formulaire au même emplacement). 
    
    Le modèle de formulaire est compilé et l' **Assistant Publication** démarre. Suivez les étapes de l' **Assistant Publication** pour déployer le formulaire à l'emplacement de votre choix. Pour plus d'informations sur l'utilisation de l' **Assistant Publication**, recherchez « Publication d'un modèle de formulaire » dans l'aide d'InfoPath.
    
## <a name="deploying-form-templates-that-require-full-trust"></a>Déploiement de modèles de formulaires nécessitant la confiance totale

Si le code du formulaire de votre modèle de formulaire n'utilise pas de membres de modèle objet InfoPath nécessitant une confiance totale ou si le modèle de formulaire utilise des fonctionnalités nécessitant une confiance totale, vous devez signer numériquement votre modèle de formulaire (.xsn) avec un certificat de signature de code provenant d'un éditeur approuvé, auquel les utilisateurs de votre formulaire devront accorder leur confiance lors de l'ouverture. Ceci accorde également la confiance totale à votre formulaire et accorde du même coup le jeu d'autorisations FullTrust au code de votre formulaire.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Compilation, publication et signature numérique d'un modèle de formulaire

1. Créez et déboguez votre modèle de formulaire dans Visual Studio 2012.
    
2. Si vous utilisez l'éditeur de code Visual Studio 2012, accédez à InfoPath, cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire**.
    
3. Cliquez sur la catégorie **Sécurité et approbation**. 
    
4. Sous **Niveau de sécurité**, désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité**, puis sélectionnez **Confiance totale**.
    
5. Sous **Signature du modèle de formulaire**, sélectionnez **Signer ce modèle de formulaire**, cliquez sur **Sélectionner un certificat**, puis spécifiez le certificat de signature de code avec lequel le modèle de formulaire doit être signé.
    
6. Cliquez deux fois sur **OK** pour fermer la boîte de dialogue **Options de formulaire**, puis enregistrez vos modifications. 
    
7. Cliquez sur l'onglet **Publier**, puis cliquez sur le bouton correspondant à la publication souhaitée. 
    
8. Le modèle de formulaire est compilé et l' **Assistant Publication** démarre. Suivez les étapes dans l' **Assistant Publication** pour déployer votre modèle de formulaire. Pour plus d'informations sur l'utilisation de l' **Assistant Publication** afin de déployer un modèle de formulaire nécessitant une confiance totale, recherchez la rubrique « Publication d'un modèle de formulaire avec confiance totale » dans l'aide d'InfoPath. 
    
 **Remarques**
- Pour signer numériquement un formulaire, vous devez disposer d'un certificat de signature de code authentifié sur votre ordinateur. Pour acquérir un tel certificat, vous devez contacter une autorité de certification ou votre administrateur réseau.
    
- Si vous devez effectuer des modifications dans le formulaire après sa publication, vous devez répéter la procédure et resigner le modèle de formulaire. Ceci est dû au fait que la modification du formulaire annule la validité de la signature. Lors du développement d’un formulaire nécessitant des autorisations de confiance totale, vous pouvez utiliser la procédure décrite dans les modèles de [formulaires](how-to-preview-and-debug-form-templates-that-require-full-trust.md) d’aperçu et de débogage qui nécessitent une autorisation totale pour inscrire le modèle de formulaire sur votre ordinateur local. 
    
## <a name="configuring-net-framework-security-settings"></a>Configuration des paramètres de sécurité .NET Framework

Pour plus de contrôle sur les autorisations accordées au code managé exécuté dans un modèle de formulaire InfoPath avec code managé, vous pouvez utiliser l'utilitaire de configuration de .NET Framework 2.0 pour appliquer un jeu d'autorisations spécifique à votre code de formulaire.
  
> [!IMPORTANT]
> [!IMPORTANTE] La configuration des paramètres de sécurité de .NET Framework pour un modèle de formulaire InfoPath avec code managé n'a pas d'influence sur le fait que les membres du modèle objet InfoPath qui nécessitent une confiance totale sont autorisés à s'exécuter ou non. Vous devez soit signer numériquement, soit inscrire le modèle de formulaire comme décrit précédemment dans cette rubrique pour permettre les appels aux membres du modèle objet InfoPath qui nécessitent une confiance totale. La configuration des paramètres de sécurité de .NET Framework s'applique uniquement aux appels aux membres des classes .NET Framework et aux composants managés autres que le modèle objet InfoPath. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Compilation, publication et configuration des paramètres de sécurité .NET d'un modèle de formulaire

1. Créez et déboguez le modèle de formulaire dans Visual Studio 2012.
    
2. Si vous utilisez l'éditeur de code Visual Studio 2012, accédez à InfoPath, cliquez sur l'onglet **Fichier**, cliquez sur **Publier**, puis cliquez sur le bouton correspond à l'emplacement de publication souhaité.
    
    Le modèle de formulaire est compilé et l' **Assistant Publication** démarre. Suivez les étapes dans l' **Assistant Publication** pour déployer votre formulaire. Pour plus d'informations sur l'utilisation de l' **Assistant Publication**, recherchez « Publication d'un modèle de formulaire » dans l'aide d'InfoPath.
    
3. Effectuez la procédure décrite dans la section « Affectation d’une confiance totale à des formulaires à une URL ou à une UNC spécifique » de la section Configurer les paramètres de sécurité pour les modèles de [formulaires](how-to-configure-security-settings-for-form-templates-with-code.md) avec code
    
## <a name="see-also"></a>Voir aussi

#### <a name="tasks"></a>Tâches

[Configurer les paramètres de sécurité pour les modèles de formulaires avec code](how-to-configure-security-settings-for-form-templates-with-code.md)


[À propos du modèle de sécurité pour les modèles de formulaires avec code](about-the-security-model-for-form-templates-with-code.md)
  
[Afficher un aperçu et déboguer des modèles de formulaire exigeant l'autorisation totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

