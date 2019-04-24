---
title: Résoudre les problèmes liés aux modèles de formulaires qui utilisent le modèle objet InfoPath au moment de l'exécution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- résolution des problèmes liés aux modèles de formulaires [InfoPath 2007], au moment de l'exécution, modèles de formulaires compatibles InfoPath 2003, résolution des problèmes au moment de l'exécution
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: Les sections suivantes décrivent les scénarios de résolution des problèmes courants que vous pouvez rencontrer lors de l'utilisation de modèles de formulaires InfoPath avec code managé qui utilisent le modèle objet compatible InfoPath 2003 fourni par Microsoft. Office. Interop. InfoPath. SemiTrust espace de noms au moment de l'exécution.
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299796"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Résoudre les problèmes liés aux modèles de formulaires qui utilisent le modèle objet InfoPath au moment de l'exécution

Les sections suivantes décrivent les scénarios de résolution des problèmes courants que vous pouvez rencontrer lors de l'utilisation de modèles de formulaires InfoPath avec code managé qui utilisent le modèle objet compatible InfoPath 2003 fourni par le ** Espace de noms Microsoft. Office. Interop. InfoPath. SemiTrust** au moment de l'exécution. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Afficher les notifications pour les exceptions de code managé non gérées au moment de l'exécution

Si vous n'utilisez pas la gestion d'exceptions try-catch dans le code du formulaire, InfoPath affiche des informations sur les exceptions non gérées dans la boîte de dialogue d'erreurs d'InfoPath lors du débogage et de l'aperçu. Cependant, par défaut, les exceptions non gérées ne sont pas affichées dans la boîte de dialogue d'erreurs d'InfoPath lors de l'exécution lorsque vous déployez votre modèle de formulaire avec code managé. Si vous souhaitez que les exceptions de code managé s'affichent au moment de l'exécution, suivez la procédure décrite dans la section «gestion des exceptions de code managé» des [Erreurs de gestion à l'aide du modèle objet InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problèmes liés aux modèles de formulaires avec code managé après déploiement

Testez votre modèle de formulaire avec code managé à l'emplacement de son déploiement. Pour plus d'informations sur les procédures de déploiement, consultez la rubrique [déployer des modèles de formulaire InfoPath avec code](how-to-deploy-infopath-form-templates-with-code.md). Pour plus d'informations sur les scénarios de sécurité qui affectent le déploiement, consultez [la rubrique relative au modèle de sécurité pour les modèles de formulaires avec code](about-the-security-model-for-form-templates-with-code.md).
  
Si vous utilisez l'utilitaire de configuration de .NET Framework 1.1 et le groupe de codes de modèles de formulaires InfoPath pour ajouter des autorisations spécifiques à un modèle de formulaire avec code managé, assurez-vous que la même stratégie de sécurité est déployée sur tous les ordinateurs clients. De même, si vous spécifiez un élément **URLEvidence** qui fait référence à un emplacement sur l'ordinateur local, assurez-vous que l'emplacement spécifié fait référence au dossier dans lequel la solution sera finalement déployée (emplacement différent de celui utilisé pendant le développement). Pour plus d'informations sur la configuration des paramètres de sécurité .NET Framework pour un modèle de formulaire avec code managé, voir la section «assignation de FullTrust à des formulaires dans une URL ou une UNC spécifique» de la rubrique [configurer les paramètres de sécurité pour les modèles de formulaires avec code](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>Voir aussi

- [À propos du modèle de sécurité pour les modèles de formulaire avec code](about-the-security-model-for-form-templates-with-code.md)
- [Déployer des modèles de formulaire InfoPath avec code](how-to-deploy-infopath-form-templates-with-code.md)
- [Gérer les erreurs à l'aide du modèle objet InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [DéBogage de projets InfoPath à l'aide du modèle objet InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

