---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585450"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Démarre une session de synchronisation et obtient l’interface **[IOSTX](iostxiunknown.md)** associé. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Paramètres

 _ppostx_
  
>  [out] Pointeur vers l’interface **IOSTX** à obtenir. 
    
## <a name="remarks"></a>Remarques

L’appelant doit s’assurer que le même dossier n’est pas synchronisé en même temps sur plusieurs threads.
  
## <a name="see-also"></a>Voir aussi



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

