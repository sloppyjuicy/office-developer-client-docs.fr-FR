---
title: Options d’arrêt rapide utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Dernière modification : 26 juin 2012'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783277"
---
# <a name="fast-shutdown-user-options"></a>Options d’arrêt rapide utilisateur

**S’applique à**: Outlook 
  
Cette rubrique décrit les trois paramètres du Registre Windows qui sont disponibles, démarrage de Microsoft Outlook 2010 et maintenant, y compris Microsoft Outlook 2013, pour l’arrêt rapide des clients MAPI de l’utilisateur. Les administrateurs peuvent utiliser ces paramètres de Registre pour spécifier le comportement de l’arrêt de client par défaut en fonction de la prise en charge des fournisseurs MAPI pour arrêt rapide du client. L’administrateur, à son tour, détermine comment le sous-système MAPI répond aux appels du client MAPI à [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en termes de prise en charge de l’arrêt rapide disponibles. 
  
Même si un paramètre de Registre reflète la préférence de l’administrateur au niveau de l’utilisateur pour l’arrêt rapide pour tous les clients MAPI, un développeur de client MAPI peut décider si le client prend en charge l’arrêt rapide indépendamment des autres clients MAPI et paramètre de Registre de l’administrateur. Néanmoins, pour l’arrêt rapide se déroule correctement, l’utilisateur doit avoir le paramètre de Registre nécessaires, un client MAPI doit initier l’arrêt rapide à l’aide de la [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface et fournisseurs MAPI qui fonctionnent avec le client doit implémenter la [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface pour prendre en charge l’arrêt rapide de client. 
  
La liste suivante décrit les trois options de niveau utilisateur.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Option 1 : Le sous-système MAPI permet d’arrêt rapide, sauf si les fournisseurs MAPI exclure explicitement 
    
À compter d’Outlook 2010, il s’agit du comportement par défaut lorsque Outlook est le client MAPI ; Il n’est pas nécessairement le comportement par défaut pour les autres clients MAPI. Pour spécifier explicitement cette option pour Outlook, les administrateurs peuvent choisir définir la valeur et la clé de Registre suivante.
    
Clé de Registre :
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valeur :
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Lorsqu’un client MAPI initie un arrêt rapide et appelle **IMAPIClientShutdown::QueryFastShutdown** à la requête pour la prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en retournant S\_OK tant qu’aucun fournisseur MAPI qui possède un MAPI active session avec le client MAPI a choisi explicitement en dehors de la prise en charge de l’arrêt rapide. 

Un fournisseur MAPI choisit en dehors de l’arrêt rapide en implémentant la méthode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) renvoie une erreur (MAPI\_E\_non\_prise en charge). Si un ou plusieurs fournisseurs MAPI renvoient une erreur dans **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI renvoie MAPI_\E_\NO\_ **IMAPIClientShutdown::QueryFastShutdown**prise en charge. 

Sauf si un fournisseur MAPI exclut, la renvoie du sous-système MAPI S\_OK, même si un ou plusieurs fournisseurs n’ont pas implémenté la **IMAPIProviderShutdown : IUnknown** interface. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Option 2 : Le sous-système MAPI permet d’arrêt rapide uniquement si tous les fournisseurs MAPI choisit explicitement dans 
    
Les administrateurs doivent définir explicitement la clé de Registre suivante et une valeur pour spécifier cette préférence pour arrêt rapide du client.
    
Clé de Registre :
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valeur :
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Lorsqu’un client MAPI initie un arrêt rapide et appelle **IMAPIClientShutdown::QueryFastShutdown** à la requête pour la prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en retournant S\_OK si tous les fournisseurs MAPI qui ont des sessions actives avec l’arrêt MAPI client prise en charge rapide. Un fournisseur MAPI illustre la prise en charge par l’implémentation **IMAPIProviderShutdown::QueryFastShutdown** pour renvoyer un code d’erreur non (S\_OK). 

Si un ou plusieurs de ces fournisseurs MAPI renvoient MAPI\_E\_non\_prise en charge, ou qui n’implémentent pas **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI retourne un code d’erreur à **IMAPIClientShutdown::QueryFastShutdown** .
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Option 3 : Un administrateur désactive la prise en charge de l’arrêt rapide client
    
Les administrateurs doivent définir explicitement la clé de Registre suivante et une valeur pour désactiver la prise en charge de l’arrêt rapide du client.
    
Clé de Registre :
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valeur :
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Lorsqu’un client MAPI initie un arrêt rapide et appelle **IMAPIClientShutdown::QueryFastShutdown** à la requête pour la prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en retournant MAPI_E_NO_SUPPORT, quel que soit si tout fournisseur MAPI prend en charge rapide de l’arrêt. Sous ce paramètre de Registre, le sous-système MAPI appelle jamais la méthode **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) d’un des fournisseurs. 
    
## <a name="see-also"></a>Voir aussi

- [Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
- [Vue d’ensemble de l’arrêt rapide](fast-shutdown-overview.md)
- [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md)

