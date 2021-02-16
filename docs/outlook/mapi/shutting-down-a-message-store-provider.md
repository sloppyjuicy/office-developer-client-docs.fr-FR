---
title: Arrêt d’un fournisseur de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339199"
---
# <a name="shutting-down-a-message-store-provider"></a>Arrêt d’un fournisseur de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si votre fournisseur est un fournisseur de magasins de messages, il peut être fermé de l’une des manières suivantes :
  
- Lorsqu’un client ou lepooler MAPI appelle [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). L’arrêt d’un fournisseur de magasins de messages avec **StoreLogoff** entraîne l’arrêt de manière ordonnée et contrôlée. 
    
- Lorsqu’un client appelle [IMAPISession::Logoff](imapisession-logoff.md). 
    
Votre implémentation **d’IMsgStore::StoreLogoff** doit commencer par appeler [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) pour informer MAPI qu’il est en cours d’arrêt, indiquant que tous les fournisseurs de transport associés doivent être déconnectés. Lorsque **IMsgStore::StoreLogoff** renvoie, son appelant appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de votre magasin de messages. **Implémentez cette méthode Release** en appelant la méthode **IUnknown::Release** de l’objet de support. 
  
MAPI effectue les tâches suivantes dans son implémentation de **IUnknown::Release** pour les magasins de messages : 
  
1. Supprime toutes les structures [MAPIUID](mapiuid.md) inscrites par le fournisseur de magasins de messages. 
    
2. Supprime la ligne du fournisseur de la boutique de messages de la table d’état.
    
3. Appelle [IMSLogon::Logoff](imslogon-logoff.md) pour libérer tous les objets ouverts, sous-objets et objets d’état. 
    
4. Appelle [IUnknown::Release pour](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) libérer l’objet d’ouverture de messagerie du fournisseur de magasins de messages. 
    
Certains clients peuvent omettre l’appel à **IMsgStore::StoreLogoff**, en initie l’arrêt de votre fournisseur de magasins de messages avec l’appel à la méthode **IUnknown::Release** de la boutique de messages. Un arrêt dans ces circonstances sans l’appel **de StoreLogoff** est moins ordonné et contrôlé. Écrivez la méthode **Release** de votre magasin de messages pour gérer cette possibilité et savoir si un appel à **IMAPISupport::StoreLogoffTransports** s’est produit ou non. **StoreLogoffTransports** doit être appelé une seule fois pendant le processus d’arrêt. Si vous détectez dans votre méthode **Release** que **StoreLogoffTransports** n’a pas encore été appelé, étiquetez-le avec l’LOGOFF_ABORT de publication. 
  
## <a name="see-also"></a>Voir aussi



[Arrêt d’un fournisseur de services](shutting-down-a-service-provider.md)

