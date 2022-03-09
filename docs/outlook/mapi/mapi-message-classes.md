---
title: MAPI Message Classes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
ms.openlocfilehash: 60c17a36ba8ebd10f6a9932ba48c5ba636b2e5e6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369083"
---
# <a name="mapi-message-classes"></a>MAPI Message Classes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque message possède une propriété de classe de message, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), qui identifie le type, l’objectif ou le contenu du message. **PR_MESSAGE_CLASS** est une propriété obligatoire sur tous les nouveaux messages. La classe d’un message détermine le formulaire utilisé pour présenter le message à l’utilisateur et le dossier pour le placement des messages entrants. 
  
Les classes de message sont des chaînes de caractères sensibles à la cas qui contiennent des caractères ASCII 32 à 127 et sont délimitées par des périodes, mais elles ne peuvent pas se terminer par un point. Chaque chaîne représente un niveau de sous-classe et il n’existe aucune limite au nombre de niveaux autorisés. 
  
Par exemple, la plupart des messages que les applications clientes envoient et reçoivent relèvent de la classe de message **IPM** , une catégorie large qui décrit tous les messages interpersonnels (c’est-à-dire, les messages destinés à être lus par un utilisateur humain, plutôt que par programme par un ordinateur). Les fournisseurs de magasins de messages décrivent plus précisément un message IPM en créant une **sous-classe IPM** . La **sous-classe IPM** hérite des propriétés de la **classe de message IPM** . Les sous-classes de la **classe IPM** sont nommées en concatenant d’autres chaînes de caractères sur l’identificateur **IPM, comme IPM. Remarque** pour décrire un message de note et **un IPM. Contactez** pour décrire un message de contact. 
  
Pour gérer l’affichage et la gestion des messages IPM, les clients peuvent utiliser un formulaire standard que MAPI fournit. Pour gérer l’affichage et la gestion des nouvelles classes de messages, en tant que développeur d’applications clientes, vous avez deux options :
  
1. Vous pouvez créer un formulaire à l’aide de l’ensemble d’interfaces de formulaire définies par MAPI qu’un client standard peut utiliser.
    
2. Vous pouvez écrire votre propre client en implémentant une application complète et autonome. 
    
Bien que les clients doivent définir la propriété PR_MESSAGE_CLASS pour chaque message sortant sur une sous-classe **IPM** ou **IPC**, le fournisseur de magasin de messages **a** la responsabilité finale de le définir. Par conséquent, si un client envoie un message sans définir sa classe de message, le fournisseur de magasin de messages le définit sur la valeur par défaut appropriée pour le type approprié de client. La classe de message par défaut pour les clients de messagerie interpersonnels est **IPM** ; La classe de message par défaut pour les clients de communication interprocessus est **IPC**. 
  
Les classes de message ont une restriction de longueur de 255 caractères. Toutefois, les classes de message ne doivent pas dépasser 127 caractères pour prendre en charge les classes de message utilisées dans les états. Les classes de message de rapport sont basées sur la classe du message d’origine, avec deux ajouts : un préfixe et un suffixe. Le préfixe REPORT indique que le message est un rapport et que le suffixe indique le type de rapport : DR (rapport de remise), NDR (rapport de non remise), IPNRN (rapport de lecture) ou IPNNRN (rapport non lu). Notez que ces restrictions de longueur sont données en caractères ; sur les plateformes qui utilisent un jeu de caractères sur deux sur deux caractères, le nombre d’byte réel peut être supérieur. 
  
Les fournisseurs de magasins de messages doivent renvoyer des MAPI_E_INVALID_PARAMETER à partir de leurs implémentations de méthode [IMAPIProp::SetProps](imapiprop-setprops.md) lorsqu’un client tente d’affecter une chaîne qui dépasse la limite autorisée pour sa classe de message. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Messages](mapi-messages.md)

