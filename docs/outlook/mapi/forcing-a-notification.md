---
title: Forçage d’une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578772"
---
# <a name="forcing-a-notification"></a>Forçage d’une notification

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque fournisseurs de services utilisent la [IMAPISupport : IUnknown](imapisupportiunknown.md) méthodes de notification, MAPI fournit des notifications à l’aide d’une fenêtre masquée et sa procédure de fenêtre correspondante. Pour chaque processus recevoir une notification, MAPI publie un message spécial dans la fenêtre masquée. Ce message est nommé avec la constante **szMAPINotificationMsg** est défini dans MAPIDEFS. H. 
  
Vous recevez ces notifications lors de la procédure de fenêtre de la fenêtre masquée traite le message **szMAPINotificationMsg** . Pour garantir que les notifications sont envoyées, il est nécessaire pour attendre et distribuer ce message **szMAPINotificationMsg** . L’implémentation de la logique pour effectuer cette opération peut être effectuée assez simple, mais MAPI fournit un point d’entrée dans la DLL MAPI appelé [HrDispatchNotifications](hrdispatchnotifications.md) pour rendre le traitement encore plus simple. Appel **HrDispatchNotifications** comme suit pour recevoir des notifications dans votre client : 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


