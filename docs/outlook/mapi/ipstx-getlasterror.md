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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414976"
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
  
>  dans Code d'erreur. 
    
 _ulFlags_
  
>  [in] Indicateurs pour modifier le comportement. Cela doit être égal à 0. 
    
 _lppMAPIError_
  
>  remarquer Pointeur vers la structure **MAPIERROR** qui contient les informations étendues pour l'erreur. Voir mapidefs. h pour la définition de type de **LPMAPIERROR**. 
    
## <a name="see-also"></a>Voir aussi



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

