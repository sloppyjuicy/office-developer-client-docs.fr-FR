---
title: MAPISIB
description: Décrit la syntaxe et les membres de MAPISIB, qui est une structure utilisée avec IMAPISync SynchronizeInBackground.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
ms.openlocfilehash: 45531c5b06793eb4e430502ae64fe8869f95a46f
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828198"
---
# <a name="mapisib"></a>MAPISIB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

 **ulSize**
  
> Taille de la structure.
    
 **ulFlags**
  
> Indicateur qui indique le type de synchronisation. Il doit s’agir de l’une des valeurs suivantes :
    
|Flag |Valeur |Description |
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Envoyez le message au serveur (non utilisé actuellement). |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Envoyer (push) les modifications de hiérarchie au serveur. |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Extrayez les modifications de hiérarchie à partir du serveur. |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Envoyer (push) les modifications de message au serveur. |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Extrayez les modifications des messages à partir du serveur. |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |La synchronisation a été lancée par l’utilisateur et doit être une priorité plus élevée. |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Ne doit synchroniser que les en-têtes et non les corps complets. |
   
 **psesSync**
  
> [IN] Pointeur vers la session MAPI.
    
 **punkCallBack**
  
> [IN] Pointeur vers l’interface sur laquelle effectuer la progression. Il peut être utilisé pour interroger l’interface pour [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] Événement qui se produit lorsque le thread qui vient d’être créé est terminé. Le pointeur doit être valide, car il contiendra l’événement.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

