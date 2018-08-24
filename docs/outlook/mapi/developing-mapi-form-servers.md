---
title: Développement de serveurs de formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d55134cf5181ebbba0108c228d9afc3a494e75ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576238"
---
# <a name="developing-mapi-form-servers"></a>Développement de serveurs de formulaires MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette section décrit le processus de création du fichier exécutable du serveur de formulaire et les fichiers de configuration de formulaire pour la création de formulaires MAPI personnalisés. Avant de lire cette section, vous devez vous familiariser avec les informations contenues dans les [Formulaires MAPI](mapi-forms.md).
  
Développement d’un serveur de formulaire comprend les étapes suivantes :
  
1. Déterminer quelles informations contiendrait le formulaire et en sélectionnant un ensemble de propriétés pour stocker ces informations. Pour plus d’informations, voir [choix de la valeur de propriété d’un formulaire](choosing-a-form-s-property-set.md).
    
2. Conception d’une interface utilisateur avec lequel les utilisateurs peuvent interagir avec les propriétés du formulaire.
    
3. Choix d’une classe de message et la génération d’un identificateur unique de classe (CLSID). Pour une vue d’ensemble des classes de messages, consultez [Les Classes de Message MAPI](mapi-message-classes.md). Pour plus d’informations sur les formulaires et les classes de messages, voir [choix d’une classe de Message](choosing-a-message-class.md).
    
4. Implémenter les interfaces de formulaire MAPI requises, ainsi que toutes les interfaces facultatifs qui a besoin de votre serveur de formulaire particulier. Pour plus d’informations, voir [L’écriture de Code de formulaire serveur](writing-form-server-code.md). 
    
5. Écriture de code pour gérer l’interaction de l’utilisateur avec l’objet de formulaire et les propriétés de l’interface utilisateur par le formulaire.
    
6. Création d’un fichier de configuration de formulaire pour le formulaire. Pour plus d’informations, voir [Fichier fichiers au Format de formulaire Configuration](file-format-of-form-configuration-files.md).
    
7. Installation du formulaire sur les ordinateurs des utilisateurs. Pour plus d’informations, consultez [installation d’un formulaire dans une bibliothèque](installing-a-form-into-a-library.md).
    
Vous serez probablement effectuer les étapes 1 à 5 simultanément au lieu de les effectuer dans l’ordre. Le processus de développement d’un serveur de formulaire, comme de nombreux projets de programmation, n’est pas est une séquence particulièrement bien définie. Par exemple, création d’un fichier de configuration de formulaire est affiché comme la seconde à la dernière étape ci-dessus, mais vous allez probablement créer votre fichier de configuration de formulaire incrémentielle, et devient plus complète lorsque vous ajoutez des fonctionnalités à votre serveur de formulaire.
  
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

