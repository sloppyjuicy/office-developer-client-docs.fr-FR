---
title: Choix d’une classe de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
ms.openlocfilehash: 9d5e1f8f8d21d9f47af3ae975d82de73199814b5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378092"
---
# <a name="choosing-a-message-class"></a>Choix d’une classe de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Comme décrit dans [classes de messages MAPI, les classes](mapi-message-classes.md) de message sont importantes pour établir la relation entre les types de messages personnalisés et, par extension, entre les serveurs de formulaires eux-mêmes. Heureusement, le choix d’une chaîne de classe de message est assez simple. La chaîne de classe de message d’une classe de message est une chaîne arbitraire, mais elle doit utiliser les conventions suivantes :
  
- La chaîne doit satisfaire toutes les conventions décrites dans la documentation pour la **propriété PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). Plus important encore, la chaîne doit être composée entièrement de caractères ANSI et avoir moins de 256 caractères.
    
- Si votre serveur de formulaires est dérivé d’un serveur de formulaires existant ou est une extension d’un serveur de formulaire existant, votre chaîne de classe de message doit être formée en ajoutant un point et un autre mot à la chaîne de classe de message du serveur de formulaires sur qui repose votre formulaire. Par exemple, vous pouvez implémenter un formulaire pour reprogrammer une réunion, et votre formulaire est basé sur un formulaire existant pour la planification des réunions. Si la chaîne de classe de message du formulaire de planification de réunion est « IPM. Réunion », votre chaîne de classe de message peut être « IPM. Meeting.Reschedule ».
    
- Si votre formulaire n’est basé sur aucun formulaire existant, votre chaîne de classe de message doit toujours commencer par l’un des deux « IPM ». ou « IPC ». préfixe, selon que le formulaire est destiné à être reçu par une personne ou par une autre application. « IPM . » désigne un message interpersonnel qui se retrouve généralement dans la boîte de réception d’un utilisateur et « IPC ». désigne un message de communication interprocessus qui n’est généralement pas remis à la boîte de réception d’un utilisateur.
    
- Si votre classe de message est destinée à être lisible par l’homme, la chaîne de classe de message doit commencer par « IPM ». Une classe de message est généralement considérée comme lisible par l’utilisateur si elle utilise des propriétés contenant du texte brut, du code HTML ou des données RTF (Rich Text Format). Si votre formulaire utilise la **propriété PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), il doit très certainement utiliser un « IPM ». chaîne de classe de message. Par exemple, si vous implémentez un formulaire pour les bon de commande et que votre organisation exige que les commandes d’achat soient approuvées par un responsable, votre chaîne de classe de message peut être « IPM ». Purchase_Order » Les formulaires conçus pour être utilisés avec des dossiers publics ou des applications de dossiers publics sont généralement considérés comme interpersonnels, car ils sont lus par des personnes même si elles ne sont pas réellement adressées à l’adresse e-mail d’une personne. Le préfixe type pour les classes de message de dossier public est « IPM.Post ». 
    
- Si votre classe de message est destinée à être reçue par une autre application plutôt que par une personne, la chaîne de classe de message doit commencer par « IPC ». Par exemple, si vous implémentez un formulaire qui permet aux utilisateurs de s’abonner automatiquement à des listes de diffusion, votre chaîne de classe de message peut être « IPC. Subscribe ».
    
- Votre chaîne de classe de message ne doit jamais se terminer par un point.
    
La chaîne de classe de message doit être mise dans la section **[Description]** du fichier de configuration du formulaire, dans l’entrée **MessageClass** , comme suit : 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Une fois que vous avez choisi une chaîne de classe de message appropriée, vous devez générer un identificateur de classe pour elle. Les identificateurs de classe peuvent être générés avec la commande **Créer un GUID** qui est incluse dans Visual Studio. L’identificateur de classe doit être placé dans l’entrée **CLSID** du fichier de configuration du formulaire, ainsi que dans l’entrée **MessageClass** , comme suit : 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Bien entendu, votre identificateur de classe sera très certainement différent. Pour plus d’informations, voir [Création d’un fichier de configuration de formulaire](creating-a-form-configuration-file.md).
  
Lorsque le formulaire est installé sur l’ordinateur d’un utilisateur, votre processus d’installation , qu’il s’agit d’un programme d’installation ou d’autres éléments, doit créer une entrée de Registre dans la section **HKEY_CLASSES_ROOT\CLSID\** du Registre pour l’identificateur de classe. Cette entrée doit être définie sur la chaîne de classe de message. Par exemple, vous créez une entrée de Registre semblable à la suivante pour l’exemple d’identificateur de classe ci-dessus : 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Pour plus d’informations, [voir Installation d’un formulaire dans une bibliothèque](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

