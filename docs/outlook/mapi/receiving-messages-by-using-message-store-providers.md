---
title: Réception de messages à l'aide de fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418728"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Réception de messages à l'aide de fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de banques de messages ne doivent pas prendre en charge les envois de messages entrants (autrement dit, prendre en charge la possibilité pour les fournisseurs de transport et le spouleur MAPI d'utiliser le fournisseur de banques de messages comme point de remise pour les messages). Toutefois, si votre fournisseur de banque de messages ne prend pas en charge les envois de messages entrants, il ne peut pas être utilisé comme banque de messages par défaut.
  
Pour prendre en charge les envois de messages entrants, votre fournisseur de banque de messages doit effectuer les opérations suivantes:
  
- Prendre en charge les méthodes [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) et [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) afin que les applications clientes puissent trouver les messages entrants. 
    
- Prendre en charge la méthode [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) afin que le spouleur MAPI puisse informer le fournisseur de banque de messages qu'un nouveau message est arrivé. 
    
- Implémenter des notifications afin que les clients puissent s'inscrire pour recevoir des notifications de nouveau message. Les notifications sont facultatives, mais votre fournisseur doit les implémenter.
    
La séquence des appels de méthode qui se produit lorsqu'un message entrant est remis à une banque de messages est la suivante:
  
1. Le spouleur MAPI appelle [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec l' [EntryID](entryid.md) de la boîte de réception pour obtenir une interface [IMAPIFolder](imapifolderimapicontainer.md) . 
    
2. Le spouleur MAPI appelle [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) pour obtenir un nouvel objet message. 
    
3. Le spouleur MAPI transmet l'objet message au fournisseur de transport.
    
4. Le fournisseur de transport remplit les propriétés du message avec des données du système de messagerie sous-jacent et appelle la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de l'objet message. 
    
5. Le fournisseur de banque de messages utilise sa méthode de notification pour informer les clients inscrits qu'un nouveau message est arrivé.
    
6. Le spouleur MAPI appelle la méthode [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) de la Banque de messages. 
    
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

