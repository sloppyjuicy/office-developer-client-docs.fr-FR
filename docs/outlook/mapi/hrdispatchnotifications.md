---
title: HrDispatchNotifications
description: Cet article décrit la fonction HrDispatchNotifications et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
ms.openlocfilehash: 968fd16c3c4438fe62cb11d545df708b18055425
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812768"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Force la distribution de toutes les notifications en file d’attente. 
  
|Propriété |Valeur |
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
  
> Toutes les notifications en file d’attente ont été distribuées.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION a été reçu.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI n’a pas été initialisé.
    
## <a name="remarks"></a>Remarques

La fonction **HrDispatchNotifications** entraîne l’envoi par MAPI de toutes les notifications actuellement mises en file d’attente dans le moteur de notification MAPI sans attendre la répartition des messages. Cela peut avoir un effet bénéfique sur l’utilisation de la mémoire. Pour plus d’informations, consultez [Forcer une notification](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Certaines applications attendent un message de notification dans une boucle de délai d’expiration à l’aide des fonctions Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) et [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx). Sur toutes les plateformes sauf les plus rapides, ces applications peuvent rencontrer des performances médiocres, voire un blocage des notifications. L’utilisation de **HrDispatchNotifications** réduit non seulement le code, mais améliore également les performances. 
  

