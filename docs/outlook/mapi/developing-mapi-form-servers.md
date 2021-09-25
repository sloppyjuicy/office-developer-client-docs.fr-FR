---
title: Développement de serveurs de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: af3960938defba5b14a602704ccd5a214951a6e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605033"
---
# <a name="developing-mapi-form-servers"></a>Développement de serveurs de formulaire MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette section décrit le processus de création de fichiers exécutables et de configuration de formulaires de serveur de formulaires pour la création de formulaires MAPI personnalisés. Avant de lire cette section, vous devez vous familiariser avec les informations des formulaires [MAPI.](mapi-forms.md)
  
Le développement d’un serveur de formulaire comprend les étapes suivantes :
  
1. Choix des informations contenues dans le formulaire et choix d’un ensemble de propriétés pour contenir ces informations. Pour plus d’informations, [voir Choosing a Form’s Property Set](choosing-a-form-s-property-set.md).
    
2. Conception d’une interface utilisateur avec laquelle les utilisateurs peuvent interagir avec les propriétés du formulaire.
    
3. Choix d’une classe de message et génération d’un identificateur de classe unique (CLSID). Pour une vue d’ensemble des classes de message, voir [CLASSES de message MAPI.](mapi-message-classes.md) Pour plus d’informations sur les classes de message et les formulaires, voir [Choosing a Message Class](choosing-a-message-class.md).
    
4. Implémenter les interfaces de formulaire MAPI requises, ainsi que les interfaces facultatives dont votre serveur de formulaires spécifique a besoin. Pour plus d’informations, voir [Écrire du code serveur de formulaires.](writing-form-server-code.md) 
    
5. Écriture de code d’interface utilisateur pour gérer l’interaction de l’utilisateur avec l’objet formulaire et les propriétés qu’il utilise.
    
6. Création d’un fichier de configuration de formulaire pour le formulaire. Pour plus d’informations, [voir Format de fichier des fichiers de configuration de formulaire.](file-format-of-form-configuration-files.md)
    
7. Installation du formulaire sur les ordinateurs des utilisateurs. Pour plus d’informations, [voir Installation d’un formulaire dans une bibliothèque.](installing-a-form-into-a-library.md)
    
Vous effectuerez probablement les étapes 1 à 5 simultanément au lieu de les effectuer dans l’ordre. Le processus de développement d’un serveur de formulaires, comme de nombreux projets de programmation, n’est pas celui dans lequel il existe une séquence particulièrement bien définie. Par exemple, la création d’un fichier de configuration de formulaire s’affiche comme avant-dernière étape ci-dessus, mais vous créerez probablement votre fichier de configuration de formulaire de manière incrémentielle et il deviendra plus complet à mesure que vous ajouterez des fonctionnalités à votre serveur de formulaires.
  
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

