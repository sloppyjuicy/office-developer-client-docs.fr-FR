---
title: NOTIFCALLBACK
description: NOTIFCALLBACK définit une fonction de rappel que MAPI appelle pour envoyer une notification d’événement. Il ne peut être utilisé qu’encapsulé dans un objet récepteur de conseils.
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
ms.openlocfilehash: 4b69f1dce7b7d0e0e8dfb2c21664d785125d4b80
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852417"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel que MAPI appelle pour envoyer une notification d’événement. Cette fonction de rappel peut uniquement être utilisée lorsqu’elle est encapsulée dans un objet récepteur de conseils créé en appelant la fonction [HrAllocAdviseSink](hrallocadvisesink.md) . 
  
|Propriété |Valeur |
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
  
> [in] Pointeur vers une valeur arbitraire transmise à la fonction de rappel lorsque MAPI l’appelle. Cette valeur peut représenter une adresse d’importance pour l’application cliente ou le fournisseur de services. En règle générale, pour le code C++, le paramètre  _lpvContext_ représente un pointeur vers un objet C++. 
    
 _cNotification_
  
> [in] Nombre de notifications d’événements dans le tableau indiqué par le paramètre  _lpNotifications_ . 
    
 _lpNotifications_
  
> [out] Pointeur vers l’emplacement où cette fonction écrit un tableau de structures [NOTIFICATION](notification.md) qui contient les notifications d’événements. 
    
## <a name="return-value"></a>Valeur renvoyée

L’ensemble de valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** dépend de l’implémentation de la fonction par une application cliente ou un fournisseur de services. Les clients doivent toujours retourner S_OK. Les fournisseurs peuvent retourner S_OK ou CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Remarques

CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrones uniquement ; il demande à MAPI d’arrêter immédiatement le traitement des rappels pour cette notification. Lorsque CALLBACK_DISCONTINUE est retourné, MAPI définit le paramètre  _lpUlFlags_ sur NOTIFY_CANCELED lorsqu’il revient [d’IMAPISupport::Notify](imapisupport-notify.md). 
  
Voici les limitations relatives à ce qu’une fonction de rappel synchrone peut faire :
  
- Il ne peut pas générer une autre notification synchrone.
    
- Il ne peut pas afficher d’interface utilisateur.
    
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

