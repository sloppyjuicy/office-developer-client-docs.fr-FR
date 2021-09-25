---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5157637bfd133f09af180253790ae3299c807417
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587957"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informe la boutique de messages locale que la synchronisation est sur le point de démarrer.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Indicateurs pour déterminer le comportement approprié lors de la synchronisation. Outlook utilise ces indicateurs dans chaque état de la machine à états de réplication pour déterminer les informations qu’il doit fournir au client. Par exemple, si le client SYNC_ONLY_ASSOCIATED **,** Outlook retournera uniquement les informations relatives aux éléments associés (ou masqués). 
    
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

