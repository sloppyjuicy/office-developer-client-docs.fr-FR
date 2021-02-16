---
title: Forcer une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433282"
---
# <a name="forcing-a-notification"></a>Forcer une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les fournisseurs de services utilisent les méthodes [IMAPISupport : IUnknown](imapisupportiunknown.md) pour la notification, MAPI fournit des notifications à l’aide d’une fenêtre masquée et de sa procédure de fenêtre correspondante. Pour chaque processus de réception d’une notification, MAPI publie un message spécial dans la fenêtre masquée. Ce message est nommé avec la constante **szMAPINotificationMsg** définie dans MAPIDEFS.H. 
  
Vous recevez ces notifications lorsque la procédure de fenêtre masquée traite le message **szMAPINotificationMsg.** Pour garantir que les notifications sont remis, il est nécessaire d’attendre et de transmettre ce message **szMAPINotificationMsg.** L’exécution de la logique pour y parvenir peut être effectuée assez simplement, mais MAPI fournit un point d’entrée dans la DLL MAPI appelée [HrDispatchNotifications](hrdispatchnotifications.md) pour simplifier encore le traitement. Appelez **HrDispatchNotifications** comme suit pour recevoir des notifications dans votre client : 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


