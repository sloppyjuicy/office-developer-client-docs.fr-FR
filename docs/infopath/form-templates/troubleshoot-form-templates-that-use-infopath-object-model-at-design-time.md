---
title: Résoudre les problèmes de modèles de formulaire qui utilisent le modèle objet InfoPath au moment de la conception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, troubleshooting at design time,troubleshooting form templates [InfoPath 2007], design time
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: Les sections suivantes décrivent les scénarios de dépannage usuels que vous pouvez rencontrer lors de la conception et du débogage des modèles de formulaires avec code managé qui utilisent le modèle objet compatible InfoPath 2003 fourni par l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: 106f12602bae86d85c2a7d2f920f59d50326c908
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436523"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Résoudre les problèmes de modèles de formulaire qui utilisent le modèle objet InfoPath au moment de la conception

Les sections suivantes décrivent les scénarios de dépannage usuels que vous pouvez rencontrer lors de la conception et du débogage des modèles de formulaires avec code managé qui utilisent le modèle objet compatible InfoPath 2003 fourni par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Impossible d'afficher l'aperçu ou de déboguer les modèles de formulaires qui utilisent des appels à des méthodes et des propriétés du niveau de sécurité 3 du modèle objet

Si vous essayez de déboguer ou d'afficher un projet avec code managé qui contient du code faisant appel à des membres du modèle objet qui nécessitent une confiance totale, InfoPath affiche le message d'erreur « Une exception de sécurité non gérée s’est produite dans le code du formulaire » et le formulaire ne s'ouvre pas. Pour autoriser le débogage ou l'aperçu de la logique métier dans le modèle de formulaire, vous devez définir le niveau de sécurité **Confiance totale** et signer numériquement le modèle de formulaire. Pour plus d’informations sur la façon de le faire, voir Aperçu et [débogage des modèles de formulaires qui nécessitent une confiance totale.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>Impossible de mettre à jour les expressions XPath dans les gestionnaires d'événements si la valeur du paramètre MatchPath a été supprimée manuellement

Si vous ajoutez un gestionnaire d'événements à un groupe ou un champ, puis que vous modifiez par la suite le schéma de la source de données dans le volet Office **Champs** et que cette modification affecte le champ ou le groupe (par exemple en le renommant ou en le déplaçant), un message s'affiche vous demandant si vous souhaitez mettre à jour les expressions XPath dans le code de votre formulaire. Les expressions XPath référentes dans ce message sont les valeurs spécifiées dans le paramètre [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) de l’attribut [InfoPathEventHandlerAttribute,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) qui sont utilisées pour associer le handler d’événements à un champ ou un groupe dans la source de données de votre formulaire. Aucune autre expression XPath dans votre code n'est mise à jour. L'algorithme de mise à jour des expressions XPath dépend d'une valeur présente dans le paramètre **MatchPath** des attributs **InfoPathEventHandler** appliqués au code de votre formulaire. Si vous supprimez manuellement ces valeurs avant de répondre à l'invite de mise à jour des expressions XPath, InfoPath ne peut pas mettre à jour automatiquement les expressions XPath. Pour plus d’informations, voir Ajouter un handler d’événements à l’aide du modèle objet [InfoPath 2003.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Impossible d'appeler les membres du modèle objet compatible InfoPath 2003 dans un thread distinct

Le modèle objet compatible InfoPath 2003 ne prend pas en charge les appels dans un thread distinct. Par exemple, le code suivant qui appelle la fonction  LaunchOMFunction, qui appelle à son tour les membres du modèle objet InfoPath, ne s'exécute pas. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

Si nécessaire, il existe un moyen de contourner cette limitation. Pour plus d’informations, voir Prise en charge des threads dans les projets InfoPath à l’aide du modèle objet [InfoPath 2003.](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>L'omission de paramètres crée une erreur de génération dans Visual Basic et Visual C#.

Si un membre du modèle objet InfoPath contient un paramètre facultatif et que vous ne spécifiez pas de valeur pour ce paramètre, vous devez transmettre le champ **Type.Missing** pour ce paramètre à la place. Si vous ne transmettez pas le champ **Type.Missing** alors que la valeur est omise, cela provoque une erreur de compilation. Ceci se produit aussi bien pour le code écrit en Visual Basic ou en Visual C#. Pour plus d’informations et d’exemples, voir la section « Passage de paramètres facultatifs aux membres du modèle objet InfoPath » dans la rubrique Modèles objet [compatibles InfoPath 2003.](infopath-2003-compatible-object-models.md) 
  
## <a name="see-also"></a>Voir aussi

- [À propos du modèle de sécurité pour les modèles de formulaires avec code](about-the-security-model-for-form-templates-with-code.md)
- [Déployer des modèles de formulaire InfoPath avec code](how-to-deploy-infopath-form-templates-with-code.md)
- [Gérer les erreurs à l’aide du modèle objet InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Afficher un aperçu et déboguer des modèles de formulaire exigeant l'autorisation totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Débogage de projets InfoPath à l’aide du modèle objet InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

