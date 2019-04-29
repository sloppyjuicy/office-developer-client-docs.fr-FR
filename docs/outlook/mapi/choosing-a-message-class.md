---
title: Sélection d'une classe de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428052"
---
# <a name="choosing-a-message-class"></a>Sélection d'une classe de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Comme décrit dans les [classes de message MAPI](mapi-message-classes.md), les classes de message sont importantes pour établir la relation entre les types de messages personnalisés et, par extension, entre les serveurs de formulaires eux-mêmes. Heureusement, le choix d'une chaîne de classe de message est relativement simple. La chaîne de classe de message d'une classe de message est une chaîne arbitraire, mais elle doit utiliser les conventions suivantes:
  
- La chaîne doit satisfaire à toutes les conventions décrites dans la documentation de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). En important, la chaîne doit être entièrement composée de caractères ANSI et comporter moins de 256 caractères.
    
- Si votre serveur de formulaire est dérivé d'un serveur de formulaires existant ou s'il s'agit d'une extension d'un serveur de formulaires existant, la chaîne de votre classe de message doit être formée en ajoutant un point et un autre mot à la chaîne de classe de message du serveur de formulaire sur lequel votre formulaire est basé. Par exemple, vous pouvez implémenter un formulaire pour replanifier une réunion, et votre formulaire est basé sur un formulaire existant pour la planification des réunions. Si la chaîne de classe de message du formulaire de planification de la réunion est «IPM. Réunion ", la chaîne de votre classe de message peut être" IPM. Meeting. reschedule».
    
- Si votre formulaire n'est pas basé sur un formulaire existant, la chaîne de votre classe de message doit toujours commencer par «IPM». ou «IPC». , selon que le formulaire est destiné à être reçu par une personne ou par une autre application. «IPM». désigne un message interpersonnel qui se trouve généralement dans la boîte de réception d'un utilisateur, et «IPC». désigne un message de communication entre processus qui n'est généralement pas remis dans la boîte de réception d'un utilisateur.
    
- Si votre classe de message est destinée à être lisible par un utilisateur, la chaîne de classe de message doit commencer par «IPM». Une classe de message est généralement considérée comme lisible par l'homme si elle utilise des propriétés qui contiennent du texte brut, du code HTML ou des données RTF (Rich Text Format). Si votre formulaire utilise la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), il doit utiliser un «IPM». chaîne de classe de message. Par exemple, si vous implémentez un formulaire pour les bons de commande et que votre organisation exige que les bons de commande soient approuvés par un responsable, la chaîne de votre classe de message peut être «IPM. Purchase_Order». Les formulaires qui sont conçus pour être utilisés avec des dossiers publics ou des applications de dossiers publics sont généralement considérés comme interpersonnels, car ils sont lus par des personnes même s'ils ne sont pas réellement adressés à l'adresse de messagerie d'une personne. Le préfixe standard pour les classes de message de dossier public est «IPM. Post». 
    
- Si votre classe de message doit être reçue par une autre application et non par une personne, la chaîne de classe de message doit commencer par «IPC». Par exemple, si vous implémentez un formulaire qui permet aux utilisateurs de s'abonner automatiquement à des listes de publipostage, la chaîne de votre classe de message peut être «IPC. S'abonner».
    
- La chaîne de votre classe de message ne doit jamais se terminer par un point.
    
La chaîne de classe de message doit être placée dans la section **[Description]** du fichier de configuration de formulaire, dans l'entrée **MessageClass** , semblable à la suivante: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Une fois que vous avez choisi une chaîne de classe de message appropriée, vous devez générer un identificateur de classe pour celle-ci. Les identificateurs de classe peuvent être générés à l'aide de la commande **Create GUID** incluse dans Visual Studio. L'identificateur de classe doit être placé dans l'entrée **CLSID** du fichier de configuration du formulaire, avec l'entrée **MessageClass** , semblable à la suivante: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Votre identificateur de classe sera presque certainement différent, bien entendu. Pour plus d'informations, consultez [la rubrique Création d'un fichier de configuration de formulaire](creating-a-form-configuration-file.md).
  
Lorsque le formulaire est installé sur l'ordinateur d'un utilisateur, votre processus d'installation, qu'il s'agisse d'un programme d'installation ou autre, doit créer une entrée de Registre dans la section **HKEY_CLASSES_ROOT\CLSID\* * du Registre pour l'identificateur de classe. Cette entrée doit être définie sur la chaîne de classe de message. Par exemple, vous créez une entrée de registre semblable à la suivante pour l'exemple d'identificateur de classe ci-dessus: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Pour plus d'informations, consultez la rubrique [installation d'un formulaire dans une bibliothèque](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

