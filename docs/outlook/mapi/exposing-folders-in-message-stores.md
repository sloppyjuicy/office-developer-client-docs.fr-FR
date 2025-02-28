---
title: Exposition de dossiers des banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
ms.openlocfilehash: b0e2c4c0ca18755aa32d9f95c93164a5f4107b97
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521546"
---
# <a name="exposing-folders-in-message-stores"></a>Exposition des dossiers dans des banques de messages

**S’applique à** : Outlook 2013 | Outlook 2016
  
Tous les fournisseurs de banques de messages doivent présenter une interface [IMAPIFolder](imapifolderimapicontainer.md) de niveau supérieur aux applications clientes. Le dossier de niveau supérieur correspond à la banque de messages dans son ensemble et permet d’accéder aux dossiers que les utilisateurs visualisent en tant que contenus de la banque de messages. Par ailleurs, le dossier de niveau supérieur est souvent utilisé comme dossier de réception par défaut pour les messages IPC et comme dossier à partir duquel les rapports de lecture sont envoyés. Les fournisseurs de banques de messages doivent également présenter une sous-arborescence IPM (ensemble de dossiers utilisés pour contenir des messages IPM) aux applications clientes.
  
Les applications clientes peuvent ouvrir le dossier de niveau supérieur en appelant la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec 0 et NULL pour les paramètres _cbEntryId_ et _lpEntryId_ , respectivement. Dans la plupart des cas, toutefois, les applications clientes ouvrir l'ensemble des dossiers qui contiennent des messages IPM.
  
## <a name="get-a-list-of-folders-in-the-message-stores-ipm-folder-tree"></a>Obtenir la liste des dossiers dans l’arborescence de dossiers IPM de la boutique de messages
  
1. Utilisez votre session MAPI pour appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).

2. Utilisez le pointeur de base de données de messages qui en résulte afin d’appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).

3. Appelez la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l’identificateur d’entrée pour obtenir un pointeur **IMAPIFolder**.

4. Appelez la m�thode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) pour obtenir une table du contenu du dossier.

5. Appelez la m�thode [IMAPITable::QueryRows](imapitable-queryrows.md) pour r�pertorier les dossiers dans le dossier de niveau sup�rieur.

Les clients MAPI utilisent ces dossiers pour accéder à d’autres objets de dossier et objets de message dans la banque de messages. **IMAPIFolder** et son interface parent [IMAPIContainer](imapicontainerimapiprop.md) contiennent les méthodes que votre fournisseur de banques de messages doit implémenter pour remplir les dossiers avec des objets de message et répondre aux demandes de client à appliquer sur les messages.
  
## <a name="see-also"></a>Voir aussi

[Implémentation de dossiers dans des banques de messages](implementing-folders-in-message-stores.md)
