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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334474"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel que MAPI appelle pour envoyer une notification d'événement. Cette fonction de rappel ne peut être utilisée que lorsqu'elle est incluse dans un wrapper dans un objet de récepteur de notifications créé en appelant la fonction [HrAllocAdviseSink](hrallocadvisesink.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Fonction définie implémentée par:  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Fonction définie appelée par:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Paramètres

 _lpvContext_
  
> dans Pointeur vers une valeur arbitraire passée à la fonction de rappel lorsque MAPI l'appelle. Cette valeur peut représenter une adresse de signification pour l'application cliente ou le fournisseur de services. En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers un objet c++. 
    
 _cNotification_
  
> dans Nombre de notifications d'événement dans le tableau indiqué par le paramètre _lpNotifications_ . 
    
 _lpNotifications_
  
> remarquer Pointeur vers l'emplacement où cette fonction écrit un tableau de structures de [notification](notification.md) qui contient les notifications d'événement. 
    
## <a name="return-value"></a>Valeur renvoyée

L'ensemble des valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** varie selon que la fonction est implémentée par une application cliente ou un fournisseur de services. Les clients doivent toujours retourner S_OK. Les fournisseurs peuvent retourner S_OK ou CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Remarques

CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrone uniquement; Il demande que l'interface MAPI cesse immédiatement de traiter les rappels pour cette notification. Lorsque CALLBACK_DISCONTINUE est renvoyé, MAPI définit le paramètre _lpUlFlags_ sur NOTIFY_CANCELED lorsqu'il revient de [IMAPISupport:: Notify](imapisupport-notify.md). 
  
Les éléments suivants sont des limitations de ce qu'une fonction de rappel synchrone peut effectuer:
  
- Il ne peut pas provoquer la génération d'une autre notification synchrone.
    
- Il ne peut pas afficher une interface utilisateur.
    
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

