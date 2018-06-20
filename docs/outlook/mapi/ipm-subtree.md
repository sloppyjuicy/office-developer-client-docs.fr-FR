---
title: Sous-arborescence IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: eebc029d4ed72f355170710061c4d3717ed0aa1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784363"
---
# <a name="ipm-subtree"></a>Sous-arborescence IPM

  
  
**S’applique à**: Outlook 
  
MAPI crée une arborescence de dossiers sous le dossier racine d’une banque de messages pour envoyant des messages et de recevoir des messages à partir de humaine, plutôt qu’ordinateur, destinataires de tous les clients. Les messages échangés entre les destinataires humaines sont appelés des messages interpersonnels et cette arborescence est connue en tant que message interpersonnel ou IPM, la sous-arborescence. 
  
Une sous-arborescence IPM pour une banque de remise comprend au moins les dossiers suivants :
  
- Inbox
    
- La boîte d’envoi
    
- Éléments envoyés
    
- Éléments supprimés
    
Ce sont les noms par défaut et les rôles pour chacun de ces dossiers ; un client peut spécifier ses propres noms si les noms par défaut ne sont pas appropriés. MAPI attribue des noms par défaut et associations pour ces dossiers pour conserver les messages de disparaître par inadvertance si un client oublie à établir les dossiers de réception des messages. 
  
Dans un contexte de Microsoft Office Outlook, une sous-arborescence IPM se compose des dossiers par défaut supplémentaires pour le calendrier, Contacts, tâches, Notes et Journal.
  
La boîte de réception conserve généralement les messages entrants et la boîte d’envoi conserve les messages sortants (autrement dit, les messages en attente d’être envoyés). Le dossier éléments envoyés conserve une copie de chaque message envoyé si le client a défini la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) à l’identificateur d’entrée de ce dossier. Le dossier éléments supprimés contient les messages marqués pour suppression. 
  
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

