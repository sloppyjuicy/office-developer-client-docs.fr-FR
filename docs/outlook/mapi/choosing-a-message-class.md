---
title: Sélection d’une classe de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c3b486838c6ce2d7fc38d950a4de6f4589767073
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574236"
---
# <a name="choosing-a-message-class"></a>Sélection d’une classe de message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Comme décrit dans [Les Classes de Message MAPI](mapi-message-classes.md), les classes de message sont importants pour l’établissement de la relation entre les types de messages personnalisés et, par extension, entre les serveurs de formulaire eux-mêmes. Heureusement, le choix d’une chaîne de classe de message est relativement simple. La chaîne de classe de message d’une classe de message est une chaîne arbitraire, mais elle doit utiliser les conventions suivantes :
  
- La chaîne doit satisfaire à toutes les conventions décrites dans la documentation de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). En premier lieu, la chaîne doit être composé uniquement de caractères ANSI et moins de 256 caractères.
    
- Si votre serveur de formulaire est dérivée d’un serveur de formulaire existant ou est une extension d’un serveur de formulaire existant, votre chaîne de classe de message doit être formé en ajoutant un point et un autre mot à la chaîne de classe de message du serveur de formulaire basé sur votre formulaire. Par exemple, vous souhaiterez peut-être mettre en œuvre un formulaire pour replanifier une réunion, et votre formulaire est basé sur un formulaire existant pour la planification de réunions. Si la réunion de planification de la chaîne de classe de message du formulaire est « IPM. Réunion », votre chaîne de classe de message peut être « IPM. Meeting.Reschedule ».
    
- Si votre formulaire n’est pas basé sur un formulaire existant, votre chaîne de classe de message doit toujours commencer par soit le « IPM. » ou « IPC. » préfixe, selon que le formulaire est destiné à être reçus par une personne ou une autre application. « IPM. » désigne un message interpersonnel finit généralement dans la boîte de réception d’un utilisateur et « IPC. » désigne un message d’une communication n’est pas généralement remis à la boîte de réception d’un utilisateur.
    
- Si votre classe de message est destiné à être explicite, la chaîne de classe de message doit commencer par « IPM. » Une classe de message est constitue comme explicite si elle utilise des propriétés qui contiennent du texte brut, HTML ou RTF (RICH Text Format). Si votre formulaire utilise la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), elle doit utiliser certainement « IPM. » chaîne de classe de message. Par exemple, si vous implémentez un formulaire pour les bons de commande et que votre organisation requiert que les commandes d’achat approuvées par un responsable, votre chaîne de classe de message peut être « IPM. Purchase_Order ». Les formulaires qui sont conçus pour utilisent des dossiers publics ou les applications de dossier public sont généralement considérés comme interpersonnel parce qu’ils sont lus par des personnes, même s’ils ne sont pas réellement adressés à l’adresse électronique toute personne. Le préfixe pour les classes de messages de dossiers publics par défaut est « IPM. POST ». 
    
- Si votre classe de message est destiné à être reçus par une autre application et non par une personne, la chaîne de classe de message doit commencer par « IPC. » Par exemple, si vous implémentez un formulaire qui permet aux utilisateurs de s’abonner automatiquement aux listes de distribution, votre chaîne de classe de message peut être « IPC. S’abonner ».
    
- La chaîne de classe de message jamais doit se terminer par un point.
    
La chaîne de classe de message doit être placée dans la section **[Description]** du fichier de configuration de formulaire, dans l’entrée **MessageClass** , semblable au suivant : 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Une fois que vous avez choisi une chaîne de classe de message approprié, vous devez générer un identificateur de classe pour qu’il. Identificateurs de classe peuvent être générés avec la commande de **Création de GUID** qui est incluse dans Visual Studio. L’identificateur de classe doit être placée dans l’entrée **CLSID** du fichier de configuration de formulaire, ainsi que l’entrée **MessageClass** , semblable au suivant : 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
L’identificateur de classe est très certainement différent, bien sûr. Pour plus d’informations, consultez [Création d’un fichier de Configuration du formulaire](creating-a-form-configuration-file.md).
  
Lorsque le formulaire est installé sur l’ordinateur d’un utilisateur, le processus d’installation, s’il s’agit d’un programme d’installation ou toute autre chose — doit créer une entrée de Registre dans la **HKEY_CLASSES_ROOT\CLSID\* * section du Registre pour l’identificateur de classe. Cette entrée doit être définie à la chaîne de classe de message. Par exemple, vous créeriez une entrée de Registre semblable à ce qui suit pour l’identificateur de classe d’exemple ci-dessus : 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Pour plus d’informations, consultez [installation d’un formulaire dans une bibliothèque](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

