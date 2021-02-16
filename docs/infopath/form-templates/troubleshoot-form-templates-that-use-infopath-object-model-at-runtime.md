---
title: Résoudre les problèmes de modèles de formulaire qui utilisent le modèle objet InfoPath au moment de l’utilisation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- troubleshooting form templates [infopath 2007], run time,InfoPath 2003-compatible form templates, troubleshooting at run time
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: Les sections suivantes décrivent les scénarios de dépannage courants que vous pouvez rencontrer lors de l’utilisation de modèles de formulaire InfoPath avec code géré qui utilisent le modèle objet compatible InfoPath 2003 fourni par l’espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust au moment de l’utilisation.
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414444"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Résoudre les problèmes de modèles de formulaire qui utilisent le modèle objet InfoPath au moment de l’utilisation

Les sections suivantes décrivent les scénarios de dépannage courants que vous pouvez rencontrer lors de l’utilisation de modèles de formulaire InfoPath avec code géré qui utilisent le modèle objet compatible InfoPath 2003 fourni par l’espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** au moment de l’utilisation. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Afficher des notifications pour les exceptions de code géré non gérée au moment de l’exécuter

Si vous n'utilisez pas la gestion d'exceptions try-catch dans le code du formulaire, InfoPath affiche des informations sur les exceptions non gérées dans la boîte de dialogue d'erreurs d'InfoPath lors du débogage et de l'aperçu. Cependant, par défaut, les exceptions non gérées ne sont pas affichées dans la boîte de dialogue d'erreurs d'InfoPath lors de l'exécution lorsque vous déployez votre modèle de formulaire avec code managé. Si vous souhaitez que les exceptions de code mana gère s’affichent au moment de l’utilisation, suivez la procédure de la section « Gestion des exceptions de code mana gère » de La gestion des erreurs à l’aide du modèle objet [InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problèmes liés aux modèles de formulaires avec code géré après le déploiement

Testez votre modèle de formulaire avec code managé à l'emplacement de son déploiement. Pour plus d’informations sur les procédures de déploiement, voir Déployer des [modèles de formulaire InfoPath avec code.](how-to-deploy-infopath-form-templates-with-code.md) Pour plus d’informations sur les scénarios de sécurité qui affectent le déploiement, voir à propos du modèle de sécurité pour les [modèles de formulaires avec code.](about-the-security-model-for-form-templates-with-code.md)
  
Si vous utilisez l'utilitaire de configuration de .NET Framework 1.1 et le groupe de codes de modèles de formulaires InfoPath pour ajouter des autorisations spécifiques à un modèle de formulaire avec code managé, assurez-vous que la même stratégie de sécurité est déployée sur tous les ordinateurs clients. De même, si vous spécifiez un élément **URLEvidence** qui fait référence à un emplacement sur l'ordinateur local, assurez-vous que l'emplacement spécifié fait référence au dossier dans lequel la solution sera finalement déployée (emplacement différent de celui utilisé pendant le développement). Pour plus d’informations sur la configuration des paramètres de sécurité .NET Framework pour un modèle de formulaire avec code géré, voir la section « Affectation de la confiance totale aux formulaires à une URL spécifique ou UNC » de la rubrique Configurer les paramètres de sécurité des modèles de formulaires avec [code.](how-to-configure-security-settings-for-form-templates-with-code.md) 
  
## <a name="see-also"></a>Voir aussi

- [À propos du modèle de sécurité pour les modèles de formulaires avec code](about-the-security-model-for-form-templates-with-code.md)
- [Déployer des modèles de formulaire InfoPath avec code](how-to-deploy-infopath-form-templates-with-code.md)
- [Gérer les erreurs à l’aide du modèle objet InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Débogage de projets InfoPath à l’aide du modèle objet InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

