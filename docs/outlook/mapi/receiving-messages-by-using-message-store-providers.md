---
title: Réception de messages à l’aide de fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
ms.openlocfilehash: d1228c02d1180c0816dd9e29eea9a50a475f9075
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379065"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Réception de messages à l’aide de fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages n’ont pas besoin de prendre en charge les envois de messages entrants (autrement dit, la prise en charge de la possibilité pour les fournisseurs de transport et lepooler MAPI d’utiliser le fournisseur de magasin de messages comme point de remise pour les messages). Toutefois, si votre fournisseur de magasin de messages ne prend pas en charge les envois de messages entrants, il ne peut pas être utilisé comme magasin de messages par défaut.
  
Pour prendre en charge les envois de messages entrants, votre fournisseur de magasins de messages doit :
  
- Prendre en charge [les méthodes IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) et [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour que les applications clientes trouvent les messages entrants. 
    
- Prise en charge de la méthode [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) afin que lepooler MAPI puisse informer le fournisseur de la boutique de messages qu’un nouveau message est arrivé. 
    
- Implémentez des notifications afin que les clients peuvent s’inscrire à la nouvelle notification de message. Les notifications sont facultatives, mais votre fournisseur doit les implémenter.
    
La séquence d’appels de méthode qui se produit lorsqu’un message entrant est remis à une magasin de messages est la suivante :
  
1. Lepooler MAPI appelle [IMsgStore::OpenEntry](imsgstore-openentry.md) avec [l’ID](entryid.md) d’entrée de boîte de réception pour obtenir une interface [IMAPIFolder](imapifolderimapicontainer.md) . 
    
2. Lepooler MAPI appelle [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour obtenir un nouvel objet message. 
    
3. Lepooler MAPI transmet l’objet message au fournisseur de transport.
    
4. Le fournisseur de transport remplit les propriétés du message avec les données du système de messagerie sous-jacent et appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de l’objet message. 
    
5. Le fournisseur de magasins de messages utilise sa méthode de notification pour informer les clients inscrits qu’un nouveau message est arrivé.
    
6. Lepooler MAPI appelle la méthode [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) de la boutique de messages. 
    
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

