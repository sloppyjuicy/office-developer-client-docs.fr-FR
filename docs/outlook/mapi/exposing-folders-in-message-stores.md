---
title: Exposition des dossiers dans des banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 457620dd0f805e78d12fc8feba09f8fc8aedc554
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341348"
---
# <a name="exposing-folders-in-message-stores"></a>Exposition des dossiers dans des banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de banques de messages doivent présenter une interface [IMAPIFolder](imapifolderimapicontainer.md) de niveau supérieur aux applications clientes. Le dossier de niveau supérieur correspond à la banque de messages dans son ensemble et permet d’accéder aux dossiers que les utilisateurs visualisent en tant que contenus de la banque de messages. Par ailleurs, le dossier de niveau supérieur est souvent utilisé comme dossier de réception par défaut pour les messages IPC et comme dossier à partir duquel les rapports de lecture sont envoyés. Les fournisseurs de banques de messages doivent également présenter une sous-arborescence IPM (ensemble de dossiers utilisés pour contenir des messages IPM) aux applications clientes. 
  
Les applications clientes peuvent ouvrir le dossier de niveau supérieur en appelant la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec les valeurs 0 et NULL pour les paramètres _cbEntryId_ et _lpEntryId_ respectivement. Dans la plupart des cas, toutefois, les applications clientes ouvrent l’ensemble de dossiers contenant des messages IPM. 
  
Pour obtenir la liste des dossiers figurant dans l’arborescence des dossiers IPM de la banque de messages, procédez comme suit :
  
1. Utilisez votre session MAPI pour appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). 
    
2. Utilisez le pointeur de base de données de messages qui en résulte afin d’appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. Appelez la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l’identificateur d’entrée pour obtenir un pointeur **IMAPIFolder**. 
    
4. Appelez la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) pour obtenir une table des matières du dossier. 
    
5. Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) pour répertorier les dossiers dans le dossier de niveau supérieur. 
    
Les clients MAPI utilisent ces dossiers pour accéder à d’autres objets de dossier et objets de message dans la banque de messages. **IMAPIFolder** et son interface parent [IMAPIContainer](imapicontainerimapiprop.md) contiennent les méthodes que votre fournisseur de banques de messages doit implémenter pour remplir les dossiers avec des objets de message et répondre aux demandes de client à appliquer sur les messages.
  
## <a name="see-also"></a>Voir aussi



[Implémentation de dossiers dans des banques de messages](implementing-folders-in-message-stores.md)

