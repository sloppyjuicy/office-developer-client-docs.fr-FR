---
title: Bo�te de r�ception et les dossiers des banques de messages de la bo�te d'envoi
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 95a2b7b9bac11404817fb6848d58c45251c141f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309673"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a><span data-ttu-id="eaa39-103">Bo�te de r�ception et les dossiers des banques de messages de la bo�te d'envoi</span><span class="sxs-lookup"><span data-stu-id="eaa39-103">Inbox and Outbox Folders in Message Stores</span></span>

  
  
<span data-ttu-id="eaa39-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaa39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaa39-p101">Pour la banque de messages par d�faut, un fournisseur de banque de messages doit impl�menter la bo�te de r�ception et les dossiers de la bo�te d'envoi. Ils sont g�n�ralement stock�s dans la sous-arborescence IPM d'une banque de messages. Ces dossiers sont sp�ciales dans la mesure o� ils sont d�sign�s comme les dossiers que les messages sont remis aux et envoy�s � partir de, mais aucune fonctionnalit� particuli�re n'on attend d'eux. Envoi et r�ception de messages s'effectue par le biais des s�quences d'appel d�finies entre les applications clientes, le spouleur MAPI et le fournisseur de banque de messages. Les dossiers bo�te de r�ception et d'envoi sont simplement les dossiers qui sont utilis�es pour stocker les messages pendant ces s�quences d'appel. Le point � retenir n'est pas que les dossiers sont sp�ciaux, ou m�me qu'ils sont nomm�s bo�te de r�ception et bo�te d'envoi. le point � retenir est que le fournisseur de banque de messages les utilise dans le cadre de la prise en charge pour l'envoi et r�ception de messages.</span><span class="sxs-lookup"><span data-stu-id="eaa39-p101">To be the default message store, a message store provider must implement Inbox and Outbox folders. They are typically stored in the IPM subtree of a message store. These folders are special in that they are designated as the folders that messages are delivered to and sent from, but no special functionality is required of them. Sending and receiving messages happens by way of defined call sequences between client applications, the MAPI spooler, and the message store provider. The Inbox and Outbox folders are simply folders that are used to hold messages during those call sequences. The important point is not that the folders are special, or even that they are named Inbox and Outbox; the important point is that the message store provider uses them as part of its support for sending and receiving messages.</span></span>
  
<span data-ttu-id="eaa39-p102">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [R�ception de Messages � l'aide de fournisseurs de banque de messages](receiving-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="eaa39-p102">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [Receiving Messages by Using Message Store Providers](receiving-messages-by-using-message-store-providers.md).</span></span>
  
<span data-ttu-id="eaa39-p103">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Envoi de Messages � l'aide de fournisseurs de banque de messages](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="eaa39-p103">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eaa39-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaa39-118">See also</span></span>



[<span data-ttu-id="eaa39-119">Implémentation de dossiers dans des banques de messages</span><span class="sxs-lookup"><span data-stu-id="eaa39-119">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

