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
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="79d8c-103">Exposition des dossiers dans des banques de messages</span><span class="sxs-lookup"><span data-stu-id="79d8c-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="79d8c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79d8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79d8c-p101">Tous les fournisseurs de banques de messages doivent présenter une interface [IMAPIFolder](imapifolderimapicontainer.md) de niveau supérieur aux applications clientes. Le dossier de niveau supérieur correspond à la banque de messages dans son ensemble et permet d’accéder aux dossiers que les utilisateurs visualisent en tant que contenus de la banque de messages. Par ailleurs, le dossier de niveau supérieur est souvent utilisé comme dossier de réception par défaut pour les messages IPC et comme dossier à partir duquel les rapports de lecture sont envoyés. Les fournisseurs de banques de messages doivent également présenter une sous-arborescence IPM (ensemble de dossiers utilisés pour contenir des messages IPM) aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="79d8c-p101">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="79d8c-p102">Les applications clientes peuvent ouvrir le dossier de niveau supérieur en appelant la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec les valeurs 0 et NULL pour les paramètres _cbEntryId_ et _lpEntryId_ respectivement. Dans la plupart des cas, toutefois, les applications clientes ouvrent l’ensemble de dossiers contenant des messages IPM.</span><span class="sxs-lookup"><span data-stu-id="79d8c-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="79d8c-111">Pour obtenir la liste des dossiers figurant dans l’arborescence des dossiers IPM de la banque de messages, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="79d8c-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="79d8c-112">Utilisez votre session MAPI pour appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="79d8c-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="79d8c-113">Utilisez le pointeur de base de données de messages qui en résulte afin d’appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="79d8c-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="79d8c-114">Appelez la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l’identificateur d’entrée pour obtenir un pointeur **IMAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="79d8c-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="79d8c-115">Appelez la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) pour obtenir une table des matières du dossier.</span><span class="sxs-lookup"><span data-stu-id="79d8c-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="79d8c-116">Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) pour répertorier les dossiers dans le dossier de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="79d8c-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="79d8c-p103">Les clients MAPI utilisent ces dossiers pour accéder à d’autres objets de dossier et objets de message dans la banque de messages. **IMAPIFolder** et son interface parent [IMAPIContainer](imapicontainerimapiprop.md) contiennent les méthodes que votre fournisseur de banques de messages doit implémenter pour remplir les dossiers avec des objets de message et répondre aux demandes de client à appliquer sur les messages.</span><span class="sxs-lookup"><span data-stu-id="79d8c-p103">MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79d8c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79d8c-119">See also</span></span>



[<span data-ttu-id="79d8c-120">Implémentation de dossiers dans des banques de messages</span><span class="sxs-lookup"><span data-stu-id="79d8c-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

