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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317191"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informe la Banque de messages locale que la synchronisation est sur le début.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Indicateurs permettant de déterminer le comportement approprié lors de la synchronisation. Outlook utilise ces indicateurs dans chaque État de la machine à États de réplication pour déterminer les informations qu'il doit fournir pour le client. Par exemple, si le client transmet **SYNC_ONLY_ASSOCIATED**, Outlook renverra uniquement les informations relatives aux éléments associés (ou masqués). 
    
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

