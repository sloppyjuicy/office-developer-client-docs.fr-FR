---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5a0632ffd892c08fdf19de2c9b34607c27534f19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594039"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informe la banque de messages local que la synchronisation est prêt à démarrer.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Indicateurs pour déterminer le comportement approprié lors de la synchronisation. Outlook utilise ces indicateurs dans chaque état de l’ordinateur d’état de réplication pour déterminer les informations qu’il doit fournir pour le client. Par exemple, si le client transmet **SYNC_ONLY_ASSOCIATED**, Outlook renvoie uniquement les informations relatives aux éléments associés (ou masqués). 
    
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

