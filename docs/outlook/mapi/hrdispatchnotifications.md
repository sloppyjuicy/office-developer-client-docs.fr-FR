---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348096"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Force la distribution de toutes les notifications en file d’attente. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Toutes les notifications en file d’attente ont été envoyées.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION reçu.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI n’a pas été initialisé.
    
## <a name="remarks"></a>Remarques

La **fonction HrDispatchNotifications** fait en sorte que MAPI envoie toutes les notifications actuellement en file d’attente dans le moteur de notification MAPI sans attendre une distribution de message. Cela peut avoir un effet bénéfique sur l’utilisation de la mémoire. Pour plus d’informations, voir [Forcer une notification.](forcing-a-notification.md) 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Certaines applications attendent un message de notification dans une boucle de délai d’attente à l’aide des fonctions Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) et [DispatchMessage.](https://msdn.microsoft.com/library/ms644934.aspx) Sur toutes les plateformes, sauf sur les plateformes les plus rapides, ces applications peuvent faire l’expérience de performances médiocres ou même d’un blocage des notifications. **L’utilisation de HrDispatchNotifications réduit** non seulement le code, mais améliore les performances. 
  

