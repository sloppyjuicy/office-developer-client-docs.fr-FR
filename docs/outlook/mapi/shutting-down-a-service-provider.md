---
title: Arrêt d'un fournisseur de services
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
# <a name="shutting-down-a-service-provider"></a>Arrêt d'un fournisseur de services

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'un client appelle la méthode [IMAPISession:: Logoff](imapisession-logoff.md) pour mettre fin à la session et arrêter tous les fournisseurs de services actifs, MAPI à son tour appelle les méthodes suivantes: 
  
- [IABLogon:: Logoff](iablogon-logoff.md) pour les fournisseurs de carnet d'adresses. 
    
- [IMSLogon:: Logoff](imslogon-logoff.md) pour les fournisseurs de banque de messages. 
    
- [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) pour les fournisseurs de transport. 
    
Ces méthodes ont des implémentations similaires. Les principales tâches qu'une méthode de fermeture de session effectue sont les suivantes:
  
- La publication de tous les objets ouverts, y compris les objets de sous-objets et d'État.
    
- Appel de la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l'objet de prise en charge pour décrémenter son décompte de références. 
    
- Suppression de toutes les structures [MAPIUID](mapiuid.md) enregistrées du fournisseur. 
    
- Suppression de la ligne de votre fournisseur dans le tableau d'État.
    
- Effectuer toutes les tâches liées au nettoyage des ressources, telles que les suivantes:
    
  - Arrêt d'une connexion à un serveur distant.
    
  - Décrémentation du décompte de références sur l'objet d'ouverture de session.
    
  - Suppression de l'objet Logon de la liste des objets d'ouverture de session que votre fournisseur stocke.
    
  - En mode de débogage, l'émission de traces pour localiser des objets ayant divulgué de la mémoire.
    
Lorsque votre méthode de fermeture de session est renvoyée, MAPI appelle les éléments suivants:
  
- La méthode **IUnknown:: Release** de votre objet d'ouverture de session. 
    
- La méthode d' **arrêt** de votre objet fournisseur pour effectuer les tâches de nettoyage finales. Selon le type de votre fournisseur, l'une des méthodes suivantes est appelée: 
    
  - [IABProvider:: Shutdown](iabprovider-shutdown.md) pour les fournisseurs de carnets d'adresses 
    
  - [IMSProvider:: Shutdown](imsprovider-shutdown.md) pour les fournisseurs de banque de messages 
    
  - [IXPProvider:: arrêt](ixpprovider-shutdown.md) pour les fournisseurs de transport 
    
- La méthode **IUnknown:: Release** de votre objet fournisseur. 
    
Si votre fournisseur est une banque de messages, un appel client à [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) lancera également le processus d'arrêt. **StoreLogoff** ferme un fournisseur de banque de messages particulier et n'a aucun effet sur la session. Seul un fournisseur de banque de messages peut être arrêté avec cette méthode; Il n'existe pas de méthode explicite pour arrêter un carnet d'adresses ou un fournisseur de transport particulier. Pour plus d'informations sur la façon de répondre à un appel **StoreLogoff** , consultez la rubrique [arrêt d'un fournisseur de banque de messages](shutting-down-a-message-store-provider.md).
  
La DLL de votre fournisseur est déchargée lorsque MAPI appelle la fonction de l'API Win32 **FreeLibrary**, un appel passé après le dernier client actif a appelé [MAPIUninitialize](mapiuninitialize.md). À ce stade, votre fournisseur de services aura terminé l'arrêt. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

