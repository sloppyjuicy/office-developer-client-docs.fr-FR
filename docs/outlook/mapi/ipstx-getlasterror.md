---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784445"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**S’applique à**: Outlook 
  
Obtient des informations sur la dernière erreur étendues.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
>  [in] Code d’erreur. 
    
 _ulFlags_
  
>  [in] Indicateurs pour modifier le comportement. Ce doit être 0. 
    
 _lppMAPIError_
  
>  [out] Pointeur vers la structure **MAPIERROR** qui contient les informations d’étendue de l’erreur. Voir mapidefs.h pour la définition du type de **LPMAPIERROR**. 
    
## <a name="see-also"></a>Voir aussi



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

