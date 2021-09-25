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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 73a5559a22ceece27e692e95d2ab1bc01c654336
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604774"
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
  
>  [in] Code d’erreur. 
    
 _ulFlags_
  
>  [in] Indicateurs pour modifier le comportement. Ce doit être 0. 
    
 _lppMAPIError_
  
>  [out] Pointeur vers la structure **MAPIERROR** qui contient les informations étendues de l’erreur. Voir mapidefs.h pour la définition de type **de LPMAPIERROR**. 
    
## <a name="see-also"></a>Voir aussi



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

