---
title: Arrêt d’un fournisseur de services
description: Décrit les méthodes appelées MAPI lorsqu’un client appelle la méthode IMAPISession::Logoff pour mettre fin à la session et arrêter tous les fournisseurs de services actifs.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
ms.openlocfilehash: b1e97c7c59b128f02734704095832d196f1a3977
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894228"
---
# <a name="shutting-down-a-service-provider"></a>Arrêt d’un fournisseur de services

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) pour mettre fin à la session et arrêter tous les fournisseurs de services actifs, MAPI appelle à son tour les méthodes suivantes : 
  
- [IABLogon::Logoff](iablogon-logoff.md) pour les fournisseurs de carnets d’adresses. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) pour les fournisseurs de magasin de messages. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) pour les fournisseurs de transport. 
    
Ces méthodes ont des implémentations similaires. Les principales tâches effectuées par une méthode de fermeture de session sont les suivantes :
  
- Libération de tous les objets ouverts, y compris les sous-objets et les objets d’état.
    
- Appel de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de support pour décrémenter son nombre de références. 
    
- Suppression de toutes les structures [MAPIUID](mapiuid.md) inscrites de votre fournisseur. 
    
- Suppression de la ligne de votre fournisseur dans la table d’état.
    
- Effectuer toutes les tâches liées au nettoyage des ressources, telles que les suivantes :
    
  - Arrêt d’une connexion avec un serveur distant.
    
  - Décrémentation du nombre de références sur l’objet d’ouverture de session.
    
  - Suppression de l’objet d’ouverture de session de la liste des objets d’ouverture de session stockés par votre fournisseur.
    
  - En mode débogage, en émettant des traces pour localiser les objets qui ont perdu de la mémoire.
    
Lorsque votre méthode de fermeture de session est retournée, MAPI appelle les éléments suivants :
  
- Méthode **IUnknown::Release** de votre objet d’ouverture de session. 
    
- Méthode **d’arrêt** de l’objet fournisseur pour effectuer toutes les tâches de nettoyage finales. Selon le type de votre fournisseur, l’une des méthodes suivantes est appelée : 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) pour les fournisseurs de carnets d’adresses 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) pour les fournisseurs de magasins de messages 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) pour les fournisseurs de transport 
    
- Méthode **IUnknown::Release** de l’objet fournisseur. 
    
Si votre fournisseur est un magasin de messages, un appel client à [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) lance également le processus d’arrêt. **StoreLogoff** arrête un fournisseur de magasin de messages particulier et n’a aucun effet sur la session. Seul un fournisseur de magasin de messages peut être arrêté avec cette méthode ; il n’existe aucun moyen explicite d’arrêter un carnet d’adresses ou un fournisseur de transport particulier. Pour plus d’informations sur la façon de répondre à un appel **StoreLogoff** , consultez [Arrêter un fournisseur de magasin](shutting-down-a-message-store-provider.md) de messages.
  
La DLL de votre fournisseur est déchargée lorsque MAPI appelle la fonction d’API Win32 **FreeLibrary**, un appel effectué après que le dernier client actif a appelé [MAPIUninitialize](mapiuninitialize.md). À ce stade, votre fournisseur de services aura terminé l’arrêt. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

