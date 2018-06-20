---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784770"
---
# <a name="mapisib"></a>MAPISIB

  
  
**S’applique à**: Outlook 
  
Cette structure est utilisée avec [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
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

## <a name="members"></a>Membres

 **ulSize**
  
> La taille de la structure.
    
 **ulFlags**
  
> Indicateur qui indique le type de synchronisation. Il doit être une des valeurs suivantes :
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0 x 00000200  <br/> |Envoyer le message vers le serveur (pas en cours d’utilisation).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Propager les modifications de la hiérarchie sur le serveur.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Extraire des modifications de la hiérarchie à partir du serveur.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0 x 00000040  <br/> |Propager les modifications de message au serveur.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Extraire des modifications de message serveur.  <br/> |
|SYNC_ON_DEMAND  <br/> |0 x 20000000  <br/> |La synchronisation a été lancée par l’utilisateur et doit être une priorité plus élevée.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Doit synchroniser uniquement les en-têtes et corps pas complètes.  <br/> |
   
 **psesSync**
  
> [IN] Pointeur vers la session MAPI.
    
 **punkCallBack**
  
> [IN] Pointeur vers l’interface sur laquelle fournir la progression. Il peut être utilisé pour interroger l’interface pour [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] L’événement se produit lorsque le thread qui vient d’être créé est terminé. Le pointeur doit être valid car il contient l’événement.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

