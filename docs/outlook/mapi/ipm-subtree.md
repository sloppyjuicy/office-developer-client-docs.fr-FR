---
title: Sous-arborescence IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317107"
---
# <a name="ipm-subtree"></a>Sous-arborescence IPM

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI crée une arborescence de dossiers sous le dossier racine d'une banque de messages pour tous les clients qui envoient et reçoivent des messages provenant de personnes, et non de destinataires. Les messages échangés entre les destinataires humains sont appelés messages interpersonnels et cet arbre est appelé message interpersonnel ou IPM, sous-arborescence. 
  
Une sous-arborescence IPM pour un magasin de remise se compose au moins des dossiers suivants:
  
- Boîte de réception
    
- Boîte d'envoi
    
- Éléments envoyés
    
- Éléments supprimés
    
Il s'agit des noms et des rôles par défaut pour chacun de ces dossiers; un client peut spécifier ses propres noms si les noms par défaut ne sont pas appropriés. MAPI affecte des noms et des associations par défaut pour ces dossiers de sorte que les messages ne soient pas dévisibles par inadvertance si un client omet d'établir des dossiers de réception pour les messages. 
  
Dans un contexte Microsoft Office Outlook, une sous-arborescence IPM est constituée de dossiers par défaut supplémentaires pour le calendrier, les contacts, les tâches, les notes et le journal.
  
La boîte de réception contient généralement des messages entrants et la boîte d'envoi conserve les messages sortants (c'est-à-dire, les messages en attente d'envoi). Le dossier éléments envoyés contient une copie de chaque message envoyé si le client a défini la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) à l'identificateur d'entrée de ce dossier. Le dossier éléments supprimés contient les messages marqués pour suppression. 
  
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

