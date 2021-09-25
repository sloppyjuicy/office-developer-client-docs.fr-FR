---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9eca18be8d9b6cc1db17d503edff8f121175f27a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591996"
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
  
> [in] Nombre de notifications d’événement dans le tableau indiqué par le _paramètre lpNotifications._ 
    
 _lpNotifications_
  
> [out] Pointeur vers l’emplacement où cette fonction écrit un tableau de structures [DE NOTIFICATION](notification.md) qui contient les notifications d’événement. 
    
## <a name="return-value"></a>Valeur renvoyée

L’ensemble des valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** varie selon que la fonction est implémentée par une application cliente ou un fournisseur de services. Les clients doivent toujours renvoyer S_OK. Les fournisseurs peuvent renvoyer S_OK ou CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Remarques

CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrones uniquement ; il demande à MAPI d’arrêter immédiatement le traitement des rappels pour cette notification. Lorsque CALLBACK_DISCONTINUE est renvoyé, MAPI définit le paramètre  _lpUlFlags_ sur NOTIFY_CANCELED lorsqu’il revient à partir [d’IMAPISupport::Notify](imapisupport-notify.md). 
  
Les limitations suivantes limitent ce que peut faire une fonction de rappel synchrone :
  
- Il ne peut pas générer une autre notification synchrone.
    
- Il ne peut pas afficher une interface utilisateur.
    
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

