---
title: Fourniture de notifications pour les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419932"
---
# <a name="providing-notifications-for-message-store-providers"></a>Fourniture de notifications pour les fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications sont facultatives, mais elles constituent un élément très important d'un fournisseur de banque de messages approprié. Les applications clientes et le spouleur MAPI s'appuient sur les notifications du fournisseur de banque de messages pour obtenir de bonnes performances lors de l'envoi de messages sortants ou de la réception de messages entrants. Les clients et le spouleur MAPI peuvent fonctionner sans recevoir de notifications du fournisseur de banque de messages, mais ils ne peuvent pas informer les utilisateurs des modifications apportées à la Banque de messages sans eux. En règle générale, cela signifie que les utilisateurs ne pourront pas voir qu'un nouveau message est arrivé jusqu'à ce que son client ouvre le dossier de réception de la Banque de messages.
  
Les clients s'inscrivent pour les notifications en appelant la méthode [IMsgStore:: Advise](imsgstore-advise.md) . Le client transmet une interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) , un masque de masques qui indique le type de notifications que le client souhaite recevoir, et un **EntryID** qui indique quel objet dans la Banque de messages est l' **avis** . demande s'applique à. Lorsque des événements pertinents se produisent dans l'objet (par exemple, lorsqu'un nouveau message arrive dans le dossier de réception dans la Banque de messages), le fournisseur de banque de messages ou l'objet lui-même doit appeler la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour tous les ** Objets IMAPIAdviseSink** qui ont été inscrits pour ce type d'événement. 
  
Même si votre fournisseur de banque de messages n'avertit jamais les autres composants MAPI des modifications apportées à la Banque de messages, il doit toujours implémenter **IMsgStore:: Advise** pour retourner MAPI_E_NO_SUPPORT. Cette fonctionnalité informe les autres composants de ne pas attendre les notifications du fournisseur de banque de messages. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

