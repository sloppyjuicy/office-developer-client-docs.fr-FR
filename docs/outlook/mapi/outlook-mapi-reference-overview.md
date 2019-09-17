---
title: Vue d’ensemble de la référence MAPI Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: Dernière modification le 1er février 2013
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348495"
---
# <a name="outlook-mapi-reference-overview"></a>Vue d’ensemble de la référence MAPI Outlook

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique fournit des informations générales sur la documentation Référence MAPI Outlook 2013.
  
## <a name="about-this-documentation"></a>À propos de la documentation

Cette documentation s’applique à l’implémentation de Messaging API (MAPI) dans Microsoft Outlook 2013. 
  
Avant Microsoft Office Outlook 2007, la référence du programmeur MAPI faisait partie de la documentation de Microsoft Exchange.
  
> [!NOTE]
> Étant donné qu’Exchange a minimisé l’utilisation de MAPI depuis Microsoft Exchange Server 2007, la prise en charge de l’implémentation Exchange est limitée. 
  
L’implémentation Outlook de MAPI diffère de l’implémentation Microsoft Exchange. L’implémentation Outlook est optimisée pour l’exécution sur les ordinateurs client et met en évidence la faible latence. L’implémentation Exchange est destinée aux serveurs où la haute disponibilité et un meilleur multithreading sont d’une grande importance.
  
Utilisez cette documentation pour les applications en cours d’exécution sur les systèmes de l’utilisateur final. Pour les applications serveur, utilisez l’implémentation Exchange de MAPI le cas échéant, ou utilisez les API Exchange actuelles telles que les Services Web Exchange. Pour plus d’informations sur les Services Web Exchange, consultez l’article [Référence des Services Web Exchange](https://msdn.microsoft.com/library/bb204119.aspx).
  
Il est possible de créer des applications qui fonctionnent avec des implémentations Outlook ou Exchange de MAPI. Par exemple, MFCMAPI fonctionne parfaitement sur les deux plateformes. Les implémentations proposent de nombreuses fonctionnalités courantes, mais il existe des différences évidentes et subtiles. Vous devez faire un essai sur les deux plateformes si vous souhaitez que votre application fonctionne dans tous les environnements. Ce test nécessitera deux systèmes, car l’exécution des deux implémentations sur l’installation du même système d’exploitation n’est pas prise en charge.
  
Sachez que MAPI convient pour un accès de bas niveau aux données d’une banque MAPI ou pour créer un transport, une banque de messages ou un fournisseur de carnets d’adresses. Étant donné que MAPI contourne la logique métier d’Outlook, vous pensez également à utiliser un modèle objet Outlook lorsque vous évaluez les API pour créer votre solution. Le modèle objet Outlook encapsule la logique métier d’Outlook, mais n’est pas utilisable pour le code multithread, la synchronisation des fournisseurs ou les applications de service Windows.
  
Pour connaître les nouveautés de cette édition, consultez les rubriques suivantes :
  
- [Nouveautés de cette édition](what-s-new-in-this-edition.md)
    
- [Éléments d’API obsolètes dans cette édition](api-elements-deprecated-in-this-edition.md)
    
Si vous êtes nouveau dans le développement d’applications MAPI pour Outlook, consultez les rubriques suivantes :
  
- [Sélection d’une API ou d’une technologie pour le développement de solutions pour Outlook 2013](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [Fichiers d’en-tête couramment utilisés](commonly-used-header-files.md)
    
- [Propriétés couramment utilisées](commonly-used-properties.md)
    
- [Objets couramment utilisés](commonly-used-objects.md)
    
Le reste de cette référence est classé dans les trois types d’informations suivants :
  
- [Exemples MAPI](mapi-samples.md) : vous dirige vers plusieurs exemples de code qui montrent l’utilisation de différents éléments d’API, et expliquent comment implémenter des fournisseurs MAPI de base et créer des éléments Outlook. 
    
- [Concepts MAPI](mapi-concepts.md) : explique les concepts et l’architecture de MAPI. 
    
- [Référence MAPI](mapi-reference.md) : fournit des informations détaillées sur les fonctions, les interfaces, les structures et les propriétés dans MAPI. 
    
## <a name="see-also"></a>Voir aussi

- [Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)
- [Exemples MAPI](mapi-samples.md)
- [Concepts MAPI](mapi-concepts.md)

