---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 14d5d904a9d9e334956e214b272daace7a82a940
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773193"
---
# <a name="mapisib"></a>MAPISIB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette structure est utilisée [avec IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a>Members

 **ulSize**
  
> Taille de la structure.
    
 **ulFlags**
  
> Indicateur qui indique le type de synchronisation. Elle doit avoir l’une des valeurs suivantes :
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Envoyez le message au serveur (non utilisé actuellement). |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Modification de la hiérarchie push sur le serveur. |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Tirez les modifications de hiérarchie à partir du serveur. |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Envoyer les modifications de message au serveur. |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Retirez les modifications de message à partir du serveur. |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |La synchronisation a été initiée par l’utilisateur et doit être une priorité plus élevée. |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Doit synchroniser uniquement les en-têtes et non les corps complets. |
   
 **psesSync**
  
> [IN] Pointeur vers la session MAPI.
    
 **callBack**
  
> [IN] Pointeur vers l’interface sur laquelle fournir la progression. Il peut être utilisé pour interroger l’interface pour [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] Événement qui se produit lorsque le thread qui vient d’être créé est terminé. Le pointeur doit être valide car il contiendra l’événement.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

