---
title: Classes de message MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b2ab5d56c53216152a83ca207ff5ba1d53c9049d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345893"
---
# <a name="mapi-message-classes"></a>Classes de message MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque message a une propriété de classe de message, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), qui identifie le type, l'objectif ou le contenu du message. **PR_MESSAGE_CLASS** est une propriété obligatoire pour tous les nouveaux messages. La classe d'un message détermine le formulaire utilisé pour présenter le message à l'utilisateur et au dossier de placement des messages entrants. 
  
Les classes de message sont des chaînes de caractères qui contiennent des caractères ASCII 32 à 127 et qui sont délimitées par des points, mais elles ne peuvent pas se terminer par un point. Chaque chaîne représente un niveau de sous-classe et il n'y a pas de limite au nombre de niveaux autorisés. 
  
Par exemple, la plupart des messages que les applications clientes envoient et reçoivent entrent dans la classe de message **IPM** , une catégorie large qui décrit tous les messages interpersonnels (c'est-à-dire, les messages destinés à être lus par un utilisateur humain, et non par programme ordinateur). Les fournisseurs de banques de messages décrivent plus précisément un message IPM en créant une sous-classe **IPM** . La sous-classe **IPM** hérite des propriétés de la classe de message **IPM** . Les sous-classes de la classe **IPM** sont nommées en concaténant d'autres chaînes de caractères sur l'identificateur IPM, comme **IPM. Remarque** pour décrire un message de note et **IPM. Contact** pour décrire un message de contact. 
  
Pour gérer l'affichage et la gestion des messages IPM, les clients peuvent utiliser un formulaire standard fourni par MAPI. Pour gérer l'affichage et la gestion des nouvelles classes de message, vous devez être développeur d'application cliente de deux options:
  
1. Vous pouvez créer un nouveau formulaire à l'aide de l'ensemble d'interfaces de formulaire défini par MAPI qu'un client standard peut utiliser.
    
2. Vous pouvez écrire votre propre client en implémentant une application complète et autonome. 
    
Bien que les clients doivent définir la propriété **PR_MESSAGE_CLASS** pour chaque message sortant sur une sous-classe de **IPM** ou **IPC**, le fournisseur de banque de messages a la responsabilité ultime de le définir. Par conséquent, si un client envoie un message sans définir sa classe de message, le fournisseur de banque de messages lui affecte la valeur par défaut appropriée pour le type de client approprié. La classe de message par défaut pour les clients de messagerie interpersonnels est **IPM**; la classe de message par défaut pour les clients de communication interprocessus est **IPC**. 
  
Les classes de message ont une restriction de longueur de 255 caractères. Toutefois, les classes de message ne doivent pas dépasser 127 caractères pour prendre en charge les classes de message utilisées dans les rapports. Les classes de message de rapport sont basées sur la classe du message d'origine, avec deux additions: un préfixe et un suffixe. Le rapport de préfixe indique que le message est un rapport et que le suffixe indique le type de rapport: DR (rapport de remise), notification d'échec de remise (rapport de non-remise), IPNRN (rapport de lecture) ou IPNNRN (rapport non lu). Notez que ces restrictions de longueur sont indiquées en caractères; sur les plateformes qui utilisent un jeu de caractères codés sur deux octets, le nombre d'octets réel peut être plus élevé. 
  
Les fournisseurs de banques de messages doivent renvoyer MAPI_E_INVALID_PARAMETER à partir de leurs implémentations de méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) lorsqu'un client tente d'assigner une chaîne dépassant la limite autorisée pour sa classe de message. 
  
## <a name="see-also"></a>Voir aussi



[Messages MAPI](mapi-messages.md)

