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
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270209"
---
# <a name="mapisib"></a>MAPISIB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette structure est utilisée avec [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
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
  
> Indicateur qui indique le type de synchronisation. Il doit prendre la valeur de l'une des valeurs suivantes:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Envoyez le message au serveur (qui n'est pas en cours d'utilisation).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Modifications apportées à la hiérarchie sur le serveur.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Modifications de la hiérarchie d'extraction du serveur.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Envoyer les modifications de message vers le serveur.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Extraire les modifications de message du serveur.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |La synchronisation a été lancée par l'utilisateur et doit avoir une priorité plus élevée.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Ne doit synchroniser que les en-têtes et pas les corps complets.  <br/> |
   
 **psesSync**
  
> DANS Pointeur vers la session MAPI.
    
 **punkCallBack**
  
> DANS Pointeur vers l'interface sur laquelle fournir la progression. Elle peut être utilisée pour interroger l'interface de [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> REMARQUER Événement qui se produit lorsque le thread qui vient d'être créé est complet. Le pointeur doit être valide, car il contiendra l'événement.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

