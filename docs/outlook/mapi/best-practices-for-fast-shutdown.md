---
title: Meilleures pratiques pour l’arrêt rapide
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c92347ab1a786196e7f0d99b286e8f4134ce7c24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590700"
---
# <a name="best-practices-for-fast-shutdown"></a>Meilleures pratiques pour l’arrêt rapide

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique recommande les meilleures pratiques pour les administrateurs, les clients MAPI et fournisseurs MAPI à utiliser les paramètres du Registre Windows et les interfaces d’arrêt rapide afin de réduire la perte de données lors de l’arrêt du client.
  
- Pour qu’un client MAPI effectuer correctement arrêt rapide afin que le processus de fournisseur n’entraînent pas la perte de données, le client MAPI devez d’abord appeler la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Le client doit alors avec les méthodes [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) en fonction de la prise en charge du sous-système MAPI pour l’arrêt rapide, comme indiqué par la valeur de retour de ** IMAPIClientShutdown::QueryFastShutdown**. Comme un client MAPI, Microsoft Outlook n’appelle pas **IMAPIClientShutdown::NotifyProcessShutdown** ou **IMAPIClientShutdown::DoFastShutdown** si **IMAPIClientShutdown::QueryFastShutdown** renvoie une erreur. Si l’administrateur a désactivé arrêt rapide dans le Registre Windows, le sous-système MAPI renvoie MAPI_E_NO_SUPPORT à **IMAPIClientShutdown::QueryFastShutdown**. Dans ce cas, le sous-système MAPI informera pas quitter fournisseurs MAPI d’un processus d’exécution client. Par conséquent, si un client MAPI ne tient pas compte de ce code d’erreur, procède à l’arrêt rapide d’et déconnecte tous les références externes, tous les fournisseurs MAPI chargés aura une perte de données. 
    
- Fournisseurs MAPI doivent implémenter la [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface d’effectuer en temps voulu et les mesures nécessaires pour éviter toute perte de données en raison de la déconnexion des références externes avant de quitte le client du client. Un fournisseur doit différer tout est non essentiels pour l’enregistrement de données à la base de données principale. Par exemple, un fournisseur de transport doit différer des opérations en arrière-plan inutiles vérifier de nouveau courrier, qu'un fournisseur de carnet d’adresses doit reporter le téléchargement des modifications récentes apportées à partir de son serveur et un fournisseur de magasins doit différer tels que des tâches de maintenance le compactage ou l’indexation. 
    
- Les utilisateurs qui souhaitent des clients MAPI pour quitter dès qu’ils ferment doivent utiliser le paramètre de Registre par défaut qui permet à l’arrêt rapide, sauf si un fournisseur exclut.
    
- Une fois qu’un client MAPI appelle **IMAPIClientShutdown::DoFastShutdown**, il ne doit pas faire des appels MAPI, y compris la fonction [MAPIUninitialize](mapiuninitialize.md) supplémentaires. Le client ne doit pas utiliser MAPI pour le reste de la durée de vie du processus client. 
    
- Un client MAPI doit appeler jamais directement l’interface de **IMAPIProviderShutdown** d’un fournisseur. Clients MAPI doivent toujours utiliser le [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface. 
    
- Si un fournisseur MAPI doit s’assurer qu’un arrêt rapide n’est pas utilisé pendant son chargement, il doit implémenter l’interface **IMAPIProviderShutdown** et MAPI_E_NO_SUPPORT de la méthode **IMAPIProviderShutdown::QueryFastShutdown** . Toutefois, pour les clients MAPI comme Outlook, cela entraînera le client à abandonner arrêt rapide et prendre plus de temps à arrêter. 
    
## <a name="see-also"></a>Voir aussi



[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
  
[Vue d’ensemble de l’arrêt rapide](fast-shutdown-overview.md)
  
[Options utilisateur d’arrêt rapide](fast-shutdown-user-options.md)

