---
title: Développement de serveurs de formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338527"
---
# <a name="developing-mapi-form-servers"></a>Développement de serveurs de formulaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette section décrit le processus de création de fichiers exécutables et de configuration de formulaire pour la création de formulaires MAPI personnalisés. Avant de lire cette section, vous devez vous familiariser avec les informations contenues dans les [formulaires MAPI](mapi-forms.md).
  
Le développement d'un serveur de formulaire comprend les étapes suivantes:
  
1. Le choix des informations que le formulaire doit contenir et la sélection d'un ensemble de propriétés pour stocker ces informations. Pour plus d'informations, consultez [la rubrique choix du jeu de propriétés d'un formulaire](choosing-a-form-s-property-set.md).
    
2. Conception d'une interface utilisateur avec laquelle les utilisateurs peuvent interagir avec les propriétés du formulaire.
    
3. Sélection d'une classe de message et génération d'un identificateur de classe unique (CLSID). Pour une vue d'ensemble des classes de message, voir [MAPI message classes](mapi-message-classes.md). Pour plus d'informations sur les classes de message et les formulaires, voir [Choosing a message Class](choosing-a-message-class.md).
    
4. L'implémentation des interfaces de formulaire MAPI requises, ainsi que les interfaces facultatives dont votre serveur de formulaire particulier a besoin. Pour plus d'informations, consultez la rubrique [Writing Form Server Code](writing-form-server-code.md). 
    
5. Écriture du code de l'interface utilisateur pour gérer l'interaction de l'utilisateur avec l'objet Form et les propriétés utilisées par le formulaire.
    
6. Création d'un fichier de configuration de formulaire pour le formulaire. Pour plus d'informations, consultez la rubrique [format de fichier des fichiers de configuration de formulaire](file-format-of-form-configuration-files.md).
    
7. Installation du formulaire sur les ordinateurs des utilisateurs. Pour plus d'informations, consultez la rubrique [installation d'un formulaire dans une bibliothèque](installing-a-form-into-a-library.md).
    
Vous devrez probablement effectuer les étapes 1 à 5 simultanément au lieu de les effectuer dans l'ordre. Le processus de développement d'un serveur de formulaire, comme de nombreux projets de programmation, n'est pas celui dans lequel il existe une séquence bien définie. Par exemple, la création d'un fichier de configuration de formulaire est l'avant-dernière étape ci-dessus, mais vous créerez probablement progressivement votre fichier de configuration de formulaire, et il deviendra plus complet à mesure que vous ajoutez des fonctionnalités à votre serveur de formulaires.
  
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

