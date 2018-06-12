---
title: Résoudre les problèmes des modèles de formulaires qui utilisent le modèle objet InfoPath au moment de l’exécution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- troubleshooting form templates [infopath 2007], run time,InfoPath 2003-compatible form templates, troubleshooting at run time
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: Les sections qui suivent décrivent les scénarios de dépannage courants que vous pouvez rencontrer lors de l'utilisation de modèles de formulaires InfoPath avec code managé, qui utilisent le modèle objet compatible InfoPath 2003 fourni par l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust lors de l'exécution.
ms.openlocfilehash: 8c83679a0cd61fae212b3143b6b0131da92ac7f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782468"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Résoudre les problèmes des modèles de formulaires qui utilisent le modèle objet InfoPath au moment de l’exécution

Les sections qui suivent décrivent les scénarios de dépannage courants que vous pouvez rencontrer lors de l'utilisation de modèles de formulaires InfoPath avec code managé, qui utilisent le modèle objet compatible InfoPath 2003 fourni par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** lors de l'exécution. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Afficher les notifications pour les exceptions de code managé en cours d’exécution

Si vous n'utilisez pas la gestion d'exceptions try-catch dans le code du formulaire, InfoPath affiche des informations sur les exceptions non gérées dans la boîte de dialogue d'erreurs d'InfoPath lors du débogage et de l'aperçu. Cependant, par défaut, les exceptions non gérées ne sont pas affichées dans la boîte de dialogue d'erreurs d'InfoPath lors de l'exécution lorsque vous déployez votre modèle de formulaire avec code managé. Si vous souhaitez que les exceptions de code managé affichées au moment de l’exécution, suivez la procédure décrite dans la section « Gérer les Exceptions de Code managé » de [Gérer les erreurs à l’aide du modèle objet InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Problèmes avec les modèles de formulaires avec code managé après le déploiement

Testez votre modèle de formulaire avec code managé à l'emplacement de son déploiement. Pour plus d’informations sur les procédures de déploiement, voir [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md). Pour plus d’informations sur les scénarios de sécurité qui affectent le déploiement, voir [Modèle de sécurité pour les modèles de formulaire avec du Code](about-the-security-model-for-form-templates-with-code.md).
  
Si vous utilisez l'utilitaire de configuration de .NET Framework 1.1 et le groupe de codes de modèles de formulaires InfoPath pour ajouter des autorisations spécifiques à un modèle de formulaire avec code managé, assurez-vous que la même stratégie de sécurité est déployée sur tous les ordinateurs clients. De même, si vous spécifiez un élément **URLEvidence** qui fait référence à un emplacement sur l'ordinateur local, assurez-vous que l'emplacement spécifié fait référence au dossier dans lequel la solution sera finalement déployée (emplacement différent de celui utilisé pendant le développement). Pour plus d’informations sur la configuration des paramètres de sécurité de .NET Framework pour un modèle de formulaire avec code managé, voir la section « Affectation de FullTrust à formulaires à un spécifique URL ou UNC » de la rubrique [Configurer les paramètres de sécurité pour les modèles de formulaire avec du Code](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>Voir aussi

- [Sur le modèle de sécurité pour les modèles de formulaires avec Code](about-the-security-model-for-form-templates-with-code.md)
- [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md)
- [Gestion des erreurs à l’aide du modèle objet InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Débogage de projets InfoPath à l’aide du modèle objet InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

