---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ea1238b128eeffe460240b835384a1055c11a287
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575469"
---
# <a name="mapioffline_notify"></a>MAPIOFFLINE_NOTIFY

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il s’agit de la notification d’une modification de l’état de connexion. Il indique la partie de l’état de connexion qui a changé, l’ancien état de connexion et le nouvel état de connexion.
  
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

## <a name="members"></a>Members

 _ulSize_
  
> Taille de la **MAPIOFFLINE_NOTIFY** structure. 
    
 _NotifyType_
  
> Type de notification. Notez que seule la notification de modification de l’état de connexion est prise en charge ; Les seules valeurs prise en charge sont les :
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Jeton défini par le client dans la structure **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** dans **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
    
 _ulMask_
  
> Partie de l’état de connexion qui a changé. La seule valeur prise en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> Ancien état de connexion. Les seules valeurs prise en charge sont :
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> Nouvel état de connexion. Les seules valeurs prise en charge sont :
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Remarques

L’API d’état hors connexion prend uniquement en charge les notifications pour les modifications en ligne/hors connexion. Un client doit vérifier qu’Outlook renvoie les valeurs suivantes avant d’examiner la modification réelle :
  
1.  *NotifyType*  a la valeur MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. Dans ce cas, le client peut supposer que la modification est un changement d’état de connexion et que  *Info*  est de la structure  *StateChange*  . 
    
2.  *ulMask a*  la valeur MAPIOFFLINE_STATE_OFFLINE_MASK. Dans ce cas, le client peut supposer que la modification est un changement d’état de connexion en ligne/hors connexion et peut passer à l’examen de  *ulStateOld*  et  *ulStateNew*  . 
    
Il est possible que Outlook avertisse un client d’autres modifications qui ne sont pas pris en charge. Dans ce cas,  *NotifyType*  ne serait pas l’une des trois valeurs précédemment énoncés, ou  *ulMask*  ne serait pas MAPIOFFLINE_STATE_OFFLINE_MASK, et le client doit ignorer le reste des données dans  *Info*  . 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API d’état hors connexion](about-the-offline-state-api.md)  
- [Constantes MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

