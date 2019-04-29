---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439575"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Termine la synchronisation à l'état actuel et quitte cet État.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Remarques

Le client doit appeler **IOSTX:: SyncEnd,** pour chaque appel à [IOSTX:: SyncBeg](iostx-syncbeg.md). La structure de données correspondante contient des informations qui indiquent si le client a réussi l'état actuel afin qu'Outlook puisse nettoyer son état interne.
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

