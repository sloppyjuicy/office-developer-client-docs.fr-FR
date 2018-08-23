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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 17b038fea2dd1614f94f005e32b9e6ba4423dbda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566263"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel appels MAPI pour envoyer une notification d’événement. Cette fonction de rappel peut être utilisée uniquement lorsqu’encapsulé dans un objet de récepteur advise créé en appelant la fonction [HrAllocAdviseSink](hrallocadvisesink.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction implémentée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
|Fonction appelée par :  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Paramètres

 _lpvContext_
  
> [in] Pointeur vers une valeur arbitraire transmis à la fonction de rappel lorsque MAPI il l’appelle. Cette valeur peut représenter une adresse de l’argument précision pour l’application cliente ou d’un fournisseur de services. En règle générale, pour le code C++, le paramètre _lpvContext_ représente un pointeur vers un objet C++. 
    
 _cNotification_
  
> [in] Nombre de notifications d’événements dans le tableau indiqué par le paramètre _lpNotifications_ . 
    
 _lpNotifications_
  
> [out] Pointeur vers l’emplacement où cette fonction écrit un tableau de structures [NOTIFICATION](notification.md) qui contient les notifications d’événements. 
    
## <a name="return-value"></a>Valeur renvoy�e

L’ensemble de valeurs de retour valides pour le prototype de fonction **NOTIFCALLBACK** dépend si la fonction est implémentée par une application cliente ou d’un fournisseur de services. Les clients doivent toujours retourner S_OK. Fournisseurs peuvent renvoyer S_OK ou CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Remarques

CALLBACK_DISCONTINUE est une valeur de retour valide pour les fonctions de rappel synchrone uniquement ; il demande que MAPI arrêter immédiatement traitement des rappels pour cette notification. Lorsque CALLBACK_DISCONTINUE est renvoyée, MAPI attribue au paramètre _lpUlFlags_ NOTIFY_CANCELED lorsqu’il retourne de [IMAPISupport::Notify](imapisupport-notify.md). 
  
Limitations sur ce que peut faire une fonction de rappel synchrone sont les suivantes :
  
- Il ne peut pas provoquer la génération d’une autre notification synchrone.
    
- Il ne peut pas afficher une interface utilisateur.
    
## <a name="see-also"></a>Voir aussi



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

