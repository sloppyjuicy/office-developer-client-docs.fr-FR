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
ms.openlocfilehash: 6781209cd1bf87f4becf1893b7cba5618549fbce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582888"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>Bo�te de r�ception et les dossiers des banques de messages de la bo�te d'envoi

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour la banque de messages par d�faut, un fournisseur de banque de messages doit impl�menter la bo�te de r�ception et les dossiers de la bo�te d'envoi. Ils sont g�n�ralement stock�s dans la sous-arborescence IPM d'une banque de messages. Ces dossiers sont sp�ciales dans la mesure o� ils sont d�sign�s comme les dossiers que les messages sont remis aux et envoy�s � partir de, mais aucune fonctionnalit� particuli�re n'on attend d'eux. Envoi et r�ception de messages s'effectue par le biais des s�quences d'appel d�finies entre les applications clientes, le spouleur MAPI et le fournisseur de banque de messages. Les dossiers bo�te de r�ception et d'envoi sont simplement les dossiers qui sont utilis�es pour stocker les messages pendant ces s�quences d'appel. Le point � retenir n'est pas que les dossiers sont sp�ciaux, ou m�me qu'ils sont nomm�s bo�te de r�ception et bo�te d'envoi. le point � retenir est que le fournisseur de banque de messages les utilise dans le cadre de la prise en charge pour l'envoi et r�ception de messages.
  
To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [R�ception de Messages � l'aide de fournisseurs de banque de messages](receiving-messages-by-using-message-store-providers.md).
  
To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Envoi de Messages � l'aide de fournisseurs de banque de messages](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Voir aussi



[Implémentation de dossiers dans des banques de messages](implementing-folders-in-message-stores.md)

