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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: afb2d133259f5eb8645e67ad1def88097b5ed60b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587831"
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
  
>  [out] Pointeur vers **l’interface IOSTX** à obtenir. 
    
## <a name="remarks"></a>Remarques

L’appelant doit s’assurer que le même dossier n’est pas synchronisé en même temps sur plusieurs threads.
  
## <a name="see-also"></a>Voir aussi



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

