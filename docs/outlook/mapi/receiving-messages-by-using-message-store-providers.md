---
title: Réception de messages à l’aide de fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8a5df2e8f50d8de05ec43b03ae5b56887e76d505
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590189"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Réception de messages à l’aide de fournisseurs de banques de messages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournisseurs de banque de messages n’ont pas prendre en charge les envois de messages entrants (autrement dit, prennent en charge la possibilité pour les fournisseurs de transport et le spouleur MAPI à utiliser le message d’un fournisseur de magasins comme point de remise des messages). Toutefois, si votre fournisseur de banque de messages n’accepte pas les envois de messages entrants, il ne peut être utilisé en tant que la banque de messages par défaut.
  
Pour prendre en charge les envois de messages entrants, votre fournisseur de magasin de message procédez comme suit :
  
- Prend en charge les méthodes [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) et [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) afin que les applications clientes peuvent trouver les messages entrants. 
    
- Prend en charge la méthode [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) afin que le spouleur MAPI peut indiquer le fournisseur de banque de messages un nouveau message est arrivé. 
    
- Implémenter des notifications de sorte que les clients peuvent s’inscrire pour la notification de nouveau message. Les notifications sont facultatifs, mais votre fournisseur doit les implémenter.
    
La séquence d’appels de méthode qui se produit lorsqu’un message entrant est remis à une banque de messages est la suivante :
  
1. Le spouleur MAPI appelle [IMsgStore::OpenEntry](imsgstore-openentry.md) avec boîte de réception [EntryID](entryid.md) pour obtenir une interface [IMAPIFolder](imapifolderimapicontainer.md) . 
    
2. Le spouleur MAPI appelle [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour obtenir un nouvel objet de message. 
    
3. Le spouleur MAPI passe l’objet de message pour le fournisseur de transport.
    
4. Le fournisseur de transport remplit les propriétés de message avec des données à partir du système de messagerie sous-jacent et appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de l’objet message. 
    
5. Le fournisseur de banque de message utilise la méthode de notification pour informer les clients inscrits qu’un nouveau message est arrivé.
    
6. Le spouleur MAPI appelle la méthode de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) de la banque de messages. 
    
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

