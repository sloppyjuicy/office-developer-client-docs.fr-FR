---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 855d50699a7ada58bd144831709cc72dc65ef322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620484"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations étendues sur la dernière erreur.
  
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
  
>  [out] Pointeur vers la structure **MAPIERROR** qui contient les informations étendues de l’erreur. Voir mapidefs.h pour la définition de type **de LPMAPIERROR**. 
    
## <a name="see-also"></a>Voir aussi



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

