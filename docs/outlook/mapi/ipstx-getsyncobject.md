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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784442"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**S’applique à**: Outlook 
  
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

