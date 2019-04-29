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
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407108"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Démarre une session de synchronisation et obtient l'interface **[IOSTX](iostxiunknown.md)** associée. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Paramètres

 _ppostx_
  
>  remarquer Pointeur vers l'interface **IOSTX** à obtenir. 
    
## <a name="remarks"></a>Remarques

L'appelant doit s'assurer que le même dossier n'est pas synchronisé en même temps sur plusieurs threads.
  
## <a name="see-also"></a>Voir aussi



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

