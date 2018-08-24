---
title: Classes de Message MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: eecbbb3b806ecaee6c7ceba5c92bd4b713ad1075
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575139"
---
# <a name="mapi-message-classes"></a>Classes de Message MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Chaque message possède une propriété de classe de message, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), qui identifie le type, l’objectif ou le contenu du message. **PR_MESSAGE_CLASS** est une propriété requise sur tous les nouveaux messages. Classe d’un message détermine la forme qui est utilisée pour présenter le message à l’utilisateur et le dossier pour placer les messages entrants. 
  
Classes de message sont des chaînes de caractères qui respecte la casse qui contiennent des caractères ASCII 32 à 127 et sont délimités par des points, mais ils ne peuvent pas se terminer par un point. Chaque chaîne représente un niveau de sous-classer, et il n’existe aucune limite au nombre de niveaux autorisés. 
  
Par exemple, la plupart des messages que les applications clientes envoient et reçoivent compris dans le message **IPM** de classe, une catégorie large qui décrit tous les messages interpersonnels (autrement dit, les messages qui sont destinées à être lues par un utilisateur humain, plutôt que par programme par un ordinateur). Fournisseurs de magasins message décrivent plus précisément un message IPM en créant une sous-classe **IPM** . La sous-classe **IPM** hérite des propriétés de la classe de message **IPM** . Sous-classes de la classe **IPM** sont nommés par la concaténation des chaînes de caractères autres sur l’identificateur IPM, tel que **IPM. Remarque** pour décrire un message de la note et les **IPM. Contactez** pour décrire un message de contact. 
  
Pour gérer l’affichage et la gestion des messages IPM, les clients peuvent utiliser un formulaire standard qui fournit MAPI. Pour gérer l’affichage et la gestion de nouvelles classes de message, en tant que développeur client application ont deux options :
  
1. Vous pouvez créer un formulaire à l’aide de l’ensemble des interfaces de formulaire MAPI défini par un client standard peut utiliser.
    
2. Vous pouvez écrire votre propre client en implémentant complète, application autonome. 
    
Bien que les clients doivent définir la propriété **PR_MESSAGE_CLASS** pour chaque message sortant pour une sous-classe de **IPM** ou **IPC**, le fournisseur de banque de messages a la responsabilité ultime de définition. Par conséquent, si un client envoie un message sans définir sa classe de message, le fournisseur de banque de message lui affecte la valeur par défaut appropriée pour le type de client approprié. La classe de message par défaut pour les clients de messagerie interpersonnels est **IPM**; la classe de message par défaut pour les clients de communication interprocessus est **IPC**. 
  
Classes de message ont une restriction sur la longueur de 255 caractères. Toutefois, les classes de message ne doivent pas dépasser 127 caractères pour prendre en charge les classes de message utilisés dans les rapports. Classes de messages de rapport sont basées sur la classe du message d’origine, avec deux ajouts : un préfixe et un suffixe. Le préfixe de rapport indique que le message est un rapport, et le suffixe indique le type de rapport : DR (rapport de remise), un rapport de non-remise (rapport de non-remise), IPNRN (état de lecture) ou IPNNRN (état nonread). Notez que ces restrictions de longueur sont indiquées dans les caractères ; sur les plateformes qui utilisent un jeu de caractères codés sur deux octets, le nombre d’octets réel peut être plus élevé. 
  
Fournisseurs de magasins de message doivent retourner MAPI_E_INVALID_PARAMETER de leurs implémentations de méthode [IMAPIProp::SetProps](imapiprop-setprops.md) lorsqu’un client tente d’assigner une chaîne qui dépasse la limite autorisée pour leur classe de message. 
  
## <a name="see-also"></a>Voir aussi



[Messages MAPI](mapi-messages.md)

