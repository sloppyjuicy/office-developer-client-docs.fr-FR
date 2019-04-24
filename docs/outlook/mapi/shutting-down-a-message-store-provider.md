---
title: Arrêt d'un fournisseur de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339199"
---
# <a name="shutting-down-a-message-store-provider"></a>Arrêt d'un fournisseur de banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si votre fournisseur est un fournisseur de banque de messages, il peut être arrêté de l'une des manières suivantes:
  
- Lorsqu'un client ou le spouleur MAPI appelle [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md). L'arrêt d'un fournisseur de banque de messages avec **StoreLogoff** entraîne l'arrêt de manière ordonnée et contrôlée. 
    
- Lorsqu'un client appelle [IMAPISession:: Logoff](imapisession-logoff.md). 
    
Votre implémentation de **IMsgStore:: StoreLogoff** doit commencer par appeler [IMAPISupport:: STORELOGOFFTRANSPORTS](imapisupport-storelogofftransports.md) pour informer MAPI qu'il est arrêté, ce qui indique que tous les fournisseurs de transport liés doivent être déconnectés. Lorsque **IMsgStore:: StoreLogoff** renvoie, son appelant appelle la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de votre magasin de messages. Implémentez cette méthode de **publication** en appelant la méthode **IUnknown:: Release** de l'objet de prise en charge. 
  
MAPI effectue les tâches suivantes dans son implémentation de **IUnknown:: Release** pour les banques de messages: 
  
1. Supprime toutes les structures [MAPIUID](mapiuid.md) enregistrées par le fournisseur de banque de messages. 
    
2. Supprime la ligne du fournisseur de banque de messages de la table d'État.
    
3. Appelle [IMSLogon:: Logoff](imslogon-logoff.md) pour libérer tous les objets ouverts, les sous-objets et les objets d'État. 
    
4. Appelle [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer l'objet de connexion du fournisseur de banque de messages. 
    
Certains clients peuvent omettre l'appel à **IMsgStore:: StoreLogoff**, en lançant l'arrêt de votre fournisseur de banque de messages avec l'appel à la méthode **IUnknown:: Release** de la Banque de messages. Un arrêt dans ces circonstances sans l'appel vers **StoreLogoff** est moins ordonné et contrôlé. Écrivez la méthode de **publication** de votre banque de messages pour gérer cette possibilité et effectuer le suivi de la présence ou non d'un appel à **IMAPISupport:: StoreLogoffTransports** . **StoreLogoffTransports** doit être appelé une fois au cours du processus d'arrêt. Si vous détectez, dans votre méthode de **publication** , que **StoreLogoffTransports** n'a pas encore été appelé, appelez-le avec l'indicateur LOGOFF_ABORT. 
  
## <a name="see-also"></a>Voir aussi



[Arrêt d'un fournisseur de services](shutting-down-a-service-provider.md)

