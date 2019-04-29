---
title: Vue d'ensemble de l'arrêt rapide
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Dernière modification : 26 juin 2012'
ms.openlocfilehash: 8c33214b04e7c41eab173196c09f145c20ddf219
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427205"
---
# <a name="fast-shutdown-overview"></a>Vue d'ensemble de l'arrêt rapide

**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'arrêt rapide est un mécanisme permettant à un client MAPI de lancer un arrêt rapide du processus client, d'avertir tous les fournisseurs avec lesquels le client a une session MAPI active pour enregistrer les données et les paramètres avant la sortie du processus client. Cette rubrique décrit le mécanisme de base de l'arrêt rapide. 

À partir de Microsoft Outlook 2010 et y compris Microsoft Outlook 2013, le sous-système MAPI fournit l'interface [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) . Outlook et d'autres clients MAPI peuvent adopter l'arrêt rapide comme mécanisme par défaut pour quitter le processus client. Un paramètre au niveau de l'utilisateur dans le Registre Windows de l'ordinateur client contrôle l'adoption de l'arrêt rapide pour tous les clients MAPI de cet utilisateur sur cet ordinateur. Pour plus d'informations sur les paramètres du Registre, consultez la rubrique options de l' [utilisateur à arrêt rapide](fast-shutdown-user-options.md).
  
Si un client MAPI doit adopter l'arrêt rapide, il doit utiliser l'interface **IMAPIClientShutdown: IUnknown** . Voici le cours classique des événements lorsque le client tente de s'arrêter: 
  
1. Le client MAPI lance l'arrêt en appelant la méthode [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) pour déterminer si le sous-système MAPI prend en charge l'arrêt rapide. 
    
2. Le sous-système MAPI répond avec la prise en charge de l'arrêt rapide disponible à l'appel **IMAPIClientShutdown:: QueryFastShutdown** du client à l'aide de la procédure suivante: 
    
    1. Le sous-système MAPI appelle la méthode [IMAPIProviderShutdown:: QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) pour chaque fournisseur MAPI avec lequel le processus client MAPI a une session MAPI active, si le fournisseur a implémenté l' [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) Lip. 
        
       > [!NOTE]
       >  Le sous-système MAPI interroge et notifie toujours les fournisseurs MAPI via l'interface **IUnknown IMAPIProviderShutdown: IUnknown** au sein de chaque session MAPI, dans l'ordre suivant:
       > 1. Fournisseurs de transport
       > 2. Fournisseurs de carnets d'adresses
       > 3. Fournisseurs de magasin 
    
    2. En fonction du paramètre de registre de l'arrêt rapide de cet utilisateur sur l'ordinateur client, le sous-système MAPI spécifie le code de retour approprié à **IMAPIClientShutdown:: QueryFastShutdown**. Le code renvoyé est S_OK ou MAPI_E_NO_SUPPORT.
        
    3. Le client MAPI appelle la méthode [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) pour indiquer au sous-système MAPI l'intention de s'arrêter. 
        
    4. Le sous-système MAPI indique à chaque fournisseur MAPI chargé de s'arrêter le client MAPI. Pour les fournisseurs qui ont implémenté l'interface **IMAPIProviderShutdown: IUnknown** , le sous-système MAPI appelle la méthode [IMAPIProviderShutdown:: NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondante. 
        
    5. Le client MAPI appelle la méthode [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) pour indiquer au sous-système MAPI que le processus client quitte immédiatement. 
        
    6. Le sous-système MAPI indique à chaque fournisseur MAPI chargé de quitter le processus client MAPI. Pour les fournisseurs qui ont implémenté l'interface **IMAPIProviderShutdown: IUnknown** , le sous-système MAPI appelle la méthode [IMAPIProviderShutdown::D ofastshutdown](imapiprovidershutdown-dofastshutdown.md) correspondante. À ce stade, ces fournisseurs MAPI doivent vérifier que toutes les actions nécessaires, telles que l'enregistrement des données et des paramètres, sont terminées en préparation pour le client MAPI afin de déconnecter immédiatement toutes les références et quitter. 
    
## <a name="see-also"></a>Voir aussi

- [Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
- [Options de l'utilisateur à arrêt rapide](fast-shutdown-user-options.md)
- [Meilleures pratiques en cas d’arrêt rapide](best-practices-for-fast-shutdown.md)

