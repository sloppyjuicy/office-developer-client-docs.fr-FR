---
title: Fourniture de notifications pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
ms.openlocfilehash: 731c9996c560fc7c7d818503cd3d2b6d2e75ac7f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373913"
---
# <a name="providing-notifications-for-message-store-providers"></a>Fourniture de notifications pour les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Bien que les notifications soient facultatives, elles sont une partie très importante d’un bon fournisseur de magasins de messages. Les applications clientes et lepooler MAPI s’appuient sur les notifications du fournisseur de magasin de messages pour obtenir de bonnes performances lors de l’envoi de messages sortants ou de la réception de messages entrants. Les clients et lepooler MAPI peuvent fonctionner sans recevoir de notifications du fournisseur de la boutique de messages, mais ils ne pourront pas informer les utilisateurs des modifications apportées à la magasin de messages sans eux. En règle générale, cela signifie que les utilisateurs ne pourront pas voir qu’un nouveau message est arrivé tant que leur client n’a pas ouvert le dossier de réception de la boutique de messages.
  
Les clients s’inscrivent pour recevoir des notifications en appelant la méthode [IMsgStore::Advise](imsgstore-advise.md) . Le client transmet une interface [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) , un masque de bits qui indique le type de notifications que le client est intéressé par la réception et un **EntryID** qui indique l’objet dans la boutique de messages auquel la demande **de** conseil s’applique. Lorsque des événements pertinents se produisent dans l’objet (par exemple, lorsqu’un nouveau message arrive dans le dossier de réception de la boutique de messages), le fournisseur de la boutique de messages ou l’objet lui-même doit appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour tous les objets **IMAPIAdviseSink** qui ont été inscrits pour ce type d’événement. 
  
Même si votre fournisseur de magasin de messages n’avertit jamais les autres composants MAPI des modifications apportées à la magasin de messages, il doit toujours implémenter **IMsgStore::Advise** pour renvoyer MAPI_E_NO_SUPPORT. Cela informe les autres composants de ne pas s’attendre à recevoir de notifications du fournisseur de la boutique de messages. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

