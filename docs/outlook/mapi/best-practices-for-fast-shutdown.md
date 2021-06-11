---
title: Meilleures pratiques en matière d’arrêt rapide
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8c7225427b80d89c6dd8adfa85f7d91885850365
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426967"
---
# <a name="best-practices-for-fast-shutdown"></a>Meilleures pratiques en matière d’arrêt rapide

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique recommande aux administrateurs, clients MAPI et fournisseurs MAPI d’utiliser les paramètres de Registre Windows et les interfaces d’arrêt rapide pour minimiser la perte de données pendant l’arrêt du client.
  
- Pour qu’un client MAPI effectue un arrêt rapide afin que les processus fournisseurs n’encourent pas de perte de données, le client MAPI doit d’abord appeler la méthode [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Le client doit ensuite poursuivre avec les méthodes [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) en fonction de la prise en charge de l’arrêt rapide du sous-système MAPI, comme indiqué par la valeur de retour de **IMAPIClientShutdown::QueryFastShutdown**. En tant que client MAPI, Microsoft Outlook n’appelle pas **IMAPIClientShutdown::NotifyProcessShutdown** ou **IMAPIClientShutdown::D oFastShutdown** si **IMAPIClientShutdown::QueryFastShutdown** renvoie une erreur. Si l’administrateur a désactivé l’arrêt rapide dans le Registre Windows, le sous-système MAPI retourne MAPI_E_NO_SUPPORT à **IMAPIClientShutdown::QueryFastShutdown**. Dans ce cas, le sous-système MAPI n’informe pas les fournisseurs MAPI d’une sortie immédiate du processus client. Par conséquent, si un client MAPI ignore ce code de retour d’erreur, procède à un arrêt rapide et déconnecte toutes les références externes, tous les fournisseurs MAPI chargés auront une perte de données. 
    
- Les fournisseurs MAPI doivent implémenter l’interface [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) pour effectuer les étapes nécessaires et en temps voulu afin d’éviter la perte de données en raison de la déconnexion des références externes par le client avant la sortie du client. Un fournisseur doit différer tout autre chose qui n’est pas essentiel à l’enregistrement des données dans son magasin de données principal. Par exemple, un fournisseur de transport doit reporter les opérations en arrière-plan inutiles qui recherchent de nouveaux messages, un fournisseur de carnet d’adresses doit différer le téléchargement des modifications récentes à partir de son serveur et un fournisseur de magasin doit reporter les tâches de maintenance telles que le compactage ou l’indexation. 
    
- Les utilisateurs qui souhaitent que les clients MAPI se ferment dès qu’ils les ferment doivent utiliser le paramètre de Registre par défaut qui active l’arrêt rapide, sauf si un fournisseur le désintique.
    
- Une fois qu’un client MAPI appelle **IMAPIClientShutdown::D oFastShutdown,** il ne doit pas effectuer d’appels supplémentaires à MAPI, y compris la fonction [MAPIUninitialize.](mapiuninitialize.md) Le client ne doit pas utiliser MAPI pour le reste de la durée de vie du processus client. 
    
- Un client MAPI ne doit jamais appeler directement l’interface **IMAPIProviderShutdown d’un** fournisseur. Les clients MAPI doivent toujours utiliser l’interface [IMAPIClientShutdown : IUnknown.](imapiclientshutdowniunknown.md) 
    
- Si un fournisseur MAPI doit s’assurer que l’arrêt rapide n’est pas utilisé pendant son chargement, il doit implémenter l’interface **IMAPIProviderShutdown** et renvoyer MAPI_E_NO_SUPPORT pour la méthode **IMAPIProviderShutdown::QueryFastShutdown.** Toutefois, pour les clients MAPI tels que Outlook, le client abandonnera l’arrêt rapide et prendra plus de temps à s’arrêter. 
    
## <a name="see-also"></a>Voir aussi



[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
  
[Présentation de l’arrêt rapide](fast-shutdown-overview.md)
  
[Options utilisateur d’arrêt rapide](fast-shutdown-user-options.md)

