---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434017"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel que MAPI appelle pour envoyer une notification d’événement. Cette fonction de rappel peut uniquement être utilisée lorsqu’elle est wrapped dans un objet de sink de conseil créé en appelant la fonction [HrAllocAdviseSink.](hrallocadvisesink.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction définie implémentée par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Fonction définie appelée par :  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Paramètres

 _lpvContext_
  
> [in] Pointeur vers une valeur arbitraire transmise à la fonction de rappel lorsque MAPI l’appelle. Cette valeur peut représenter une adresse significative pour l’application cliente ou le fournisseur de services. En règle générale, pour le code C++,  _le paramètre lpvContext_ représente un pointeur vers un objet C++. 
    
 _cNotification_
  
> [in] Nombre de notifications d’événement dans le tableau indiqué par _le paramètre lpNotifications._ 
    
 _lpNotifications_
  
> [out] Pointeur vers l’emplacement où cette fonction écrit un tableau de structures [DE NOTIFICATION](notification.md) qui contient les notifications d’événement. 
    
## <a name="return-value"></a>Valeur renvoyée

L’ensemble des valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** varie selon que la fonction est implémentée par une application cliente ou un fournisseur de services. Les clients doivent toujours renvoyer S_OK. Les fournisseurs peuvent renvoyer S_OK ou CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Remarques

CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrones uniquement ; Il demande à MAPI d’arrêter immédiatement le traitement des rappels pour cette notification. Lorsque CALLBACK_DISCONTINUE est renvoyé, MAPI définit le paramètre  _lpUlFlags_ sur NOTIFY_CANCELED lorsqu’il revient à partir [d’IMAPISupport::Notify](imapisupport-notify.md). 
  
Les limitations suivantes limitent ce que peut faire une fonction de rappel synchrone :
  
- Il ne peut pas générer une autre notification synchrone.
    
- Il ne peut pas afficher une interface utilisateur.
    
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

