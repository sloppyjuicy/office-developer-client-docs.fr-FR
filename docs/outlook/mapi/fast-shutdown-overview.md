---
title: Vue d’ensemble de l’arrêt rapide
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Dernière modification : 26 juin 2012'
ms.openlocfilehash: 17b1307427af2c35fe9ba8ee40dc78958e6b4a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783274"
---
# <a name="fast-shutdown-overview"></a>Vue d’ensemble de l’arrêt rapide

**S’applique à**: Outlook 
  
Arrêt rapide est un mécanisme d’un client MAPI d’initier un arrêt rapide du processus de client, en informer tous les fournisseurs dont le client dispose d’une session MAPI active pour enregistrer les données et les paramètres avant la fermeture du processus client. Cette rubrique décrit le mécanisme de base d’arrêt rapide. 

Démarrage de Microsoft Outlook 2010 et maintenant, y compris Microsoft Outlook 2013, le sous-système MAPI fournit la [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface. Outlook et autres clients MAPI peuvent prendre arrêt rapide le mécanisme par défaut pour quitter le processus de client. Un paramètre de niveau utilisateur dans le Registre Windows de l’ordinateur client contrôle l’adoption d’arrêt rapide pour tous les clients MAPI pour cet utilisateur sur cet ordinateur. Pour plus d’informations sur les paramètres de Registre, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md).
  
Si un client MAPI doit adopter arrêt rapide, elle doit utiliser le **IMAPIClientShutdown : IUnknown** interface. Vous trouverez ci-dessous le cours standard d’événements lorsque le client essaie d’arrêter : 
  
1. Le client MAPI initie l’arrêt en appelant la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) pour déterminer si le sous-système MAPI prend en charge l’arrêt rapide. 
    
2. Le sous-système MAPI répond avec la prise en charge de l’arrêt rapide disponible à l’appel du client **IMAPIClientShutdown::QueryFastShutdown** à l’aide de la procédure suivante : 
    
    1. Le sous-système MAPI appelle la méthode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) pour chaque fournisseur MAPI dont le processus de client MAPI dispose d’une session MAPI active, si le fournisseur a mis en œuvre la [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface. 
        
       > [!NOTE]
       >  Le sous-système MAPI toujours interroge et avertit les fournisseurs MAPI par le biais de la **IMAPIProviderShutdown : IUnknown** interface au sein de chaque session MAPI dans l’ordre suivant :
       > 1. Fournisseurs de transport
       > 2. Fournisseurs de carnet d’adresses
       > 3. Fournisseurs de magasins 
    
    2. Selon le paramètre de Registre d’arrêt rapide pour cet utilisateur sur l’ordinateur client, le sous-système MAPI Spécifie que le code de retour à **IMAPIClientShutdown::QueryFastShutdown**. Le code de retour est S_OK ou MAPI_E_NO_SUPPORT.
        
    3. Le client MAPI appelle la méthode [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) pour indiquer le sous-système MAPI l’intention d’arrêter le. 
        
    4. Le sous-système MAPI indique à chaque fournisseur MAPI chargé permettant d’arrête le client MAPI. Pour les fournisseurs qui ont mis en œuvre la **IMAPIProviderShutdown : IUnknown** interface, le sous-système MAPI appelle la méthode [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondante. 
        
    5. Le client MAPI appelle la méthode [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) pour indiquer le sous-système MAPI que le processus client va s’arrêter immédiatement. 
        
    6. Le sous-système MAPI indique à chaque fournisseur MAPI chargé que le processus de client MAPI est en cours de fermeture. Pour les fournisseurs qui ont mis en œuvre la **IMAPIProviderShutdown : IUnknown** interface, le sous-système MAPI appelle la méthode [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) correspondante. À ce stade, ces fournisseurs MAPI doivent vérifier que toutes les actions nécessaires, telles que l’enregistrement de données et les paramètres, sont terminées dans la préparation pour le client MAPI pour se déconnecter de toutes les références et quitter immédiatement. 
    
## <a name="see-also"></a>Voir aussi

- [Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
- [Options d’arrêt rapide utilisateur](fast-shutdown-user-options.md)
- [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md)

