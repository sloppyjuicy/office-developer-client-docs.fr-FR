---
title: Meilleures pratiques pour l'arrêt rapide
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
# <a name="best-practices-for-fast-shutdown"></a>Meilleures pratiques pour l'arrêt rapide

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique recommande les meilleures pratiques pour les administrateurs, les clients MAPI et les fournisseurs MAPI afin d'utiliser les paramètres du Registre Windows et les interfaces d'arrêt rapide pour réduire la perte de données lors de l'arrêt du client.
  
- Pour qu'un client MAPI effectue une arrêt rapide afin que les processus du fournisseur n'engendrent pas de perte de données, le client MAPI doit d'abord appeler la méthode [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Le client doit ensuite procéder aux [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) méthodes basées sur la prise en charge du sous-système MAPI pour l'arrêt rapide, comme indiqué par la valeur de retour de ** IMAPIClientShutdown:: QueryFastShutdown**. En tant que client MAPI, Microsoft Outlook n'appelle pas **IMAPIClientShutdown:: NotifyProcessShutdown** ou **IMAPIClientShutdown::D ofastshutdown** si **IMAPIClientShutdown:: QueryFastShutdown** renvoie une erreur. Si l'administrateur a désactivé l'arrêt rapide dans le Registre Windows, le sous-système MAPI renvoie MAPI_E_NO_SUPPORT à **IMAPIClientShutdown:: QueryFastShutdown**. Dans ce cas, le sous-système MAPI n'informe pas les fournisseurs MAPI d'une sortie de processus client immédiate. Par conséquent, si un client MAPI ignore ce code d'erreur, procède à l'arrêt rapide et déconnecte toutes les références externes, tous les fournisseurs MAPI chargés auront une perte de données. 
    
- Les fournisseurs MAPI doivent implémenter l'interface [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) pour effectuer les étapes opportunes et nécessaires pour éviter la perte de données, car le client déconnecte les références externes avant la fermeture du client. Un fournisseur doit reporter tous les autres éléments non essentiels pour enregistrer des données dans son magasin de données principal. Par exemple, un fournisseur de transport doit retarder les opérations d'arrière-plan inutiles qui vérifient les nouveaux messages, un fournisseur de carnets d'adresses doit différer le téléchargement des modifications récentes à partir de son serveur, et un fournisseur de banque doit reporter des tâches de maintenance telles que compactage ou indexation. 
    
- Les utilisateurs qui souhaitent que les clients MAPI se ferment dès qu'ils les ferment doivent utiliser le paramètre de Registre par défaut qui active l'arrêt rapide à moins qu'un fournisseur ne le ferme.
    
- Une fois qu'un client MAPI appelle **IMAPIClientShutdown::D ofastshutdown**, il ne doit pas effectuer d'appels supplémentaires à MAPI, y compris la fonction [MAPIUninitialize](mapiuninitialize.md) . Le client ne doit pas utiliser MAPI pour le reste de la durée de vie du processus client. 
    
- Un client MAPI ne doit jamais appeler directement l'interface **IMAPIProviderShutdown** d'un fournisseur. Les clients MAPI doivent toujours utiliser l'interface [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) . 
    
- Si un fournisseur MAPI doit s'assurer que l'arrêt rapide n'est pas utilisé pendant son chargement, il doit implémenter l'interface **IMAPIProviderShutdown** et renvoyer MAPI_E_NO_SUPPORT pour la méthode **IMAPIProviderShutdown:: QueryFastShutdown** . Toutefois, pour les clients MAPI tels qu'Outlook, cela entraînera l'arrêt rapide du client et mettre un moment à s'arrêter. 
    
## <a name="see-also"></a>Voir aussi



[Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
  
[Présentation de l’arrêt rapide](fast-shutdown-overview.md)
  
[Options de l'utilisateur à arrêt rapide](fast-shutdown-user-options.md)

