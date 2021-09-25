---
title: Sous-arbre IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 89f29feffa4cbcfc5a9b4351f12d616ae45532c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561410"
---
# <a name="ipm-subtree"></a>Sous-arbre IPM

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI crée une arborescence de dossiers sous le dossier racine d’une magasin de messages pour tous les clients qui envoient et reçoivent des messages à partir de destinataires humains, plutôt que d’ordinateurs. Les messages échangés entre des destinataires humains sont appelés messages interpersonnels, et cette arborescence est appelée sous-arborescence de message interpersonnel( IPM). 
  
Une sous-arbre IPM pour un magasin de remise se compose au moins des dossiers suivants :
  
- Boîte de réception
    
- Boîte d’envoi
    
- Éléments envoyés
    
- Éléments supprimés
    
Voici les noms et rôles par défaut pour chacun de ces dossiers ; un client peut spécifier ses propres noms si les noms par défaut ne sont pas appropriés. MAPI affecte des noms et des associations par défaut pour ces dossiers afin que les messages ne disparaissent pas par inadvertance si un client oublie d’établir des dossiers de réception pour les messages. 
  
Dans un contexte Microsoft Office Outlook, une sous-arbre IPM se compose de dossiers par défaut supplémentaires pour le calendrier, les contacts, les tâches, les notes et le journal.
  
La boîte de réception contient généralement les messages entrants et la boîte d’envoi contient les messages sortants (c’est-à-dire, les messages en attente d’envoi). Le dossier Éléments envoyés contient une copie de chaque message envoyé si le client a définie la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sur l’identificateur d’entrée de ce dossier. Le dossier Éléments supprimés contient les messages marqués pour suppression. 
  
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

