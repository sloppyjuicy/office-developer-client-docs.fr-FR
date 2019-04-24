---
title: Forçage d'une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328097"
---
# <a name="forcing-a-notification"></a>Forçage d'une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les fournisseurs de services utilisent les méthodes [IMAPISupport: IUnknown](imapisupportiunknown.md) pour la notification, MAPI envoie des notifications à l'aide d'une fenêtre masquée et de la procédure de fenêtre correspondante. Pour chaque processus de réception d'une notification, MAPI publie un message particulier dans la fenêtre masquée. Ce message est nommé à l'aide de la constante **szMAPINotificationMsg** qui est définie dans MAPIDEFS. H. 
  
Ces notifications s'affichent lorsque la procédure de fenêtre masquée traite le message **szMAPINotificationMsg** . Pour garantir la remise des notifications, il est nécessaire d'attendre et de distribuer ce message **szMAPINotificationMsg** . L'implémentation de la logique pour y parvenir peut être réalisée simplement, mais MAPI fournit un point d'entrée dans la DLL MAPI appelée [HrDispatchNotifications](hrdispatchnotifications.md) pour simplifier le traitement. Appelez **HrDispatchNotifications** comme suit pour recevoir des notifications dans votre client: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


