---
title: Vue d’ensemble de la référence MAPI Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Derni�re modification�: vendredi 1 f�vrier 2013'
ms.openlocfilehash: a5c1daf44f89d1ef8aa7472d69dfd7e86bbb92f6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387999"
---
# <a name="outlook-mapi-reference-overview"></a>Vue d’ensemble de la référence MAPI Outlook

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique fournit des informations générales sur la documentation de référence de MAPI pour Outlook 2013.
  
## <a name="about-this-documentation"></a>À propos de cette documentation

Cette documentation s’applique à l’implémentation de la MAPI (Messaging API) dans Microsoft Outlook 2013. 
  
Antérieures à Microsoft Office Outlook 2007, référence du programmeur MAPI fait partie de la documentation de Microsoft Exchange.
  
> [!NOTE]
> Étant donné que Exchange a deemphasized l’utilisation de MAPI depuis Microsoft Exchange Server 2007, prise en charge pour l’implémentation Exchange est limitée. 
  
L’implémentation Outlook de MAPI diffère de l’implémentation de Microsoft Exchange. L’implémentation d’Outlook est optimisée pour l’exécution sur les ordinateurs clients et met en évidence faible latence. L’implémentation Exchange est conçue pour les serveurs où la haute disponibilité et mieux multithreading sont importantes.
  
Utilisez cette documentation pour les applications en cours d’exécution sur les systèmes de l’utilisateur final. Pour les applications serveur, utilisez l’implémentation Exchange de MAPI, le cas échéant, ou des API Exchange actuelles telles que les Services Web Exchange. Pour plus d’informations sur les Services Web Exchange, voir la [Référence de Services Web Exchange](https://msdn.microsoft.com/library/bb204119.aspx).
  
Il peut être possible d’écrire des applications qui fonctionnent avec les implémentations Exchange ou Outlook de MAPI. Par exemple, MFCMAPI fonctionne sur les deux plates-formes. Les implémentations proposent de nombreuses fonctionnalités courantes, mais il existe des différences évidentes et discret. Vous devez tester avec soin sur les deux plateformes si vous souhaitez que votre application fonctionne dans les environnements. Ce test nécessite deux systèmes, car les deux implémentations en cours d’exécution sur la même installation de système d’exploitation n’est pas pris en charge.
  
Sachez que MAPI est appropriée pour l’accès aux données dans un emplacement de stockage MAPI de bas niveau ou à la création d’un transport, la banque de messages ou le fournisseur de carnet d’adresses. Étant donné que MAPI contourne la logique métier d’Outlook, vous devez également envisager l’utilisation du modèle objet Outlook lors de l’évaluation des API pour la création de votre solution. Le modèle objet Outlook encapsule la logique métier Outlook mais n’est pas adapté aux applications de Service Windows, les fournisseurs de synchronisation ou code multithread.
  
Pour plus d’informations sur les nouveautés de cette édition, consultez les rubriques suivantes :
  
- [Nouveaut�s de cette �dition (en anglais)](what-s-new-in-this-edition.md)
    
- [�l�ments d'API d�conseill�es dans cette �dition](api-elements-deprecated-in-this-edition.md)
    
Si vous débutez au développement d’applications MAPI pour Outlook, consultez les rubriques suivantes :
  
- [Sélection d’une API ou d’une technologie pour développer des solutions pour Outlook 2013](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [Utilis�e couramment des fichiers d'en-t�te](commonly-used-header-files.md)
    
- [Propri�t�s couramment utilis�es](commonly-used-properties.md)
    
- [Objets couramment utilis�es](commonly-used-objects.md)
    
Le reste de cette référence est classé dans les trois types d’informations suivantes :
  
- [Exemples MAPI](mapi-samples.md) - permet d’accéder à nombreux exemples de code qui illustrent l’utilisation des différents éléments d’API et comment implémenter des fournisseurs de base MAPI et créer des éléments Outlook. 
    
- [Concepts MAPI](mapi-concepts.md) - explique les concepts et l’architecture de MAPI. 
    
- [Référence MAPI](mapi-reference.md) - fournit des informations détaillées sur les fonctions, les interfaces, les structures et les propriétés MAPI. 
    
## <a name="see-also"></a>Voir aussi

- [Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)
- [Exemples MAPI (en anglais)](mapi-samples.md)
- [Concepts MAPI (en anglais)](mapi-concepts.md)

