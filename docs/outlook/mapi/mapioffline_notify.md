---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784762"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**S’applique à**: Outlook 
  
Il s’agit de la notification d’une modification dans l’état de connexion. Elle indique la partie de l’état de connexion qui a été modifié, l’état de connexion ancien et le nouvel état de connexion.
  
## <a name="quick-info"></a>Informations rapides

Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a>Membres

 _ulSize_
  
> Taille de la structure **MAPIOFFLINE_NOTIFY** . 
    
 _NotifyType_
  
> Type de notification. Notez que seule notification des modifications de l’état de connexion est pris en charge ; les seules valeurs prises en charge sont :
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Jeton défini par le client dans la structure **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** dans **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
    
 _ulMask_
  
> La partie de l’état de connexion qui a été modifiée. La seule valeur pris en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> L’état de connexion ancien. Les seules valeurs prises en charge sont :
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> Le nouvel état de connexion. Les seules valeurs prises en charge sont :
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Remarques

L’API d’état en mode hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion. Un client doit vérifier que Outlook renvoie les valeurs suivantes avant d’examiner la modification :
  
1.  *NotifyType* a la valeur MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. Dans ce cas, le client peut partent du principe que la modification est un changement d’état de connexion et *Info* est de la structure *StateChange* . 
    
2.  *ulMask* a la valeur MAPIOFFLINE_STATE_OFFLINE_MASK. Dans ce cas, le client peut partent du principe que la modification est un changement d’état en ligne/hors connexion et peut poursuivre examen *ulStateOld* et *ulStateNew* . 
    
Il est possible qu’Outlook indique d’autres modifications ne sont pas pris en charge un client. Dans ce cas, *NotifyType* ne serait pas l’une des trois valeurs mentionné plus haut, ou *ulMask* ne serait pas MAPIOFFLINE_STATE_OFFLINE_MASK, et le client doit ignorer le reste des données dans les *Info* . 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API d’état en mode hors connexion](about-the-offline-state-api.md)  
- [Constantes MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

