---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
ms.openlocfilehash: a92f0aec02831ed2856fbf88d30c9ee70e292d9f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369658"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Démarre une session de synchronisation et obtient l’interface **[IOSTX](iostxiunknown.md)** associée. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Paramètres

 _ppostx_
  
> [out] Pointeur vers **l’interface IOSTX** à obtenir. 
    
## <a name="remarks"></a>Remarques

L’appelant doit s’assurer que le même dossier n’est pas synchronisé en même temps sur plusieurs threads.
  
## <a name="see-also"></a>Voir aussi



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

