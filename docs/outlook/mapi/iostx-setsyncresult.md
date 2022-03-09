---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
ms.openlocfilehash: b2c79e8c486415867aae2e15f484df4498b5fa32
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377147"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le résultat de la synchronisation.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Paramètres

 _hrSync_
  
> [in] Résultat de la synchronisation. 
    
## <a name="remarks"></a>Remarques

Appelez **IOSTX::SetSyncResult** avant **d’appeler IOSTX::SyncEnd** pour informer le magasin local du résultat de la synchronisation. 
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[Constantes MAPI](mapi-constants.md)

