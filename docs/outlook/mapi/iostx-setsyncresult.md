---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332143"
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
  
>  dans Résultat de la synchronisation. 
    
## <a name="remarks"></a>Remarques

Appelez **IOSTX:: SetSyncResult** avant d'appeler **IOSTX:: SyncEnd,** pour informer le magasin local du résultat de la synchronisation. 
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[Constantes MAPI](mapi-constants.md)

