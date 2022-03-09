---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
ms.openlocfilehash: 70d2eb92c10e3d00f06049033c52d255969eb3fd
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372205"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations étendues sur la dernière erreur.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Code d’erreur. 
    
 _ulFlags_
  
> [in] Indicateurs pour modifier le comportement. Ce doit être 0. 
    
 _lppMAPIError_
  
> [out] Pointeur vers la structure **MAPIERROR** qui contient les informations étendues de l’erreur. Voir mapidefs.h pour la définition de type **de LPMAPIERROR**. 
    
## <a name="see-also"></a>Voir aussi



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

