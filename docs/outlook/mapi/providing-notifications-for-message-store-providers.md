---
title: Fournir des Notifications pour les fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3abb4ba67ff5f0cf2284fa9286b6968698877b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786956"
---
# <a name="providing-notifications-for-message-store-providers"></a>Fournir des Notifications pour les fournisseurs de banque de messages

  
  
**S’applique à**: Outlook 
  
Alors que les notifications sont facultatives, ils sont un composant essentiel d’un fournisseur de magasin de message bonne. Les applications clientes et le spouleur MAPI s’appuient sur les notifications à partir du fournisseur de banque de messages pour obtenir de bonnes performances lors de l’envoi de messages sortants ou la réception de messages entrants. Clients et le spouleur MAPI peuvent fonctionner sans recevoir des notifications à partir du fournisseur de banque de messages, mais ils ne seront pas en mesure d’informer les utilisateurs des modifications dans la banque de messages sans les. En règle générale, cela signifie que les utilisateurs ne pourront pas savoir qu’un nouveau message est arrivé jusqu'à ce que le client suivant pour ouvrir la banque de messages reçoivent dossier.
  
Clients s’inscrire pour les notifications en appelant la méthode [IMsgStore::Advise](imsgstore-advise.md) . Le client transmet une [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) de l’interface, un masque de bits qui indique le type de notifications le client est intéressé par la réception, et un **ID d’entrée** qui indique quel objet dans le message stocker les **notifications** demande s’applique à. Lorsque des événements pertinents se produisent dans l’objet (par exemple, lorsqu’un nouveau message arrive dans le dossier de réception dans la banque de messages), le fournisseur de banque de message ou de l’objet lui-même doit appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour tous les ** IMAPIAdviseSink** les objets qui se sont inscrits pour ce type d’événement. 
  
Même si la base de vos messages fournisseur avertit jamais autres composants MAPI des modifications dans la banque de messages, qu'il doit toujours implémenter **IMsgStore::Advise** pour retourner MAPI_E_NO_SUPPORT. Cela informe les autres composants ne pas pour attendre le fournisseur de magasins de notifications à partir du message. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

