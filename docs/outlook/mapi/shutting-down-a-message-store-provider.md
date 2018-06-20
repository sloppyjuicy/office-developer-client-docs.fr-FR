---
title: Arrêt d’un fournisseur de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b5c9874ca465bb0ebed62f218d1512feb1a2f9ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787163"
---
# <a name="shutting-down-a-message-store-provider"></a>Arrêt d’un fournisseur de banque de messages

  
  
**S’applique à**: Outlook 
  
Si votre fournisseur est un fournisseur de magasin de message, il peut être arrêté d’une des manières suivantes :
  
- Lorsqu’un client ou le spouleur MAPI appelle [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). Arrêt d’un fournisseur de banque de messages avec **StoreLogoff** entraîne l’arrêt se produise de manière ordonnée et mieux contrôlée. 
    
- Lorsqu’un client appelle [IMAPISession::Logoff](imapisession-logoff.md). 
    
Votre implémentation de **IMsgStore::StoreLogoff** doit commencer en appelant [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) pour informer MAPI qu’il est arrêté, indiquant que tous les fournisseurs de transport associées doivent être déconnectés. **IMsgStore::StoreLogoff** retourne son appelant appelle la méthode de [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de la banque de messages. Mettre en œuvre cette méthode **version** en appelant la méthode **IUnknown::Release** de l’objet de la prise en charge. 
  
MAPI effectue les tâches suivantes dans son implémentation de **IUnknown::Release** pour les magasins de message : 
  
1. Supprime toutes les structures [MAPIUID](mapiuid.md) enregistrés par le fournisseur de banque de messages. 
    
2. Supprime la ligne du fournisseur de banque de messages à partir de la table d’état.
    
3. Appelle [IMSLogon::Logoff](imslogon-logoff.md) pour libérer tous les objets ouverts, sous-objets et objets d’état. 
    
4. Appelle [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer l’objet de connexion du fournisseur de banque de messages. 
    
Certains clients peuvent omettre l’appel à **IMsgStore::StoreLogoff**, l’arrêt de votre fournisseur de magasin de message avec l’appel de méthode de **IUnknown::Release** de la banque de messages. Un arrêt dans ces circonstances sans l’appel à **StoreLogoff** est moins ordonnée et mieux contrôlée. Écrire la méthode de **publication** de votre banque de messages pour gérer cette possibilité et de garder une trace des ou non un appel à **IMAPISupport::StoreLogoffTransports** s’est produite. **StoreLogoffTransports** doit être appelée qu’une seule fois pendant le processus d’arrêt. Si vous détectez dans votre méthode **version** que **StoreLogoffTransports** n’a pas encore été appelée, l’appel avec l’indicateur LOGOFF_ABORT. 
  
## <a name="see-also"></a>Voir aussi



[Arrêt d’un fournisseur de services](shutting-down-a-service-provider.md)

