---
title: Résoudre les problèmes des modèles de formulaires qui utilisent le modèle objet InfoPath au moment du design
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, troubleshooting at design time,troubleshooting form templates [InfoPath 2007], design time
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: Les sections suivantes décrivent les scénarios de dépannage usuels que vous pouvez rencontrer lors de la conception et du débogage des modèles de formulaires avec code managé qui utilisent le modèle objet compatible InfoPath 2003 fourni par l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: af71c8058744561a4c8ee0870fb37054e9979751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782462"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Résoudre les problèmes des modèles de formulaires qui utilisent le modèle objet InfoPath au moment du design

Les sections suivantes décrivent les scénarios de dépannage usuels que vous pouvez rencontrer lors de la conception et du débogage des modèles de formulaires avec code managé qui utilisent le modèle objet compatible InfoPath 2003 fourni par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Impossible d'afficher l'aperçu ou de déboguer les modèles de formulaires qui utilisent des appels à des méthodes et des propriétés du niveau de sécurité 3 du modèle objet

Si vous essayez de déboguer ou d'afficher un projet avec code managé qui contient du code faisant appel à des membres du modèle objet qui nécessitent une confiance totale, InfoPath affiche le message d'erreur « Une exception de sécurité non gérée s'est produite dans le code du formulaire » et le formulaire ne s'ouvre pas. Pour autoriser le débogage ou l'aperçu de la logique métier dans le modèle de formulaire, vous devez définir le niveau de sécurité **Confiance totale** et signer numériquement le modèle de formulaire. Pour plus d’informations sur la procédure à suivre, voir [prévisualiser et déboguer les modèles de formulaires qui nécessitent une confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md).
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>Impossible de mettre à jour les expressions XPath dans les gestionnaires d'événements si la valeur du paramètre MatchPath a été supprimée manuellement

Si vous ajoutez un gestionnaire d'événements à un groupe ou un champ, puis que vous modifiez par la suite le schéma de la source de données dans le volet Office **Champs** et que cette modification affecte le champ ou le groupe (par exemple en le renommant ou en le déplaçant), un message s'affiche vous demandant si vous souhaitez mettre à jour les expressions XPath dans le code de votre formulaire. Les expressions XPath auxquelles ce message fait référence sont les valeurs spécifiées dans le paramètre [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) de l'attribut [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) qui sont utilisées pour associer le gestionnaire d'événements à un champ ou un groupe dans la source de données de votre formulaire. Aucune autre expression XPath dans votre code n'est mise à jour. L'algorithme de mise à jour des expressions XPath dépend d'une valeur présente dans le paramètre **MatchPath** des attributs **InfoPathEventHandler** appliqués au code de votre formulaire. Si vous supprimez manuellement ces valeurs avant de répondre à l'invite de mise à jour des expressions XPath, InfoPath ne peut pas mettre à jour automatiquement les expressions XPath. Pour plus d’informations, voir [Ajouter un gestionnaire d’événement à l’aide du modèle objet InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Impossible d'appeler les membres du modèle objet compatible InfoPath 2003 dans un thread distinct

Le modèle objet compatible InfoPath 2003 ne prend pas en charge les appels dans un thread distinct. Par exemple, le code suivant qui appelle la fonction LaunchOMFunction, qui appelle à son tour les membres du modèle objet InfoPath, ne s'exécute pas. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

Si nécessaire, il existe un moyen de contourner cette limitation. Pour plus d'information, voir [Prise en charge du threading dans les projets InfoPath à l'aide du modèle de projet InfoPath 2003](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>L'omission de paramètres crée une erreur de génération dans Visual Basic et Visual C#.

Si un membre du modèle objet InfoPath contient un paramètre facultatif et que vous ne spécifiez pas de valeur pour ce paramètre, vous devez transmettre le champ **Type.Missing** pour ce paramètre à la place. La non-transmission du champ **Type.Missing** lorsqu'une valeur réelle est omise provoque une erreur de génération. Ceci se produit aussi bien pour le code écrit en Visual Basic ou en Visual C#. Pour plus d'informations et d'exemples, voir la section « Transmission de paramètres facultatifs à des membres du modèle objet InfoPath » dans la rubrique [Modèles objet compatibles avec InfoPath 2003](infopath-2003-compatible-object-models.md). 
  
## <a name="see-also"></a>Voir aussi

- [Sur le modèle de sécurité pour les modèles de formulaires avec Code](about-the-security-model-for-form-templates-with-code.md)
- [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md)
- [Gestion des erreurs à l’aide du modèle objet InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Afficher un aperçu et déboguer les modèles de formulaires nécessitant la confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Débogage de projets InfoPath à l’aide du modèle objet InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

