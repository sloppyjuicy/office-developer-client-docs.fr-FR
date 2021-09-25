---
title: Forcer une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 878a4372b4fe017fce001ddb3322f1d044151134
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621079"
---
# <a name="forcing-a-notification"></a>Forcer une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les fournisseurs de services utilisent les méthodes [IMAPISupport : IUnknown](imapisupportiunknown.md) pour la notification, MAPI fournit des notifications à l’aide d’une fenêtre masquée et de sa procédure de fenêtre correspondante. Pour chaque processus de réception d’une notification, MAPI publie un message spécial dans la fenêtre masquée. Ce message est nommé avec la constante **szMAPINotificationMsg** définie dans MAPIDEFS.H. 
  
Vous recevez ces notifications lorsque la procédure de fenêtre masquée traite le message **szMAPINotificationMsg.** Pour garantir que les notifications sont remis, il est nécessaire d’attendre et de transmettre ce message **szMAPINotificationMsg.** L’exécution de la logique pour y parvenir peut être effectuée assez simplement, mais MAPI fournit un point d’entrée dans la DLL MAPI appelée [HrDispatchNotifications](hrdispatchnotifications.md) pour simplifier encore le traitement. Appelez **HrDispatchNotifications** comme suit pour recevoir des notifications dans votre client : 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


