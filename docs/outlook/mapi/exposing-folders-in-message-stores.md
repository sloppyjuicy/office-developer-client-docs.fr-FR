---
title: Exposition de dossiers des banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582594"
---
# <a name="exposing-folders-in-message-stores"></a>Exposition de dossiers des banques de messages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Chaque fournisseur de banque de messages doit pr�senter une interface [IMAPIFolder](imapifolderimapicontainer.md) de niveau sup�rieur pour les applications clientes. Le dossier de niveau sup�rieur correspond au magasin de l'int�gralit� du message ; Il fournit l'acc�s aux dossiers que les utilisateurs voient en tant que le contenu de la banque de messages. En outre, le dossier de niveau sup�rieur est souvent utilis� comme dossier pour les messages IPC et que le dossier de r�ception par d�faut � partir de laquelle lire les rapports sont envoy�s. Les fournisseurs de banque de message doivent �galement pr�senter une sous-arborescence IPM � un ensemble de dossiers utilis� pour contenir des messages IPM � pour les applications clientes. 
  
Les applications clientes peuvent ouvrir le dossier de niveau sup�rieur en appelant la m�thode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec 0 et la valeur NULL pour les param�tres  _cbEntryId_ et  _lpEntryId_, respectivement. Dans la plupart des cas, toutefois, les applications clientes ouvrir l'ensemble des dossiers qui contiennent des messages IPM. 
  
Pour obtenir une liste de dossiers dans l'arborescence de dossiers de la banque de messages IPM, utilisez la proc�dure suivante :
  
1. Utilisez votre session MAPI pour appeler la m�thode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
    
2. Utilisez le pointeur de base de données de message qui en résulte pour appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. Appelez la m�thode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l'identificateur d'entr�e pour obtenir un pointeur **IMAPIFolder**. 
    
4. Appelez la m�thode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) pour obtenir une table du contenu du dossier. 
    
5. Appelez la m�thode [IMAPITable::QueryRows](imapitable-queryrows.md) pour r�pertorier les dossiers dans le dossier de niveau sup�rieur. 
    
Clients MAPI utilisent ces dossiers pour acc�der aux autres objets folder et les objets de message dans la banque de messages. **IMAPIFolder**et son interface parente [IMAPIContainer](imapicontainerimapiprop.md), contiennent les m�thodes que votre fournisseur de banque de messages doit impl�menter pour remplir des dossiers avec des objets de message et r�pondre aux demandes des clients pour fonctionner sur des messages.
  
## <a name="see-also"></a>Voir aussi



[Impl�mentation de dossiers dans les banques de messages](implementing-folders-in-message-stores.md)

