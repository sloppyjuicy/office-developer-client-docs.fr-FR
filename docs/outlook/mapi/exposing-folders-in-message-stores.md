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
ms.openlocfilehash: 0e7b479931b6b2b00dd3927133187fe058b4c6e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783265"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="c8d2a-103">Exposition de dossiers des banques de messages</span><span class="sxs-lookup"><span data-stu-id="c8d2a-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="c8d2a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8d2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8d2a-p101">Chaque fournisseur de banque de messages doit pr�senter une interface [IMAPIFolder](imapifolderimapicontainer.md) de niveau sup�rieur pour les applications clientes. Le dossier de niveau sup�rieur correspond au magasin de l'int�gralit� du message ; Il fournit l'acc�s aux dossiers que les utilisateurs voient en tant que le contenu de la banque de messages. En outre, le dossier de niveau sup�rieur est souvent utilis� comme dossier pour les messages IPC et que le dossier de r�ception par d�faut � partir de laquelle lire les rapports sont envoy�s. Les fournisseurs de banque de message doivent �galement pr�senter une sous-arborescence IPM � un ensemble de dossiers utilis� pour contenir des messages IPM � pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="c8d2a-p101">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="c8d2a-p102">Les applications clientes peuvent ouvrir le dossier de niveau sup�rieur en appelant la m�thode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec 0 et la valeur NULL pour les param�tres  _cbEntryId_ et  _lpEntryId_, respectivement. Dans la plupart des cas, toutefois, les applications clientes ouvrir l'ensemble des dossiers qui contiennent des messages IPM.</span><span class="sxs-lookup"><span data-stu-id="c8d2a-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="c8d2a-111">Pour obtenir une liste de dossiers dans l'arborescence de dossiers de la banque de messages IPM, utilisez la proc�dure suivante :</span><span class="sxs-lookup"><span data-stu-id="c8d2a-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="c8d2a-112">Utilisez votre session MAPI pour appeler la m�thode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="c8d2a-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="c8d2a-113">Utilisez le pointeur de base de données de message qui en résulte pour appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c8d2a-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="c8d2a-114">Appelez la m�thode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l'identificateur d'entr�e pour obtenir un pointeur **IMAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="c8d2a-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="c8d2a-115">Appelez la m�thode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) pour obtenir une table du contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="c8d2a-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="c8d2a-116">Appelez la m�thode [IMAPITable::QueryRows](imapitable-queryrows.md) pour r�pertorier les dossiers dans le dossier de niveau sup�rieur.</span><span class="sxs-lookup"><span data-stu-id="c8d2a-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="c8d2a-p103">Clients MAPI utilisent ces dossiers pour acc�der aux autres objets folder et les objets de message dans la banque de messages. **IMAPIFolder**et son interface parente [IMAPIContainer](imapicontainerimapiprop.md), contiennent les m�thodes que votre fournisseur de banque de messages doit impl�menter pour remplir des dossiers avec des objets de message et r�pondre aux demandes des clients pour fonctionner sur des messages.</span><span class="sxs-lookup"><span data-stu-id="c8d2a-p103">MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8d2a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8d2a-119">See also</span></span>



[<span data-ttu-id="c8d2a-120">Impl�mentation de dossiers dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="c8d2a-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

