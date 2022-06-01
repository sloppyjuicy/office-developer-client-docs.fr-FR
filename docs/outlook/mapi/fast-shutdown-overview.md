---
title: Vue d’ensemble de l’arrêt rapide
description: L’arrêt rapide est un mécanisme permettant à un client MAPI de lancer un arrêt rapide du processus client, en informant tous les fournisseurs d’enregistrer les données et les paramètres.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
ms.openlocfilehash: 3e7f06338dd27c5aed2026d52998e0f96ebecf95
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816478"
---
# <a name="fast-shutdown-overview"></a>Vue d’ensemble de l’arrêt rapide

**S’applique à** : Outlook 2013 | Outlook 2016
  
L’arrêt rapide est un mécanisme permettant à un client MAPI de lancer un arrêt rapide du processus client, en informant tous les fournisseurs avec lesquels le client dispose d’une session MAPI active pour enregistrer les données et les paramètres avant la fin du processus client. Cette rubrique décrit le mécanisme de base de l’arrêt rapide.

À compter de Microsoft Outlook 2010 et maintenant de Microsoft Outlook 2013, le sous-système MAPI fournit l’interface [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md). Outlook et d’autres clients MAPI peuvent adopter l’arrêt rapide comme mécanisme par défaut pour quitter le processus client. Un paramètre de niveau utilisateur dans le registre Windows de l’ordinateur client contrôle l’adoption de l’arrêt rapide pour tous les clients MAPI pour cet utilisateur sur cet ordinateur. Pour plus d’informations sur les paramètres du Registre, consultez [Options utilisateur d’arrêt rapide](fast-shutdown-user-options.md).
  
Si un client MAPI doit adopter un arrêt rapide, il doit utiliser l’interface **IMAPIClientShutdown : IUnknown** . Voici le cours classique des événements lorsque le client tente de s’arrêter :
  
1. Le client MAPI lance l’arrêt en appelant la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) pour déterminer si le sous-système MAPI prend en charge l’arrêt rapide.

2. Le sous-système MAPI répond avec la prise en charge de l’arrêt rapide disponible à l’appel **IMAPIClientShutdown::QueryFastShutdown du** client à l’aide de la procédure suivante :

    1. Le sous-système MAPI appelle la méthode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) pour chaque fournisseur MAPI avec lequel le processus client MAPI a une session MAPI active, si le fournisseur a implémenté l’interface [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) .

       > [!NOTE]
       > Le sous-système MAPI interroge toujours et avertit les fournisseurs MAPI par le biais de l’interface **IMAPIProviderShutdown : IUnknown** dans chaque session MAPI dans l’ordre suivant :
       >
       > 1. Fournisseurs de transport
       > 2. Fournisseurs de carnets d’adresses
       > 3. Fournisseurs du Store

    2. Selon le paramètre de Registre d’arrêt rapide pour cet utilisateur sur l’ordinateur client, le sous-système MAPI spécifie le code de retour approprié à **IMAPIClientShutdown::QueryFastShutdown**. Le code de retour est S_OK ou MAPI_E_NO_SUPPORT.

    3. Le client MAPI appelle la méthode [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) pour indiquer au sous-système MAPI l’intention de s’arrêter.

    4. Le sous-système MAPI indique à chaque fournisseur MAPI chargé que le client MAPI s’arrêtera. Pour les fournisseurs qui ont implémenté l’interface **IMAPIProviderShutdown : IUnknown** , le sous-système MAPI appelle la méthode [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondante.

    5. Le client MAPI appelle la méthode [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) pour indiquer au sous-système MAPI que le processus client se termine immédiatement.

    6. Le sous-système MAPI indique à chaque fournisseur MAPI chargé que le processus client MAPI se termine. Pour les fournisseurs qui ont implémenté l’interface **IMAPIProviderShutdown : IUnknown** , le sous-système MAPI appelle la méthode [IMAPIProviderShutdown::D oFastShutdown](imapiprovidershutdown-dofastshutdown.md) correspondante. À ce stade, ces fournisseurs MAPI doivent vérifier que toutes les actions nécessaires, telles que l’enregistrement des données et des paramètres, sont terminées en préparation pour que le client MAPI déconnecte immédiatement toutes les références et quitte.

## <a name="see-also"></a>Voir aussi

- [Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
- [Options utilisateur d’arrêt rapide](fast-shutdown-user-options.md)
- [Meilleures pratiques en cas d’arrêt rapide](best-practices-for-fast-shutdown.md)
