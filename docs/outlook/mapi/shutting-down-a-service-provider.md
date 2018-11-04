---
title: Arrêt d’un fournisseur de services
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: 'Dernière modification : 07 décembre 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395174"
---
# <a name="shutting-down-a-service-provider"></a>Arrêt d’un fournisseur de services

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) à la fin de la session et arrêter tous les fournisseurs de service active, MAPI appelle à son tour les méthodes suivantes : 
  
- [IABLogon::Logoff](iablogon-logoff.md) pour les fournisseurs de carnet d’adresses. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) pour les fournisseurs de banque de messages. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) pour les fournisseurs de transport. 
    
Ces méthodes ont des implémentations similaires. Les principales tâches qui effectue une méthode de fermeture de session sont les suivants :
  
- Libérer tous les objets ouverts, y compris les sous-objets et objets d’état.
    
- Appel de méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de la prise en charge pour décrémenter son décompte de références. 
    
- Suppression de toutes les structures [MAPIUID](mapiuid.md) inscrits votre fournisseur. 
    
- Suppression de ligne de votre fournisseur dans la table d’état.
    
- Effectue toutes les tâches qui sont associées au nettoyage de ressources, telles que les suivantes :
    
  - Arrêt d’une connexion avec un serveur distant.
    
  - Nombre de décrémenter la référence sur l’objet d’ouverture de session.
    
  - Suppression de l’objet d’ouverture de session dans la liste d’objets d’ouverture de session qui stocke de votre fournisseur.
    
  - En mode débogage, émettre des traces pour localiser des objets qui ont une fuite de mémoire.
    
Retourne la méthode de fermeture de session MAPI appelle les éléments suivants :
  
- Méthode **IUnknown::Release** de l’objet d’ouverture de session. 
    
- Méthode de **l’arrêt** de l’objet de votre fournisseur pour effectuer les tâches de nettoyage final. Selon le type de votre fournisseur, une des méthodes suivantes est appelée : 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) pour les fournisseurs de carnet d’adresses 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) pour les fournisseurs de banque de messages 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) pour les fournisseurs de transport 
    
- Méthode **IUnknown::Release** de l’objet de votre fournisseur. 
    
Si votre fournisseur est une banque de messages, un appel client [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) lance également le processus d’arrêt. **StoreLogoff** fournisseur de magasins d’un message particulier s’arrête et n’a aucun effet sur la session. Qu’un fournisseur de magasin de message peut être arrêté avec cette méthode ; Il n’existe pas de manière explicite pour arrêter un fournisseur de transport ou du carnet d’adresses particulière. Pour plus d’informations sur la façon de répondre à un **StoreLogoff** appel, voir [Arrêt vers le bas un Message fournisseur de magasins](shutting-down-a-message-store-provider.md).
  
DLL de votre fournisseur sera déchargé MAPI appelle la fonction API Win32 **FreeLibrary**, un appel est effectué après que le dernier client actif a appelé [MAPIUninitialize](mapiuninitialize.md). À ce stade, votre fournisseur de services est arrêtés. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

