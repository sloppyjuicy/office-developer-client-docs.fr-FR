---
title: Arrêt d’un fournisseur de services
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339206"
---
# <a name="shutting-down-a-service-provider"></a>Arrêt d’un fournisseur de services

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) pour mettre fin à la session et arrêter tous les fournisseurs de services actifs, MAPI appelle à son tour les méthodes suivantes : 
  
- [IABLogon::Logoff](iablogon-logoff.md) pour les fournisseurs de carnet d’adresses. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) pour les fournisseurs de magasins de messages. 
    
- [IXPLogon::TransportLogoff pour](ixplogon-transportlogoff.md) les fournisseurs de transport. 
    
Ces méthodes ont des implémentations similaires. Les principales tâches effectuées par une méthode de ff de logo sont les suivantes :
  
- Libération de tous les objets ouverts, y compris les sous-objets et les objets d’état.
    
- Appel de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de support pour décrémenter son nombre de références. 
    
- Suppression de toutes les structures [MAPIUID](mapiuid.md) inscrites de votre fournisseur. 
    
- Suppression de la ligne de votre fournisseur dans la table d’état.
    
- Effectuer toutes les tâches liées au nettoyage des ressources, telles que les suivantes :
    
  - Arrêt d’une connexion avec un serveur distant.
    
  - Décrémentation du nombre de références sur l’objet d’logon.
    
  - Suppression de l’objet d' logon dans la liste des objets d' logo que votre fournisseur stocke.
    
  - En mode débogage, émission de suivis pour localiser les objets dont la mémoire a été divulguée.
    
Lorsque votre méthode de ff de logo renvoie, MAPI appelle les appels suivants :
  
- Méthode **IUnknown::Release** de votre objet d’logo. 
    
- Méthode d’arrêt **de** votre objet fournisseur pour effectuer les tâches de nettoyage finales. Selon le type de votre fournisseur, l’une des méthodes suivantes est appelée : 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) pour les fournisseurs de carnets d’adresses 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) pour les fournisseurs de magasins de messages 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) pour les fournisseurs de transport 
    
- Méthode **IUnknown::Release** de votre objet fournisseur. 
    
Si votre fournisseur est un magasin de messages, un appel client à [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) lancera également le processus d’arrêt. **StoreLogoff** arrête un fournisseur de magasin de messages particulier et n’a aucun effet sur la session. Seul un fournisseur de magasin de messages peut être arrêté avec cette méthode ; il n’existe aucun moyen explicite d’arrêter un carnet d’adresses ou un fournisseur de transport particulier. Pour plus d’informations sur la réponse à un appel **StoreLogoff,** voir [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).
  
La DLL de votre fournisseur sera déchargée lorsque MAPI appelle la fonction API Win32 **FreeLibrary**, un appel effectué après que le dernier client actif a appelé [MAPIUninitialize](mapiuninitialize.md). À ce moment-là, votre fournisseur de services aura fini de s’arrêter. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

