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
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568839"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Met fin à la synchronisation dans l’état actuel et quitte cet état.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Remarques

Le client doit appeler **IOSTX::SyncEnd** pour chaque appel à [IOSTX::SyncBeg](iostx-syncbeg.md). La structure de données correspondante conserve des informations pour indiquer si le client a terminé l’état actuel afin qu’Outlook peut nettoyer son état interne.
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

