---
title: MAPIOFFLINE_NOTIFY
manager: lindalu
ms.date: 02/22/2022
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
ms.openlocfilehash: a08c2a12d645878968c3042c67f5132321e71d0b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382012"
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
  
1. _NotifyType_ a la valeur MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. Dans ce cas, le client peut supposer que la modification est un changement d’état de connexion et que _Info_ est de la structure _StateChange_.

2. _ulMask a_ la valeur MAPIOFFLINE_STATE_OFFLINE_MASK. Dans ce cas, le client peut supposer que la modification est un changement d’état de connexion en ligne/hors connexion et peut passer à l’examen de _ulStateOld_ et _ulStateNew_.

Il est possible que Outlook avertisse un client d’autres modifications qui ne sont pas pris en charge. Dans ce cas, _NotifyType_ ne serait pas l’une des trois valeurs précédemment énoncés, ou _ulMask_ ne serait pas MAPIOFFLINE_STATE_OFFLINE_MASK et le client doit ignorer le reste des données dans _Info_.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API d’état hors connexion](about-the-offline-state-api.md)  
- [Constantes MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)
