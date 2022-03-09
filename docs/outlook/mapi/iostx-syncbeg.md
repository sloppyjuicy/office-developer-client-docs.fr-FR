---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
ms.openlocfilehash: 66a5871658c9a0d3d620f8eb0939dead4d6e444c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379191"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prépare le magasin local pour la synchronisation dans un état particulier et récupère les informations nécessaires à répliquer.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Paramètres

 _uiSync_
  
> [in] État entré par le magasin local. Voici une liste des identifateurs d’état : 
    
LR_SYNC_IDLE
  
> 
    
LR_SYNC
  
> 
    
LR_SYNC_UPLOAD_HIERARCHY
  
> 
    
LR_SYNC_UPLOAD_FOLDER
  
> 
    
LR_SYNC_CONTENTS
  
> 
    
LR_SYNC_UPLOAD_TABLE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_READ
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_DEL
  
> 
    
LR_SYNC_DOWNLOAD_HIERARCHY
  
> 
    
LR_SYNC_DOWNLOAD_TABLE
  
> 
    
 _ppv_
  
> [in]/[out] Pointeur vers la structure de données correspondant à l’état à entrer. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SYNC](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>Remarques

Le client appelle **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** pour définir le résultat de la synchronisation, puis appelle **[IOSTX::SyncEnd](iostx-syncend.md)** pour mettre fin à cet état. Le client doit appeler **[IOSTX::SyncEnd](iostx-syncend.md)** pour chaque appel à **IOSTX::SyncBeg** afin de déterminer si l’état a été répliqué avec succès. Une fois cela déterminé, Outlook pouvez commencer à nettoyer son état interne. 
  
La plupart de ces structures contiennent des informations [out]/[in], ce qui permet à Outlook de transmettre des informations au client et au client de transmettre des informations à Outlook. Lorsque le client appelle **IOSTX::SyncBeg**, Outlook alloue la structure de données pour un état donné et l’initialise avec des informations pour cet état. Il s’agit des informations [sortantes]. Lorsqu’il est dans un état, le client met à jour la structure de données correspondante pour cet état. Il s’agit des informations [in]. 
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

