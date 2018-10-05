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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385563"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Répartition des forces de toutes les notifications en file d’attente. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Toutes les notifications en file d’attente ont été acheminées.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION a été reçue.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI n’a pas été initialisé.
    
## <a name="remarks"></a>Remarques

La fonction **HrDispatchNotifications** entraîne MAPI distribuer toutes les notifications sont actuellement en file d’attente dans le moteur de notification MAPI sans attendre une intervention du message. Cela peut avoir un effet bénéfique sur l’utilisation de la mémoire. Pour plus d’informations, voir [forcer une Notification](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Certaines applications attendent un message de notification dans une boucle de délai d’expiration en utilisant les fonctions [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) . Sur tous les, mais les plateformes plus rapides, ces applications peuvent rencontrer des performances médiocres ou même blocage de notifications. À l’aide de **HrDispatchNotifications** non seulement réduit code mais améliore les performances. 
  

