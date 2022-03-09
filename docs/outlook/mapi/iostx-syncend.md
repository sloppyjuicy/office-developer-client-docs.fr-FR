---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
ms.openlocfilehash: f76a333d003310cf68610fb92da4688ad387a09a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381487"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met fin à la synchronisation dans l’état actuel et quitte cet état.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Remarques

Le client doit appeler **IOSTX::SyncEnd** pour chaque appel [à IOSTX::SyncBeg](iostx-syncbeg.md). La structure de données correspondante contient des informations pour indiquer si le client a correctement terminé l’état actuel afin Outlook nettoyer son état interne.
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

