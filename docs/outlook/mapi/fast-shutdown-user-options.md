---
title: Options utilisateur en cas d’arrêt rapide
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Dernière modification : 26 juin 2012'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716368"
---
# <a name="fast-shutdown-user-options"></a>Options utilisateur en cas d’arrêt rapide

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit les trois paramètres de Registre Windows disponibles dans Microsoft Outlook 2010 et désormais dans Microsoft Outlook 2013 pour l’arrêt rapide des clients MAPI d’un utilisateur. Les administrateurs peuvent utiliser ces paramètres de Registre pour spécifier le comportement d’arrêt favori du client en fonction de la prise en charge des fournisseurs MAPI de l’arrêt rapide du client. Le paramètre de l’administrateur, à son tour, détermine comment le sous-système MAPI répond à l’appel du client MAPI à l’interface [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en matière de prise en charge de l’arrêt rapide disponible. 
  
Même si un paramètre de Registre reflète la préférence de l’administrateur au niveau utilisateur pour l’arrêt rapide pour tous les clients MAPI, un développeur client MAPI peut décider si le client prend en charge l’arrêt rapide indépendamment d’autres clients MAPI et du paramètre de Registre de l’administrateur. Néanmoins, pour que l’arrêt rapide ait lieu correctement, l’utilisateur doit disposer du paramètre de Registre nécessaire, un client MAPI doit lancer l’arrêt rapide à l’aide de l’interface [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) et les fournisseurs MAPI qui utilisent le client doivent implémenter l’interface [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) pour prendre en charge l’arrêt rapide du client. 
  
La liste suivante décrit les trois options au niveau utilisateur.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Option 1 : le sous-système MAPI active l’arrêt rapide, sauf si les fournisseurs MAPI le désactivent explicitement 
    
À partir d’Outlook 2010, il s’agit du comportement par défaut si Outlook est le client MAPI. Ce n’est pas nécessairement le comportement par défaut pour d’autres clients MAPI. Pour spécifier explicitement cette option pour Outlook, les administrateurs peuvent choisir de définir la valeur et la clé de Registre suivantes.
    
Clé de Registre :
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valeur :
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Lorsqu’un client MAPI lance un arrêt rapide et appelle l’interface **IMAPIClientShutdown::QueryFastShutdown** pour effectuer une requête pour une prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en renvoyant S\_OK tant qu’aucun fournisseur MAPI ayant une session MAPI active avec le client MAPI n’a désactivé explicitement la prise en charge de l’arrêt rapide. 

Un fournisseur MAPI désactive l’arrêt rapide en implémentant la méthode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) pour qu’elle renvoie une erreur (MAPI\_E\_NO\_SUPPORT). Si un ou plusieurs fournisseurs MAPI renvoient une erreur dans **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI renvoie MAPI_\E_\NO\_SUPPORT à **IMAPIClientShutdown::QueryFastShutdown**. 

Sauf si un fournisseur MAPI désactive l’arrêt rapide, le sous-système MAPI renvoie S\_OK, même si un ou plusieurs fournisseurs n’ont pas implémenté l’interface **IMAPIProviderShutdown : IUnknown**. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Option 2 : le sous-système MAPI active l’arrêt rapide uniquement si chaque fournisseur MAPI l’active explicitement 
    
Les administrateurs doivent explicitement définir la valeur et la clé de Registre suivantes pour spécifier cette préférence pour l’arrêt rapide du client.
    
Clé de Registre :
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valeur :
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Lorsqu’un client MAPI lance un arrêt rapide et appelle l’interface **IMAPIClientShutdown::QueryFastShutdown** pour effectuer une requête pour une prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en renvoyant S\_OK si tous les fournisseurs MAPI ayant des sessions actives avec le client MAPI prennent en charge l’arrêt rapide. Un fournisseur MAPI démontre sa prise en charge en implémentant **IMAPIProviderShutdown::QueryFastShutdown** de façon à renvoyer un code de non-erreur (S\_OK). 

Si un ou plusieurs de ces fournisseurs MAPI renvoient MAPI\_E\_NO\_SUPPORT ou n’implémentent pas **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI renvoie un code d’erreur à **IMAPIClientShutdown::QueryFastShutdown**.
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Option 3 : un administrateur désactive la prise en charge de l’arrêt rapide du client
    
Les administrateurs doivent explicitement définir la valeur et la clé de Registre suivantes pour désactiver la prise en charge pour l’arrêt rapide du client.
    
Clé de Registre :
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Valeur :
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Lorsqu’un client MAPI lance un arrêt rapide et appelle l’interface **IMAPIClientShutdown::QueryFastShutdown** pour effectuer une requête pour une prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en renvoyant MAPI_E_NO_SUPPORT, indépendamment du fait qu’un fournisseur MAPI prenne en charge l’arrêt rapide. Sous ce paramètre de Registre, le sous-système MAPI n’appelle jamais la méthode **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de l’un des fournisseurs. 
    
## <a name="see-also"></a>Voir aussi

- [Arrêt du client dans MAPI](client-shutdown-in-mapi.md)
- [Présentation de l’arrêt rapide](fast-shutdown-overview.md)
- [Meilleures pratiques en cas d’arrêt rapide](best-practices-for-fast-shutdown.md)

