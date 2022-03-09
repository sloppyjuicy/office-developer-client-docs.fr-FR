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
ms.openlocfilehash: 1d30ab6c1af25664d83e920de54e0fe19a85b424
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371869"
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
  
> [in] Indicateurs pour déterminer le comportement approprié lors de la synchronisation. Outlook utilise ces indicateurs dans chaque état de la machine à états de réplication pour déterminer les informations qu’il doit fournir au client. Par exemple, si le client passe **SYNC_ONLY_ASSOCIATED**, Outlook retournera uniquement les informations relatives aux éléments associés (ou masqués). 
    
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

